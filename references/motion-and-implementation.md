# Motion and Implementation

Treat motion, scrolling, cursors, and interaction code as a system to audit, not as automatic polish. Start with the current experience and the interaction rule. Reuse the project's working stack when it fits; add a dependency only after a demonstrated capability gap justifies it.

## Audit Before Building

Inventory consequential existing and proposed motion, scroll, cursor, and JavaScript behaviors. For each, choose **Keep/Preserve**, **Refine**, **Simplify**, **Replace**, **Reduce**, **Remove**, or **Introduce**. Test it against these questions:

1. Does it serve a specific purpose?
2. Does it improve comprehension, feedback, orientation, or interaction?
3. Does it reinforce the visual identity or interaction model?
4. Are its timing, travel, intensity, and repetition appropriate?
5. Does it create friction, distraction, motion discomfort, input conflict, or performance cost?
6. Would removal produce an equal or better experience?

Do not preserve an animation merely because it exists. Static behavior or no added motion is a passing outcome. For an approved behavior, name the user moment, expected benefit, fallback, and validation path before implementation.

### Scrolling Gate

Native scrolling is the baseline, not an automatic failure of ambition. Consider smooth or inertial scrolling only when it creates a defined benefit that fits the interaction model, such as a coherent long-form narrative or a demonstrably better response to an existing problem. Do not use it to conceal weak composition or manufacture a premium feel.

Before changing scroll behavior, test or plan for:

- keyboard, touch, wheel, trackpad, text selection, focus navigation, skip links, and browser zoom;
- anchors, history navigation, restoration, programmatic focus/scroll, nested scrollers, and route changes;
- reduced-motion preference, an intelligible native fallback, and a way to escape any staged scene;
- latency, frame cost, battery impact, and behavior on representative lower-power devices.

Keep native scrolling when custom behavior is not materially better. A lightweight tool such as Lenis can be appropriate when it solves a demonstrated smooth-scroll or orchestration need more reliably than the current implementation, but it still must preserve expected browser behavior and have a justified lifecycle, fallback, and bundle cost.

### Cursor Gate

The system cursor is the baseline. Consider a custom cursor only as nonessential, fine-pointer feedback that makes a real interaction state or object relationship clearer and supports the visual language. It must not replace meaning with spectacle.

- Keep normal affordances for links, controls, text selection, and form fields; never hide the pointer where the system cursor communicates a needed state.
- Disable or avoid it for coarse pointers, keyboard-only use, unsupported devices, and contexts where it obscures content or causes lag.
- Provide the same information through visible focus, hover-independent controls, and direct activation. Remove it when it merely trails, stretches, or decorates.

## Choose the Implementation

Compare the existing stack, native platform behavior, CSS or Web Animations API, focused custom code, and a lightweight established library. Choose the smallest option that materially improves user experience, reliability, maintainability, performance, or consistency. Do not hand-roll a complex behavior merely to avoid a dependency, and do not add a dependency merely because it is fashionable.

- **Native platform:** default scrolling, semantic controls, focus, anchors, and browser navigation when they meet the need
- **CSS:** state transitions, keyframes, simple reveals, and target-supported scroll-driven effects
- **Web Animations API:** imperative DOM sequences without a framework dependency
- **Motion for React:** React presence, layout transitions, gestures, and shared layout
- **GSAP:** coordinated timelines, ScrollTrigger scenes, SVG choreography, and complex sequencing
- **Lenis or another focused scroll utility:** justified smooth-scroll, inertia, or scroll-orchestration needs after the scrolling gate passes
- **Three.js:** direct control of a WebGL or 3D scene
- **React Three Fiber:** a React renderer for Three.js when React lifecycle and composition help the project

For vanilla JavaScript, inspect listeners, observers, timers, state ownership, cleanup, and failure paths before replacing or extending behavior. Prefer a focused library when it removes substantial bespoke synchronization, accessibility, browser-compatibility, or lifecycle risk; otherwise keep the native or lightweight custom implementation. For new React installs, the current Motion package uses `motion` and `motion/react`. Preserve an existing `framer-motion` installation unless the task includes migration. Do not add a motion or 3D library for an effect that CSS or the project's current dependency handles well.

When choosing a new implementation, record the capability gap, alternatives considered, integration and teardown plan, fallback, dependency or bundle cost, and the evidence that will validate the choice.

## Define the Motion System

For approved motion, choose a small family of related behaviors. Two or three often suffice; this is a default, not a quota.

- **Entrance:** establish hierarchy in the first viewport
- **Continuity:** connect sections, states, or narrative beats
- **Response:** confirm focus, activation, drag, selection, or submission
- **Depth:** reveal spatial relationships when depth carries meaning

