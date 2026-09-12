# Motion and Implementation

Use for consequential animation, transitions, scrolling, cursors, heavy media, WebGL, and 3D. Start with the signature candidate and constraints from [SKILL.md](../SKILL.md). Judge identity, atmosphere, feedback, and narrative alongside usability; movement need not explain a physical product to earn its place.

## Specify the Behavior

Describe the trigger, subject, transformation, timing, overlap, settled state, and exit. State what stays readable and stable while another layer moves. Connect entrances, continuity, responses, and depth through a related family of behaviors; tune duration and easing to distance, hierarchy, and input.

For kinetic type, preserve reading time and a legible resting state. For masks and image transformations, maintain a clear focal subject. Keep controls responsive during choreography; handle interruption, reversal, repeated activation, and rapid navigation. A transition must not become a queue users wait through.

## Choose the Mechanism

Check the installed versions, target browsers, and current authoritative documentation when selecting APIs. Feature support is specific to an API and engine; avoid a blanket "native is supported" assumption.

| Need | Candidates and decision |
| --- | --- |
| State changes and local sequences | CSS transitions/keyframes or Web Animations; choose a library when coordination or lifecycle becomes simpler |
| Shared elements or route continuity | Native View Transitions where the required mode is supported; framework/library orchestration for unmet needs |
| Scroll-linked progress or reveals | Native CSS scroll/view timelines; GSAP ScrollTrigger for more complex scenes or target gaps |
| React layout, presence, gestures | Motion for React when it fits the installed stack |
| Coordinated timelines, masks, SVG | GSAP when it materially reduces synchronization work |
| Altered scroll response | Existing solution or a focused utility such as Lenis only after the input checks below |
| Spatial rendering | Three.js; React Three Fiber when React composition and lifecycle help |

Reuse a suitable existing dependency. Do not migrate `framer-motion` just to use the current `motion` package name. Record a new dependency's capability gain, bundle cost, fallback, and teardown plan. Avoid both unnecessary libraries and fragile custom replacements.

### Native Enhancements

