# Critical Design Audit

Use this guide before a substantial build, redesign, concept, or visual audit. Turn project evidence into a preservation and change plan before styling or editing. For a greenfield build, inspect the available product evidence, content, assets, requirements, and constraints before defining the static core. It is a decision aid, not a demand to change every category.

## 1. Establish Intent From Evidence

Create the context profile from `SKILL.md` and distinguish **observed**, **inferred**, and **unknown** information. Look for evidence in the product, real content, assets, component patterns, analytics or research supplied by the user, brand documentation, and the current interaction behavior.

Pay particular attention to:

- **Product and user job:** What must be clear, credible, discoverable, or actionable for the user?
- **Audience and context:** Is attention fleeting, exploratory, high-trust, task-focused, or returning? What devices and inputs matter?
- **Brand personality and feeling:** Which tone is intentional, and what should someone feel or understand after a key moment?
- **Visual language:** Describe recurring type, color, crop, composition, density, material, and interaction rules. Name deliberate departures, too. A quiet or conventional-looking system may be exactly right.
- **Interaction model:** Identify the primary actions, state changes, input methods, and feedback expectations before treating motion as a visual layer.
- **Constraints:** Include real content, supported browsers, stack, available assets, privacy, accessibility, performance, maintenance, and delivery limits.

Do not turn a style label into a prescription. The useful question is: **Does this recommendation strengthen this site's observed visual language, audience fit, and intended feeling?** If evidence is weak, make consequential changes reversible and state the assumption.

## 2. Make a Baseline Audit Map

Capture the relevant routes, states, and desktop/mobile views when possible. Review source, assets, and implementation behavior when rendering is unavailable. Record observations in a compact map; a table is useful but not mandatory:

| Area | Evidence and current strength or risk | Disposition | Highest-value outcome |
| --- | --- | --- | --- |
| Example: feature comparison | Similar card chrome hides the primary choice | Simplify | Make the decision path legible without adding more UI |

Inspect the following as a connected system:

- **Identity and visual language:** art direction, tone, originality, consistency, and whether the system fits the product instead of a trend.
- **Hierarchy and composition:** first-view clarity, reading paths, typography, color, spacing, imagery, layout, and responsive recomposition.
- **Content and density:** information priority, repetition, copy length, labels, calls to action, proof, and component proliferation.
- **Interaction:** affordances, states, feedback, navigation, motion, scroll behavior, cursor behavior, touch, keyboard, and error recovery.
- **Quality and implementation:** component consistency, semantic structure, accessibility, resilience, responsive behavior, media cost, JavaScript lifecycle, dependency fit, and performance.

Mark material areas **Preserve**, **Refine**, **Simplify**, **Remove**, **Replace**, or **Introduce**. Add `not applicable` only when a category truly does not occur. A useful audit protects good decisions; it does not treat every existing element as a defect.

## 3. Decide What Earns Complexity

Useful complexity improves a concrete user task, communicates essential information, reinforces hierarchy, provides necessary feedback, or makes the product's identity more legible. Decorative complexity merely looks interesting, repeats a message, competes for attention, or creates a separate interaction burden.

For each material element, layer, component, text block, effect, or interaction, ask:

1. What unique job does it perform: orientation, task completion, hierarchy, feedback, evidence, or identity?
2. What is lost if it is combined, simplified, or removed?
3. Does it repeat another element's information or visual emphasis?
4. Does it make the reading path, input model, or maintenance burden worse?
5. Is its cost proportionate on the devices and conditions that matter?

Prefer consolidation, removal, or a lighter treatment when the answer is vague. Do not remove intentional contrast, pacing, or an expressive detail simply because it is not utilitarian; it must still have a defensible relationship to the experience.

## 4. Audit Copy as Interface Material

Assess visible copy for purpose, not just grammar. Every string should help someone orient, act, decide, understand a state, or evaluate evidence. Preserve the product's actual tone: concise product copy, warm editorial copy, and formal institutional copy can each be correct when the context supports them.

- Keep the essential subject, action, constraint, and proof. Shorten only when it improves scanning or fit.
- Prefer familiar words, concrete nouns, and direct verbs. Let headings carry hierarchy rather than stacking labels, slogans, and explanations.
- Remove repeated claims, throat-clearing, over-formal phrasing, and generic superlatives. Do not replace them with invented facts or false confidence.
- Check buttons, labels, errors, empty states, confirmations, and help text as carefully as hero copy. The shortest clear string is often better, but no word-count target is a design goal.

## 5. Look for Purposeful Creative Opportunities

After identifying defects and strengths, actively scan for a missing moment that could make the experience more memorable, useful, or distinctive. Consider a visual story, interaction, transition, responsive composition, material detail, or new structure only when it serves the product.

For each credible candidate, record:

- the user moment or content gap it improves;
- the project evidence and visual-language connection;
- the exact behavior or composition, rather than a trend label;
- the expected gain in comprehension, feedback, identity, or delight;
- the simpler alternative and the no-addition alternative;
- accessibility, performance, maintenance, and fallback costs.

Introduce a candidate only when it wins that comparison. One well-judged addition can be valuable; a passing opportunity scan may also conclude that preserving and simplifying the existing system is the strongest direction.

## 6. Prioritize and Re-Audit

Resolve hard failures in accessibility, usability, content integrity, resilience, and core tasks first. Then favor changes with the greatest expected effect on visual identity, user experience, hierarchy and clarity, interaction quality, perceived polish, accessibility, performance, and implementation quality, in that order unless project risk makes a lower item urgent.

After implementation, revisit the changed routes and states with the same evidence where possible. Confirm that:

- preserved strengths survived the work;
- the altered design better expresses the context profile;
- new content, components, and effects earned their attention and cost;
- copy is clearer without losing the brand voice or facts; and
- responsive, accessible, reduced-capability, and failed-enhancement paths still work.

If a change does not show a clear net improvement, refine, simplify, or remove it. Report what was observed, what was inferred, and what remains unverified.
