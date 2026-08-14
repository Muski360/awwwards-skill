---
name: awwwards-skill
description: Art-direct and implement award-caliber websites with distinct identity, editorial composition, expressive typography, purposeful motion, and performance-aware effects. Use when an AI coding agent must create, redesign, or audit a landing page, portfolio, brand site, campaign, product story, or experimental web interface; remove generic AI-style visual patterns; or turn a conventional frontend into a memorable experience.
---

# Awwwards Skill

Build each experience around a specific brand idea. Use effects to express that idea, guide attention, or improve feedback. Treat decoration without purpose as SLOP.

## Required References

- Read [references/visual-identity.md](references/visual-identity.md) before choosing typography, color, imagery, layout, or art direction.
- Read [references/slop-patterns.md](references/slop-patterns.md) before implementing or auditing a visual concept.
- Read [references/evaluation-framework.md](references/evaluation-framework.md) before the final review or when comparing concepts.
- Read [references/motion-and-implementation.md](references/motion-and-implementation.md) when the work includes animation, WebGL, 3D, scroll effects, or a performance-sensitive frontend.
- Read [references/examples.md](references/examples.md) when the concept lacks specificity or the interface needs a SLOP-to-distinctive reformulation.

## Core Standard

Use “SLOP” for fashionable treatments applied without a relationship to the brand, content, or interaction. A polished surface can still be SLOP when the same design could serve a fintech app, coffee shop, AI startup, or photographer with minor copy changes.

Create distinction through a coherent system:

- one visual thesis
- two or three identity anchors
- one dominant composition per section
- one motion grammar
- one technical budget

Do not imitate an awarded site. Extract a useful mechanism such as pacing, cropping, type scale, scene transitions, or interaction rhythm, then rebuild it from the project’s own content.

## Workflow

1. **Inspect the project.** Identify the framework, routes, components, content, assets, brand cues, browser targets, and current performance constraints. Preserve the existing stack unless the task requires a change.
2. **Write the creative brief.** Define the visual thesis, identity anchors, emotional target, content spine, interaction thesis, and technical budget. Use one sentence for each.
3. **Build the visual system.** Choose typography, palette, grid, image treatment, material language, and motion behavior from evidence in the brief. Follow `references/visual-identity.md`.
4. **Compose the narrative.** Give each section one job and one dominant visual idea. Favor a strong opening, clear progression, proof or depth, and a decisive close.
5. **Implement the static core.** Establish semantic structure, responsive layout, content hierarchy, and image behavior before adding complex motion.
6. **Add purposeful interaction.** Use the lightest tool that can express the interaction thesis. Follow `references/motion-and-implementation.md`.
7. **Run the SLOP audit.** Review each prominent treatment against `references/slop-patterns.md`. Remove or reformulate choices that fail the identity test.
8. **Verify the result.** Test responsive states, keyboard use, contrast, reduced motion, overflow, loading behavior, and the project’s existing checks. Review the result with `references/evaluation-framework.md`. Run Lighthouse and smoke tests after coherent implementation milestones when the environment supports them. Report measured results without inventing scores.

## Visual Decision Gate

Answer these questions before adding a prominent visual device:

1. Which brand or content idea does it reinforce?
2. Which hierarchy, affordance, or narrative problem does it solve?
3. Could the same treatment move unchanged to an unrelated site?
4. What rendering, loading, motion, and accessibility costs does it add?

Remove the device when the first two answers lack substance. Reformulate it when the third answer is yes. Simplify it when the cost exceeds its contribution.

## Non-Negotiable Rules

- **Unmotivated gradient -> SLOP.** Remove it. Keep a gradient only when it models light, depth, data, state, or a documented brand behavior.
- **No visual identity -> SLOP.** Stop styling and derive a visual thesis plus identity anchors before writing more CSS.
- **Default card grid -> SLOP.** Use editorial grouping, rhythm, dividers, media, tables, or spatial hierarchy unless a card represents a real interactive object.
- **Effect stack -> SLOP.** Do not combine glow, glass, grain, parallax, magnetic controls, custom cursors, and 3D to manufacture interest.
- **Template typography -> SLOP.** Create hierarchy through type choice, scale contrast, measure, spacing, and alignment. A giant heading alone does not create identity.
- **Decorative 3D -> SLOP.** Use 3D only when form, space, or interaction carries the product story. Provide a strong static fallback.
- **Motion without narrative or feedback -> SLOP.** Give each animation a role in entrance, continuity, depth, state, or response.
- **Generic copy -> SLOP.** Write concrete product or brand language. Remove vague claims, filler labels, and design commentary from the interface.
- Keep content legible and controls operable without animation.
- Preserve semantic HTML, focus visibility, contrast, and usable target sizes.

## Implementation Discipline

- Use the project’s design tokens and component patterns when they support the new direction. Refactor them when they encode the problem.
- Prefer CSS for layout, transitions, and simple reveals. Add GSAP, Framer Motion, Three.js, or React Three Fiber only when the concept needs their capabilities.
- Animate transforms and opacity where possible. Avoid layout thrashing and continuous work outside the viewport.
- Treat 3D and heavy media as progressive enhancement. Cap rendering cost, lazy-load scenes, pause hidden work, and provide fallbacks.
- Test at narrow mobile, common laptop, and wide desktop sizes. Check intermediate widths instead of tuning only fixed screenshots.
- Respect `prefers-reduced-motion`, keyboard navigation, touch input, and coarse pointers.
- Keep the page usable while fonts, media, or scripts load.

## Delivery Contract

Before implementation, state:

- visual thesis
- identity anchors
- content spine
- interaction thesis
- technical budget

After implementation, report:

- files changed
- distinctive choices and their rationale
- responsive and accessibility checks
- tests, smoke checks, and Lighthouse results that ran
- remaining constraints or fallbacks
