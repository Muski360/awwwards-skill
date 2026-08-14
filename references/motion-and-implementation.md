# Motion and Implementation

Create a motion grammar from the interaction thesis. Use a few related behaviors across the experience.

## Choose the Tool

Use the least complex tool that can express the concept:

- **CSS:** hover states, focus states, small transitions, keyframes, and simple entrance effects
- **Web Animations API:** controlled sequences without a framework dependency
- **Framer Motion:** React layout transitions, component presence, gestures, and shared layout
- **GSAP:** timelines, ScrollTrigger scenes, SVG choreography, and coordinated sequences
- **Three.js or React Three Fiber:** spatial products, data, environments, or forms that require a render loop

Do not add a motion or 3D library to solve an effect that CSS handles well.

## Define the Grammar

Choose two or three signature behaviors:

- **Entrance:** establish hierarchy in the first viewport
- **Continuity:** connect sections, states, or narrative beats
- **Response:** confirm hover, focus, drag, selection, or submission
- **Depth:** reveal spatial relation when depth carries meaning

Use consistent duration, easing, direction, and distance. Vary them only to communicate hierarchy or state.

## Animation Rules

- Animate transforms and opacity where possible.
- Keep text readable during motion.
- Preserve native scroll and input behavior.
- Trigger work only near the viewport.
- Stop `requestAnimationFrame` loops, video, and WebGL work when hidden.
- Avoid animating large blur regions and full-screen filters on mobile.
- Provide an immediate state for reduced-motion users.
- Ensure hover behavior has a touch and keyboard equivalent.

## 3D Gate

Use 3D when the answer to at least one question is concrete:

1. Does spatial form explain the product?
2. Does camera movement reveal information?
3. Does direct manipulation create useful understanding?
4. Does the brand own a physical or spatial artifact?

Use an image, video, or CSS composition when 3D adds spectacle without meaning.

For approved 3D:

- lazy-load the scene
- cap device pixel ratio
- compress geometry and textures
- reduce draw calls and transparent layers
- pause offscreen rendering
- provide a poster or static fallback
- test touch controls and low-power devices

## Responsive Strategy

- Recompose scenes for mobile instead of shrinking desktop choreography.
- Shorten travel distance and reduce simultaneous motion on small screens.
- Keep primary content outside canvas-only rendering.
- Prevent fixed and sticky elements from covering controls or content.
- Test portrait, landscape, intermediate widths, and browser chrome changes.

## Verification

After each coherent milestone:

1. Run the project’s lint, type, and build checks.
2. Smoke-test primary routes and interactions.
3. Check console errors, failed requests, overflow, and layout shift.
4. Run Lighthouse when the environment supports it.
5. Record measured regressions and improve the largest cost first.

Do not fabricate a performance score. Report blocked or unavailable checks.

## Primary References

- [W3C technique for prefers-reduced-motion](https://www.w3.org/WAI/WCAG21/Techniques/css/C39.html)
- [web.dev animations and performance](https://web.dev/articles/animations-and-performance)
- [web.dev high-performance CSS animations](https://web.dev/articles/animations-guide)
