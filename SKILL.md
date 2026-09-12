---
name: awwwards-skill
description: Art-direct, build, redesign, or audit visually ambitious websites where project-specific identity and interaction matter, including brands, products, portfolios, campaigns, and editorial experiences. Use for substantial visual direction or transformation; skip routine UI maintenance and non-visual fixes.
---

# Awwwards Skill

Create a memorable experience grounded in the project's content, audience, and identity. Cinematic, editorial, spatial, kinetic, playful, brutalist, minimal, luxury, and restrained work can all be right. Do not impose an "Awwwards aesthetic" or copy a reference site's design.

User and project instructions, including a requested new direction, outrank this skill's defaults. Preserve scope, verified facts, documented brand constraints, and the working stack. Accessibility and performance are part of art direction.

## Choose the Mode

- **Build or redesign:** inspect, art-direct, implement, and verify.
- **Concept:** develop the direction and its feasibility; change code only when requested.
- **Audit:** report evidence and recommendations; stay read-only unless fixes are authorized.
- **Narrow change:** fit the existing system and inspect the affected concern without expanding scope.

## Load Guidance When Needed

Resolve links from the installed skill folder containing this `SKILL.md`, regardless of the project's working directory. Read the relevant guide at the point of decision; do not load the whole collection.

| Need | Reference |
| --- | --- |
| Establish or change direction; inspect assets, screenshots, recordings, or sites | [Visual identity](references/visual-identity.md) |
| Audit an existing experience or plan a substantial redesign | [Critical design audit](references/critical-design-audit.md) |
| Diagnose generic treatments or a direction that lacks identity | [SLOP patterns](references/slop-patterns.md) |
| Audit or implement consequential motion, transitions, scrolling, cursors, video, WebGL, or 3D | [Motion and implementation](references/motion-and-implementation.md) |
| Evaluate a finished experience, compare iterations, or provide requested scores | [Evaluation framework](references/evaluation-framework.md) |
| Find a stronger mechanism when a concept remains generic | [Reformulation examples](references/examples.md) |

## Establish Context

Before substantial work, inspect the codebase, routes, components, real copy, assets, brand rules, and supplied visual references. Use available visual tools to inspect media itself. Separate observed facts, inference, and unknowns; ask only when a missing answer would materially change the result.

Keep a compact working profile, proportional to the task:

- **Product and user job:** purpose, goals, and primary action.
- **Audience and context:** attention, trust, devices, and inputs.
- **Brand and feeling:** intended response, must-keep and must-avoid choices.
- **Observed language:** recurring type, layout, imagery, material, and motion.
- **Visual thesis:** a project truth connected to a visual approach.
- **Content spine:** the reading, narrative, or decision path.
- **Identity anchors:** recurring choices that make the project recognizable.
- **Interaction model:** inputs, feedback, and what movement contributes.
- **Constraints:** stack, browsers, assets and rights, delivery, performance, and unknowns.

Inspect and use strong real material before sourcing or generating replacements. Do not invent brand history, clients, awards, metrics, testimonials, product behavior, or claims. Label permitted placeholders.

## Build and Redesign

1. Establish the context and baseline. For an existing site, capture relevant routes and states, including desktop and mobile when tools permit. For a new site, assess the brief, content, assets, and feasibility. Protect successful decisions.
2. Classify material findings as **preserve**, **refine**, **simplify**, **remove**, **replace**, or **introduce**. Resolve broken tasks, accessibility, content integrity, and loading failures first; choose remaining work by expected project value and risk.
3. Run the signature experience pass below. Make a focused plan connecting composition, typography, media, and behavior. Keep working notes brief; proceed with authorized edits.
4. Build a semantic, responsive, visible core. Prototype uncertain signature mechanics early enough to change direction, with readable content and useful actions available throughout.
5. Integrate the chosen interactions with the lightest reliable implementation. Compare native capabilities, the existing stack, and established libraries; choose by capability, lifecycle, cost, and maintainability.
6. Inspect the rendered result, challenge your own changes, and refine until it shows a net improvement. A successful build alone does not establish visual quality.

## Signature Experience Pass

For visually led work, actively investigate what could make this specific experience memorable. Give the opening viewport particular attention for brand, person, product, venue, campaign, portfolio, entertainment, and story-led projects.

Consider expressive type or kinetic lettering, photography or video, spatial composition, depth or 3D, page and section transitions, scroll choreography, cursor response, micro-interactions, unconventional navigation, mobile recomposition, and loading or transitional moments. These are opportunities, not required ingredients.

Describe a credible candidate through its project connection, composition or behavior, pacing, expected benefit, technical cost, and mobile/reduced-motion/failure alternative. Compare it with stronger static art direction and no addition. Atmosphere, delight, and a demonstration of craft can justify investment alongside explanation and task utility.

Ask: **What will someone remember five minutes later?** If the answer is unconvincing, explore a project-specific signature moment. Keep an intentionally quiet experience when it is stronger. Prefer the simpler implementation when the experience is equivalent; do not mistake minimum effects for maximum quality.

## Non-Negotiable Quality

- Preserve semantic content, accessible names and states, logical focus, visible focus, contrast, readable reflow, and usable controls.
- Keep essential information and actions available without hover, animation, WebGL, or a fine pointer. Respect reduced motion and retain useful feedback.
- Make enhancement failure recoverable. Core content must survive failed fonts, media, scripts, hydration, and observers.
- Preserve expected scrolling and navigation. Custom scrolling, cursors, and navigation must earn their cost and support relevant inputs without trapping users.
- Recompose mobile and intermediate layouts around the same identity; finish the whole experience, including secondary routes and relevant loading, empty, offline, error, and 404 states. Use the [audit guide](references/critical-design-audit.md) to decide when exceptional states deserve a signature treatment.
- Never claim checks or measured results that did not occur.

## Verify and Deliver

Run relevant repository checks. Inspect changed routes and states at narrow, intermediate, and wide widths; exercise keyboard, touch, zoom/reflow, reduced motion, loading failure, console errors, and target browsers where tools permit. Use production-equivalent performance measurements when consequential media or interaction work warrants them.

Compare against the baseline: did identity, hierarchy, content, interaction, responsive composition, and finish improve together? Identify the weakest changed moment. Question generic substitution, competing effects, awkward crops, repetitive layouts, and unnecessary complexity; revise clear failures before delivery.

Report the outcome, important preservation/change decisions, files, checks and measurements, fallbacks, and remaining gaps. Scale the format to the task. For audits, prioritize findings with evidence, impact, and a concrete reformulation. If evidence or tools are missing, state the limitation and continue useful work within scope.
