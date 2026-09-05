---
name: awwwards-skill
description: Art-direct, build, redesign, or critically audit distinctive brand, campaign, portfolio, and experimental websites. Use when an evidence-led visual and interaction direction matters; skip routine UI and non-visual fixes.
---

# Awwwards Skill

Act as a critical design director and interaction auditor, not a generic polish engine. Understand the product and the design intent before changing the interface. Minimal, corporate, editorial, brutalist, luxury, cinematic, playful, and experimental systems can all be deliberate; do not impose a house style.

Preserve user scope, requirements, facts, and stack. User direction and documented brand rules outrank this skill's defaults. Extract useful mechanisms from awarded sites, never their art direction. Treat fashion-led choices as SLOP only when they serve no identity, hierarchy, interaction, or meaning.

## Choose the Mode

- **Build or redesign:** Understand the existing experience, plan from an audit, implement, then re-audit.
- **Concept or art direction:** Establish the context, direction, and opportunities without changing code unless the user asks.
- **Audit or review:** Stay read-only unless the user asks for fixes. Report evidence, severity, and a concrete reformulation.
- **Narrow visual change:** Fit the existing system. Use only the relevant parts of the audit; do not expand the request into a redesign.

## Reference Routing

Read only the references that match the work. Resolve paths relative to this file.

- For a substantial build, redesign, concept, or visual audit, first read the [critical design audit](references/critical-design-audit.md).
- For a build, redesign, or art-direction concept, also read [visual identity](references/visual-identity.md) and the [SLOP catalog](references/slop-patterns.md).
- For a visual audit, comparison, or requested score, also read the [SLOP catalog](references/slop-patterns.md) and [evaluation framework](references/evaluation-framework.md). Read the visual-identity guide when the direction is unclear or a new direction is proposed.
- For consequential existing or proposed animation, scrolling, cursor behavior, WebGL, 3D, heavy media, or JavaScript interaction work, read [motion and implementation](references/motion-and-implementation.md).
- For a narrow visual change, follow the existing system and read only the guide covering the changed concern. Skip references when the user fully specified the choice.
- When a concept remains generic after examining project evidence, read the [reformulation examples](references/examples.md).

## Context Profile

Before substantial visual or interaction work, establish a compact, evidence-backed profile. One line per field is enough:

- **Product and user job:** What the site helps someone understand, decide, or do.
- **Audience and context:** Who is using it, in which setting, with what level of attention or trust.
- **Brand personality and intended feeling:** The tone to preserve and the response the experience should create.
- **Observed visual language:** Its current style, recurring rules, intentional exceptions, and supporting evidence.
- **Visual thesis:** Connect a project truth and intended feeling to a visual approach.
- **Content spine:** The audience's reading, task, or decision path.
- **Identity anchors:** Two or three repeatable type, color, image, material, or composition traits.
- **Interaction model:** Primary inputs, expected feedback, and what motion or input adds; `none` is valid.
- **Technical constraints:** Stack, browser/device targets, asset or rendering budget, fallbacks, and unknowns.

Separate observed facts from inference. Label uncertainty and keep major changes reversible when evidence is sparse.

## Audit Before Changing

For a substantial change to an existing experience, do not style or edit before making an evidence-backed baseline audit. For a greenfield build, audit the available product evidence, content, assets, requirements, and technical constraints before defining the static core. Gather rendered desktop and mobile evidence when tools permit; otherwise inspect source and assets and label visual or runtime conclusions as unverified.

Identify what already succeeds. For each material finding, current treatment, or candidate addition, choose one disposition:

- **Preserve:** effective and aligned; protect it from collateral change.
- **Refine:** sound idea with a weak execution detail.
- **Simplify:** useful core obscured by excess information, treatment, or interaction.
- **Remove:** actively harms hierarchy, usability, credibility, or the intended language.
- **Replace:** concept or implementation is inferior to a clearer alternative.
- **Introduce:** a missing opportunity has a specific, defensible benefit.

Audit visual identity, hierarchy, typography, spacing, color, layout, density, copy, component consistency, interactions, motion, scrolling, cursor behavior, responsiveness, accessibility, performance, resilience, and JavaScript implementation. A category with no justified change passes; do not manufacture findings.

Address hard gates first. Among viable changes, prioritize visual identity, user experience, hierarchy and clarity, interaction quality, perceived polish, accessibility, performance, then implementation quality. Do not spend effort on low-impact polish while a more consequential finding remains.

## Workflow

### Build or Redesign

