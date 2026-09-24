---
name: apple-design
description: Apple's approach to interface design and fluid, physical motion, translated for the web. Use when building or reviewing gesture-driven UI, spring animations, drag/swipe/sheet interactions, momentum and interruptible transitions, translucent materials and depth, typography (optical sizing, tracking, leading), reduced-motion, or the design foundations (feedback, spatial consistency, restraint) behind Apple-style interfaces.
---

# Apple Design

## Initial Response

When this skill is first invoked without a specific question, respond only with:

> I'm ready to help you build fluid, Apple-style interfaces on the web, my knowledge comes from Apple's WWDC design talks, translated for the web.

Do not provide any other information until the user asks a question.

## Core idea

Build interfaces that behave like a physical extension of the person using them: respond immediately, track continuously, carry momentum, resist at boundaries, and accept reversal at any instant. Start each motion from its current on-screen value, inherit gesture velocity, project momentum forward, and use interruptible springs rather than prescribed timelines.

Use this guidance to serve safety/predictability, understanding, achievement, and joy. Favor purposeful restraint: every element, material, motion, and confirmation must earn its place.

## Response and direct manipulation

- Respond on `pointerdown`, not release. Apply pressed feedback immediately; do not introduce nonessential debounce, timers, or transition waits on the input path.
- Keep feedback continuous throughout the gesture. For drags, sliders, and drawers, update the presentation 1:1 with the pointer rather than animating only after release.
- Use Pointer Events and `setPointerCapture` so interaction continues outside the element bounds. Preserve the offset at which the person grabbed the object; do not snap it to the pointer center.
- Keep a short position/timestamp history to calculate release velocity.
- Add approximately 10px hysteresis before committing to a drag direction. Detect plausible gestures in parallel, then cancel the losing recognizers after intent is clear.
- For taps, show feedback on touch-down and commit on touch-up. Let the person cancel a tap by dragging away and return to it. Do not add double-tap delays unless double-tap is actually supported.

```css
.button:active {
  transform: scale(0.97);
  transition: transform 100ms ease-out;
}
```

```js
el.addEventListener('pointerdown', (event) => {
  el.setPointerCapture(event.pointerId);
  const grabOffset = event.clientY - el.getBoundingClientRect().top;
  // Record position and timestamp samples for release velocity.
});
```

## Interruptibility and springs

Treat an animation as an ongoing conversation, not a fixed-duration sequence.

- Never lock input during a transition.
- On interruption, start from the presentation (live rendered) value, never a stale logical target. Reading the live transform avoids a visible jump.
- Do not use CSS transitions or keyframes for gesture-driven motion; they cannot be smoothly grabbed and reversed. Use a spring that retargets from the current value and blends velocity.
- Decompose 2D motion into independent X and Y springs when the axes have different velocities.
- Use critically damped motion by default: damping ratio `1.0`, response `0.3–0.4s`. It settles without distracting overshoot.
- Reserve slight under-damping (roughly `0.8`, response `0.3–0.4s`) for momentum-driven releases such as a flick, throw, drawer, or sheet—not for passive menu entrances.

| Interaction | Damping | Response |
| --- | --- | --- |
| Move / reposition | `1.0` | `0.4s` |
| Rotation | `0.8` | `0.4s` |
| Drawer / sheet | `0.8` | `0.3s` |

With Motion/Framer Motion, use a no-bounce spring for ordinary UI and a small bounce only after a momentum gesture. Preserve absolute gesture velocity when the API supports it.

```js
import { animate } from 'motion';

animate(el, { y: 0 }, { type: 'spring', bounce: 0, duration: 0.4 });
animate(el, { y: target }, {
  type: 'spring',
  bounce: 0.2,
  duration: 0.4,
  velocity: releaseVelocity,
});
```

## Velocity handoff and momentum projection

At release, continue at the finger's exact velocity so drag and spring have no seam. When a library requires normalized velocity, calculate it as:

```text
relativeVelocity = gestureVelocity / (targetValue - currentValue)
```

Choose a snap target from the projected resting position, not merely the release point. Use Apple's exponential-decay projection rather than textbook constant-deceleration physics:

```js
function project(initialVelocity, decelerationRate = 0.998) {
  return (initialVelocity / 1000) * decelerationRate / (1 - decelerationRate);
}

const projectedEndpoint = currentPosition + project(releaseVelocity);
const target = nearestSnapPoint(projectedEndpoint);
animateSpringTo(target, { velocity: releaseVelocity });
```

Use about `0.998` for normal scroll-like projection and `0.99` for a snappier feel. Choose reverse versus commit from release velocity sign when appropriate, rather than position alone.

## Spatial consistency and soft bounds

- Enter and exit along the same path. A panel entering from the right also dismisses to the right.
- Anchor menus, popovers, and sheets to their trigger with a meaningful `transform-origin`; preserve the source-to-result relationship.
- Mirror easing for reversible non-gesture transitions using inverse cubic-bezier curves.
- Make intermediate states indicate the eventual direction. Movement should point toward its outcome.
- At boundaries, progressively resist rather than stop abruptly. Rubber-banding remains responsive while communicating that there is no further space.

```js
function rubberband(overshoot, dimension, constant = 0.55) {
  return (overshoot * dimension * constant) /
    (dimension + constant * Math.abs(overshoot));
}
```

## Smooth frames

