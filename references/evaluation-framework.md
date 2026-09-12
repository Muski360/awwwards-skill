# Evaluation Framework

Use for finished-experience reviews, comparisons, or requested scoring. Default to qualitative evidence. Evaluate the actual brief and available states; do not predict awards or present this as an official Awwwards score.

## Quality Lens

| Dimension | Evidence to examine |
| --- | --- |
| Project-specific identity | A visual thesis grounded in the product, audience, and assets; a recognizable point of view without forced novelty |
| System coherence | Type, composition, media, material, motion, and navigation expressing related choices |
| First impression | Hierarchy, tone, premise, intrigue, and useful action; a memorable opening when appropriate |
| Content and usability | Comprehension, reading path, navigation, feedback, and task completion |
| Motion and interaction | Deliberate timing, responsiveness, continuity, interruption, input parity, and appropriate rest |
| Responsive art direction | Intentional recomposition across small, intermediate, and large layouts |
| Finish | Spacing, type details, crops, state changes, route continuity, loading, errors, and edge cases |

Transferability is a diagnostic signal, not a gate. Familiar controls or a quiet design can fit the brief. A prominent generic treatment deserves attention when it weakens the project's identity or purpose.

## Technical Acceptance

Assess applicable concerns as **pass**, **fail**, **unverified**, or **not applicable**, with evidence:

- Semantic content, accessibility, keyboard/focus, contrast, zoom/reflow, and relevant input methods.
- Responsive behavior, supported browsers, reduced motion, and enhancement failure paths.
- Loading and rendering cost, layout stability, interaction responsiveness, and media budgets.
- Navigation, not-found behavior where relevant, metadata/indexability appropriate to the project, and content integrity.
- Lifecycle, teardown, dependency fit, maintainability, and available build/type/lint/test checks.

Core task failures, inaccessible core controls, fabricated claims, or loss of the only usable content path block acceptance. Continue the audit and report remediation. If fixes are authorized, implement and recheck them. Do not stop the task or ask for renewed permission merely because a finding blocks acceptance.

Technical failures cannot be averaged away by visual scores. Automated accessibility tools and Lighthouse supply partial evidence; they do not certify the whole experience. Use current [WCAG guidance](https://www.w3.org/TR/WCAG22/) and the project's stated targets.

## Evidence and Dispositions

Cite a route, viewport, state, timestamp, element, or source location for each material finding. Separate observed failures from inferred risks. Without rendered evidence, avoid numeric visual scores and identify what remains unverified.

For each significant strength or weakness, provide its impact, **preserve/refine/simplify/remove/replace/introduce** disposition, and concrete next action. Prioritize by severity and expected project value. Do not require a finding in every dimension.

## Optional Comparison Scores

Only when requested and matched rendered evidence exists, score iterations of the same project. Match content, viewport, state, capture conditions, and consequential interactions. If the user supplied no rubric, use Design 40%, Usability 30%, Creativity 20%, Content 10% as an internal comparison convention. Report technical acceptance separately and withhold a composite when core failures or material evidence gaps prevent a fair comparison.

Use whole numbers with criterion-specific reasons:

| Band | Meaning within that criterion |
| --- | --- |
| 1–2 | Fundamental failure or severe weakness |
| 3–4 | Partly works; substantial incoherence or unresolved defects |
| 5–6 | Competent baseline with clear limitations |
| 7–8 | Strong project fit and execution; identifiable refinements remain |
| 9–10 | Exceptional coherence and finish across inspected states; little material weakness observed |

These bands do not correspond to awards. Do not claim statistical precision or rank unrelated brands against one aesthetic. A single-site review can use qualitative assessments.

## Net Improvement

Compare the result with the baseline. Identify preserved strengths, the most consequential improvement, and the weakest remaining moment. Added complexity passes only when it improves the intended experience enough to justify its cost. For expressive work, revisit what someone will remember five minutes later; for quiet work, judge whether restraint strengthens the intended outcome.