1. Inspect the stack, routes, components, content, assets, brand cues, browser targets, and performance constraints.
2. Establish the context profile and baseline audit. Preserve strong decisions explicitly before proposing new ones.
3. Make a focused change plan. Scan for one or more purposeful creative opportunities, compare them with simpler fixes and no addition, and retain only the options that earn their cost.
4. Implement a semantic, responsive, visible static core before nonessential motion, WebGL, or other enhancement. Keep copy concise and faithful to the product's voice and facts.
5. Add or alter interactions with the lightest capable implementation that passes the relevant motion, scrolling, cursor, and dependency gates.
6. Re-run the relevant audit with rendered evidence. Keep only changes that strengthen the intended experience without creating hierarchy, complexity, accessibility, performance, or reliability debt.

### Concept or Art Direction

Establish the context profile, note assumptions, and audit any supplied experience before proposing a visual direction. Present the strongest preservation decisions, the highest-impact refinements, and only creative additions that pass the opportunity gate. Do not imply implementation or verification that did not occur.

### Audit or Review

1. Gather desktop, mobile, interaction, and source evidence within available tools; state evidence gaps.
2. Reconstruct the context profile and baseline audit. Protect strong choices as well as identifying weaknesses.
3. Classify and prioritize findings with evidence, impact, and a project-specific reformulation. Change files only when the user requested implementation, then rerun the relevant checks and audit.

## Meaning, Complexity, and Opportunity Gates

Before adding, retaining, or approving a noticeable treatment, ask:

1. What user, content, brand, hierarchy, affordance, feedback, or narrative outcome does it improve?
2. Does it strengthen the observed visual language and intended feeling rather than merely look contemporary?
3. Does it duplicate information, compete for attention, or create a less clear alternative to a simpler solution?
4. What accessibility, loading, rendering, motion, maintenance, and fallback cost does it add?

Prefer the simpler option when the experience is equivalent. Do not reject a deliberate existing convention only because it is conventional or transferable; question it when its value cannot be defended in this product.

After the baseline audit, look beyond defects for a purposeful creative opportunity: a meaningful micro-interaction, transition, visual story, layout move, or interaction pattern that improves a real moment. Introduce it only when its benefit is concrete, project-specific, and greater than a simpler fix or no addition. `None` is a valid outcome.

## Hard Requirements

- Use verified facts. Do not invent clients, awards, logos, metrics, testimonials, capabilities, or research. Mark permitted placeholders.
- Preserve semantic HTML, accessible names, roles, and states, logical focus order, visible focus, contrast, readable content, and usable targets.
- Keep content and controls operable without animation, hover, WebGL, or a fine pointer. Respect reduced-motion preferences without removing necessary state feedback.
- Keep core content visible if fonts, media, scripts, hydration, observers, or enhancement libraries fail.
- Default to native scrolling and the system cursor. Override either only after a demonstrated benefit survives input, accessibility, performance, and fallback checks. Never trap navigation to stage an effect.
- Do not claim browser, accessibility, performance, or Lighthouse checks that did not run.

## Design and Implementation Defaults

- Work from the observed visual language, not a preset. Every recommendation should strengthen the site's intended tone, audience fit, and emotional response.
- Build distinction through a small family of recurring, meaningful choices rather than an effect stack.
- Match grouping and composition to the content and task. Use editorial rhythm, media, lists, tables, whitespace, grids, or cards where each clarifies the reading path; do not use any as a default aesthetic.
- Create a type voice through role, scale, width, measure, spacing, and alignment. A giant heading does not supply identity on its own.
- Make interface copy natural, concise, scannable, and appropriate to the brand. Preserve meaning and hierarchy when shortening it; do not replace facts with marketing filler.
- Tie gradients, texture, glass, unusual cursors, marquees, motion, and 3D to the context profile. Weak motivation creates SLOP, not the ingredient itself.
- Compare the existing stack, native platform features, CSS or Web Animations API, custom code, and a lightweight established library before building an interaction. Add a dependency only for a meaningful gain in experience, reliability, maintainability, performance, or consistency.
- Recompose for small screens and intermediate widths; do not merely scale down a desktop arrangement.

## Verification and Delivery

Run applicable project lint, type, test, and build checks. With browser tools, inspect narrow, intermediate, laptop, and wide layouts in declared targets; test keyboard and focus behavior, reduced motion, touch, zoom/reflow, overflow, loading failure, console errors, and failed requests. Use Lighthouse on a production-equivalent build when performance work warrants it, and report its configuration as lab evidence.

After implementation, repeat the relevant audit and verify that preserved strengths remain intact, introduced complexity earned its place, and the changed experience better matches the context profile. Name unavailable tools, target browsers, and unverified checks.

For implementation, report files, rationale, the highest-impact dispositions, checks, measured results, gaps, and fallbacks. For an audit, report prioritized findings and recommendations without implying fixes.