Share timing, easing, direction, and travel across related behaviors. Vary them to communicate hierarchy, causality, or state.

## Progressive Enhancement and Accessibility

- Start with visible, semantic DOM content. Apply hidden reveal states after enhancement initializes so failed scripts, hydration, observers, or assets cannot strand content offscreen or at zero opacity.
- Animate transforms and opacity when they fit, then measure. Large composited layers, blur, filters, and careless `will-change` use can still cost memory and frame time.
- Preserve expected browser scroll and input behavior unless an approved enhancement demonstrably improves it. Defer nonessential visual work until it nears the viewport; keep essential application logic independent from observation.
- No information or action may exist only on hover. Provide focus and activation or tap paths where they apply.
- Keep visual state, focusability, and the accessibility tree in sync. Hidden or exiting controls must leave focus navigation. Text splitting and cloned marquees must preserve reading order and accessible names, with true duplicates hidden from assistive technology.
- For reduced motion, suppress or reformulate nonessential spatial, parallax, scroll-linked, and continuous motion. Preserve useful state feedback through direct changes or restrained fades. JavaScript and library logic should respond if the preference changes during a session.
- Provide pause or stop controls for autoplay movement that persists or competes with use.
- On unmount, route change, or breakpoint change, cancel or revert timelines and animations; remove listeners and observers; clear scheduled work.

## 3D Gate

Use 3D when at least one answer is concrete:

1. Does spatial form explain the product?
2. Does camera movement reveal information?
3. Does direct manipulation improve understanding?
4. Does the brand own a physical or spatial artifact?

Use an image, video, or CSS composition when 3D adds spectacle without meaning.

For approved 3D:

- Check support and feature requirements before loading the scene.
- Lazy-load noncritical code and assets. Do not lazy-load likely LCP or hero media.
- Render on demand for static scenes. Run a continuous loop only while pixels change, and pause nonessential offscreen work.
- Cap or adapt device pixel ratio and scene quality. Reduce draw calls, transparent layers, geometry, and decoded texture dimensions; download compression alone does not reduce GPU memory.
- Keep essential content and actions in accessible DOM. A poster works for decoration; an essential canvas interaction needs a DOM equivalent.
- Handle unsupported WebGL, asset failure, and context loss with a tested static fallback or DOM path.
- Dispose unused geometry, materials, textures, render targets, controls, and renderer resources.
- Test touch input, representative low-power hardware, load failure, and teardown.

## Responsive Media and Composition

- Recompose scenes for small screens instead of shrinking desktop choreography.
- Shorten travel and reduce simultaneous motion where space or device cost requires it.
- Reserve image and video dimensions, use responsive sources, and lazy-load below-fold media.
- Keep primary content outside canvas-only rendering.
- Prevent fixed and sticky layers from covering focus, controls, or browser UI.
- Test portrait, landscape, intermediate widths, text enlargement, and browser chrome changes.

## Motion, Scroll, and Cursor Verification

After the core checks in `SKILL.md`:

1. Test each enhanced interaction across the relevant input types and target engines. A viewport emulator is not a device test, and a WebKit engine run is not branded Safari.
2. Check initial content visibility, focus and accessibility-tree state during transitions, reduced-motion behavior, persistent-motion controls, teardown on route or breakpoint changes, and fixed or sticky layer collisions.
3. For changed scrolling, exercise keyboard, touch, wheel, trackpad, anchors, navigation history, focus-driven scroll, nested regions, restoration, and the native or reduced-motion fallback. For a custom cursor, check fine and coarse pointers, text and form interactions, latency, obscured content, and keyboard-visible equivalents.
4. Exercise animation-asset failure plus WebGL support, context-loss, and DOM-fallback paths where applicable.
5. Measure animation cost with available browser performance tools. Do not infer smoothness from the library or CSS properties alone.

## Primary References

- [Motion for React upgrade guide](https://motion.dev/docs/react-upgrade-guide)
- [W3C reduced-motion CSS technique](https://www.w3.org/WAI/WCAG22/Techniques/css/C39)
- [W3C reduced-motion script technique](https://www.w3.org/WAI/WCAG22/Techniques/client-side-script/SCR40)
- [web.dev high-performance CSS animations](https://web.dev/articles/animations-guide)
- [Three.js rendering on demand](https://threejs.org/manual/en/rendering-on-demand.html)
- [Three.js cleanup](https://threejs.org/manual/en/how-to-dispose-of-objects.html)
- [React Three Fiber Canvas API](https://github.com/pmndrs/react-three-fiber/blob/master/docs/API/canvas.mdx)
- [GSAP context cleanup](https://gsap.com/docs/v3/GSAP/gsap.context%28%29/)
- [Lighthouse variability](https://github.com/GoogleChrome/lighthouse/blob/main/docs/variability.md)