[View Transitions](https://developer.mozilla.org/en-US/docs/Web/API/View_Transition_API/Using) support same-document changes through `document.startViewTransition` and cross-document navigation through separate opt-in mechanisms. Check the required mode: cross-document transitions require same-origin navigation and both documents opting in. Preserve ordinary DOM updates/navigation when unavailable or skipped. Suppress nonessential transition animation under reduced motion; keep route focus, history, and scroll restoration correct.

[CSS scroll-driven animations](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Scroll-driven_animations) can follow scroll or element visibility progress without replacing native input. Keep content visible outside a feature/reduced-motion guard. Declare `animation-timeline` after an `animation` shorthand, which [resets the timeline](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/animation-timeline). Unsupported timelines must not leave invisible content or accidentally run a timed substitute.

### Framework and Lifecycle Boundaries

- Isolate DOM, pointer, media-query, and renderer initialization in the framework's browser lifecycle. Check import-time side effects as well as calls; dynamically import an incompatible enhancement when needed.
- In React Server Component frameworks, keep interactive client boundaries small. `'use client'` does not prevent initial server prerendering; keep server output and initial hydration deterministic. Disable SSR only for an incompatible island with a useful fallback, not the whole page. See [Next.js server/client behavior](https://nextjs.org/docs/app/getting-started/server-and-client-components).
- [Motion components](https://motion.dev/docs/react-motion-component) support SSR. Use `motion/react` within a client boundary or the documented `motion/react-client` entry for supported RSC composition; hooks and event logic still need the appropriate client boundary. Avoid initial hidden content that depends on hydration to become readable.
- In React with GSAP, consider [`useGSAP`](https://gsap.com/resources/React/) from `@gsap/react` for scoped cleanup. [`gsap.context()`](https://gsap.com/docs/v3/GSAP/gsap.context%28%29/) with proper reversion remains valid. Delayed callbacks and handlers need context-safe animation ownership; manually attached listeners still need removal.
- On unmount, route/breakpoint changes, or reinitialization, revert owned animations, remove listeners, disconnect observers, clear timers, and stop render loops. Test repeated mounting and navigation for duplicates and leaks.

## Input, Scrolling, and Cursors

Native scrolling and the system cursor provide a reliable starting point. Custom behavior can support expressive identity, spatial relationships, or feedback when its benefit survives input and performance testing.

For altered scrolling or staged scenes, preserve wheel, trackpad, keyboard, touch, selection, anchors, skip links, focus-driven scroll, nested regions, history, and restoration. Keep an intelligible reading order and a direct way through or past the scene. A sticky narrative can follow native progress; unusual horizontal or spatial navigation still needs discoverable controls and meaningful locations.

A custom cursor is optional fine-pointer enhancement. Preserve pointing, link, text-selection, and form affordances; keep overlays from intercepting input. Avoid lag or obscuring content. Disable the decoration for coarse pointers and retain keyboard-visible equivalents for useful feedback. Batch pointer updates to the render cycle rather than rerendering the application on every event.

For mobile, choose positive alternatives: a native swipeable media sequence with visible controls, reachable navigation, or a focused detail tray when appropriate. Recompose crops and type around touch use. Preserve page panning and pinch zoom, pad targets, and provide alternatives to drag-only actions. Keep sticky layers clear of focus, controls, safe areas, and changing browser chrome. Scroll snap is optional; avoid forced stops that hide content or trap movement.

## Accessible Motion

Start with visible semantic DOM and apply reveal setup only after successful initialization. Ensure a failure after setup can restore visibility. Keep visual state, focusability, and the accessibility tree synchronized during exits.

Split text without breaking the heading's meaning, reading order, inline semantics, or accessible name. Hide only visual duplicates from assistive technology; do not rely on an `aria-label` on arbitrary spans. Recalculate line-dependent splits when fonts or layout change.

Respect reduced motion in CSS and JavaScript, including preference changes. Recompose spatial, continuous, and scroll-linked motion into legible states while preserving useful feedback. Provide [pause/stop controls](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide.html) for applicable ongoing automatic movement; reduced-motion support alone does not replace these controls.

## Video, WebGL, and 3D

Choose real-time 3D when spatial explanation, manipulation, an authored brand world, or a meaningful transformation improves the experience over a still, video, or CSS composition. Atmosphere can justify it; generic spectacle cannot. Define a reduced-capability composition before integrating the scene.

- Reserve media dimensions and choose responsive sources and crops. Prioritize the likely LCP image/poster; defer nonessential video downloads, scene code, and below-fold assets without delaying useful content.
- For decorative video, plan a strong poster, muted inline playback, and a composed failure state. [Autoplay can be denied](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Autoplay); handle rejected `play()` calls. Give meaningful media usable controls and appropriate captions, transcripts, or descriptions. Avoid unsolicited audio.
- Pause nonessential media and render loops offscreen or in hidden tabs. Render static scenes on demand. Cap or adapt pixel ratio and quality based on measured cost.
- Budget decoded textures, draw calls, transparency, geometry, video decode, and GPU memory as well as network bytes. Large blur/filter/composited layers can also be expensive; transforms alone do not guarantee smoothness.
- Keep core information and actions in accessible DOM. Test unsupported WebGL, asset failure, and context loss. Decorative scenes can use posters; essential canvas interactions need a usable DOM equivalent.
- Dispose resources the scene owns, including geometry, materials, textures, render targets, controls, and renderer state. Account for shared asset ownership. See [Three.js resource cleanup](https://threejs.org/manual/pages/how-to-dispose-of-objects.html).

## Verify the Chosen Experience

Exercise relevant inputs, mobile recomposition, reduced motion, rapid transitions, repeat navigation, blocked autoplay, missing assets, and enhancement teardown. Measure loading, frame cost, layout stability, and responsiveness on representative conditions; inspect memory or GPU behavior when the work warrants it.

Use bounded server-readiness and navigation waits and finite timeouts. In unattended environments, use the supported headless mode; preserve the normal rendering configuration for measurements. Stop only processes you started. Report unavailable tools instead of inventing results. Viewport emulation is not a device test, and a WebKit run is not branded Safari. Record build, engine/device, throttling, and routes for performance evidence; [Lighthouse results vary](https://github.com/GoogleChrome/lighthouse/blob/main/docs/variability.md).