Animate display-synchronously with `requestAnimationFrame` or a spring library and prefer compositor properties (`transform`, `opacity`). Use `will-change` only where motion is imminent. Keep per-frame travel small enough to avoid strobing. For unusually fast movement, a subtle stretch or blur can communicate speed better than a sharp streak.

## Materials and depth

Use translucent material to communicate hierarchy without stealing focus.

- Let content scroll beneath translucent navigation, toolbars, and panels; avoid opaque fixed bars where material would preserve continuity.
- Use heavier/darker material for structural separation and lighter material for interactive emphasis. Do not stack light translucent surfaces.
- Scale material weight with surface size: larger surfaces need stronger blur and more separation. Tune shadows to the background's visual busyness.
- Use a dimming scrim for modal focus. For parallel, nonblocking panels, use translucency and spatial offset without a scrim. Progressively push and dim parent layers for stacked sheets.
- Keep text legible over changing material with higher contrast, slightly heavier weight, and modest tracking. Place color on solid layers rather than a translucent foreground.
- Prefer a blur or gradient scroll-edge effect where floating chrome overlaps content over a permanent 1px divider.
- Materialize glass: animate blur radius and scale alongside opacity so a surface arrives as material, not just a fade.

```css
.toolbar {
  background: rgba(255, 255, 255, 0.6);
  backdrop-filter: blur(20px) saturate(180%);
  border-top: 1px solid rgba(255, 255, 255, 0.4);
}
```

## Multimodal feedback

Use sound and haptics only when they serve a meaningful event. Align feedback on the same frame as its visual cause; delayed sensory feedback breaks causality. Match its character to the action, and reserve it for status, success, error, commit, or snap moments so it remains useful rather than noisy.

## Accessibility and reduced motion

Reduced motion preserves understanding; it does not remove feedback.

- Under `prefers-reduced-motion: reduce`, replace slides, parallax, and elastic springs with short opacity cross-fades or static state changes. Remove overshoot while retaining useful opacity and color feedback.
- Under `prefers-reduced-transparency: reduce`, make materials more opaque and remove blur.
- Under `prefers-contrast: more`, use near-solid backgrounds and clear contrasting borders.
- Avoid full-viewport moving backgrounds, slow looping oscillation, and abrupt brightness shifts. During large repositioning, reduce the moving surface opacity and restore it after settling.

```css
@media (prefers-reduced-motion: reduce) {
  .sheet { transition: opacity 200ms ease; transform: none !important; }
}

@media (prefers-reduced-transparency: reduce) {
  .toolbar { background: white; backdrop-filter: none; }
}
```

## Typography

Use the platform system font unless there is a clear reason to override it. Build hierarchy from weight, size, and leading together; respect user text size and scale spacing in `rem`/`em` so layouts grow with type.

- Apply size-specific tracking: tighten large display type (often around `-0.02em`); leave body copy near zero or slightly positive at small sizes.
- Use tight leading for large headings and looser leading for body text; adapt for scripts with taller ascenders/descenders or dense information.
- Enable optical sizing when the font supports it.

```css
:root { font: 100%/1.5 system-ui, sans-serif; }

.display {
  font-size: clamp(2rem, 5vw, 4rem);
  line-height: 1.05;
  letter-spacing: -0.02em;
  font-optical-sizing: auto;
}
```

## Design foundations

Apply these principles during design and review:

1. **Purpose:** decide what not to build; spend attention and trust deliberately.
2. **Agency:** keep people in control, make recovery and undo easy, and reserve confirmation dialogs for genuinely destructive irreversible actions.
3. **Responsibility:** act in the person's interest; request only necessary data at the right time and account for safety risks.
4. **Familiarity:** build on established metaphors and consistent behavior; break conventions only when evidence shows a better result.
5. **Flexibility:** adapt to device, context, ability, language, and expertise; offer personalization when no single layout suits everyone.
6. **Simplicity:** remove the unnecessary, clarify hierarchy, use plain specific labels, and place advanced controls one level deeper.
7. **Craft:** defend spacing, alignment, typography, contrast, and feedback details; maintain quality as features and hardware evolve.
8. **Delight:** let calm, confidence, or excitement emerge from the preceding principles rather than decoration layered on top.

Ensure every screen answers: where am I, where can I go, what is there, and how do I leave? Use proximity and control placement to map actions directly to their effects. Provide status, completion, warning, and error feedback at the moment it is useful, including inline validation rather than late-form submission surprises.

## Working process

Prototype interactions, not only static screens. Design movement and visual treatment together, then test with people in their real context. Review complex transitions in slow motion or frame-by-frame to find discontinuities, unsafe motion, and details that full-speed playback hides.

## Quick reference

| Need | Technique | Concrete value |
| --- | --- | --- |
| Default UI spring | Critically damped, no overshoot | `damping: 1.0`, response `0.3–0.4s` |
| Flick release | Slightly under-damped spring | `damping: ~0.8`, response `0.3–0.4s` |
| Drag handoff | Preserve release velocity | raw px/s when supported |
| Flick target | Project velocity before snapping | `current + (v/1000) * d / (1-d)` |
| Clean interruption | Start at live presentation value | read the rendered transform |
| 1:1 dragging | Pointer Events + capture | preserve grab offset |
| Boundary | Progressive rubber-band resistance | never hard-stop |
| Feedback | Press immediately and update continuously | use pointer-down |
| Translucent chrome | Backdrop-filter material | let content scroll underneath |
| Type | Size-specific tracking | large display around `-0.02em` |
| Reduced motion | Cross-fade instead of spring/slide | `prefers-reduced-motion` |
