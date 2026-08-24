---
name: awwwards-skill
description: Art-direct, build, redesign, or visually audit distinctive brand, campaign, portfolio, and experimental websites. Use when project-specific identity matters; skip routine UI and non-visual fixes.
---

# Awwwards Skill

Create expressive sites from the project's brand, content, audience, and constraints. Treat fashion-led choices as SLOP when they serve no identity, hierarchy, interaction, or meaning.

Preserve user scope, requirements, facts, and stack; user direction and documented brand rules outrank this skill's defaults. Extract useful mechanisms from awarded sites, never their art direction.

## Choose the Mode

- **Build or redesign:** Define a direction, implement it, and verify the result.
- **Concept or art direction:** Produce the direction and rationale without changing code unless the user asks.
- **Audit or review:** Stay read-only unless the user asks for fixes. Report evidence, severity, and a concrete reformulation.
- **Narrow visual change:** Fit the existing system. Do not force a new brief or redesign unrelated areas.

## Reference Routing

Read only the references that match the current work. Resolve paths relative to this file.

- For a build, redesign, or art-direction concept, read [visual identity](references/visual-identity.md) and the [SLOP catalog](references/slop-patterns.md).
- For a visual audit, comparison, or requested score, read the [SLOP catalog](references/slop-patterns.md) and [evaluation framework](references/evaluation-framework.md). Add the visual-identity guide when proposing a new direction.
- For animation, scroll effects, WebGL, 3D, heavy media, or performance-sensitive work, read [motion and implementation](references/motion-and-implementation.md).
- For a narrow visual change, follow the existing system and read only the guide covering the changed concern. Skip references when the user fully specified the choice.
- When a concept remains generic after examining project evidence, read the [reformulation examples](references/examples.md).

## Direction Brief

For a substantial concept, build, or redesign, record this brief before styling. One line per field is enough:

- **Visual thesis:** Connect a project truth and intended feeling to a visual approach.
- **Identity anchors:** Choose two or three repeatable type, color, image, material, or composition traits.
- **Content spine:** Order sections or states around the audience's reading, task, or decision path.
- **Interaction rule:** State what motion or input adds; `none` is valid.
- **Technical budget:** Name target browsers/devices, existing stack constraints, acceptable asset or rendering cost, and the failure fallback.

For an audit, infer the fields and flag gaps. A narrow change needs only the relevant fields. When evidence is sparse, state reversible assumptions.

## Workflow

### Build or Redesign

1. Inspect the stack, routes, components, content, assets, brand cues, browser targets, and performance constraints.
2. Write the brief. Derive the visual system and compose each section around a clear job and reading path.
3. Implement a semantic, responsive, visible static core before motion, WebGL, or other enhancement.
4. Add interaction with the lightest capable tool in the project. Add a dependency when the direction requires its capability.
5. Run the SLOP audit, verify the result, and fix the highest-impact failure within scope. Do not remove a sound choice to satisfy a quota.

### Audit or Review

1. Gather rendered desktop and mobile evidence when tools permit. Otherwise inspect source and assets, then label visual and runtime conclusions as unverified.
2. Reconstruct the brief. Prioritize identity, hierarchy, usability, accessibility, performance, and content-integrity findings by severity and evidence. Give a project-specific reformulation.
3. Change files only when the user requested implementation, then rerun the relevant checks.

## Prominent-Treatment Gate

Before adding or approving a prominent device, ask:

1. Which brand or content idea does it reinforce?
2. Which hierarchy, affordance, feedback, or narrative problem does it solve?
3. Could it move unchanged to an unrelated site?
4. What loading, rendering, motion, and accessibility cost does it add?

Remove it when the first two answers lack substance. Reformulate it when it transfers unchanged. Simplify it or provide a static alternative when its cost exceeds its contribution.

## Hard Requirements

- Use verified facts. Do not invent clients, awards, logos, metrics, testimonials, capabilities, or research. Mark permitted placeholders.
- Preserve semantic HTML, accessible names, roles, and states, logical focus order, visible focus, contrast, readable content, and usable targets.
- Keep content and controls operable without animation, hover, WebGL, or a fine pointer. Respect reduced-motion preferences without removing necessary state feedback.
- Keep core content visible if fonts, media, scripts, hydration, observers, or enhancement libraries fail.
- Preserve native scrolling and expected input behavior. Never trap navigation to stage an effect.
- Do not claim browser, accessibility, performance, or Lighthouse checks that did not run.

## Design and Implementation Defaults

- Build distinction through recurring choices, not an effect stack.
- Use editorial grouping, rhythm, media, lists, tables, or spatial hierarchy before a card grid. Keep cards for discrete interactive objects.
- Create a type voice through role, scale, width, measure, spacing, and alignment. A giant heading does not supply identity on its own.
- Tie gradients, texture, glass, unusual cursors, marquees, motion, and 3D to the brief. Weak motivation creates SLOP, not the ingredient itself.
- Prefer project tokens, existing dependencies, and CSS for simple behavior. Treat heavy media and 3D as progressive enhancement. Recompose for small screens and intermediate widths.

## Verification and Delivery

Run applicable project lint, type, test, and build checks. With browser tools, inspect narrow, intermediate, laptop, and wide layouts in declared targets; test keyboard and focus behavior, reduced motion, touch, zoom/reflow, overflow, loading failure, console errors, and failed requests. Use Lighthouse on a production-equivalent build when performance work warrants it, and report its configuration as lab evidence.

Name unavailable tools, target browsers, and unverified checks.

For implementation, report files, rationale, checks, measured results, gaps, and fallbacks. For an audit, report prioritized findings and recommendations without implying fixes.
