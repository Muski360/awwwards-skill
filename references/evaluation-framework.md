# Evaluation Framework

Use this framework for visual audits, concept comparisons, and requested scoring. Default to an evidence-backed qualitative review. Do not predict an award or present this review as an official Awwwards score.

## Awwwards-Informed Lens

Official site listings publish Design, Usability, Creativity, and Content scores plus a separate development review. The listing calculations are consistent with the internal comparison weights below; Awwwards does not present this table as a general-purpose rubric.

| Criterion | Comparison weight | Review focus |
|---|---:|---|
| Design | 40% | Art direction, composition, typography, color, imagery, detail, and system coherence |
| Usability | 30% | Orientation, navigation, readability, feedback, control, and task completion |
| Creativity | 20% | Original concept, project-specific expression, and meaningful interaction |
| Content | 10% | Relevance, hierarchy, clarity, media quality, and narrative structure |

Current listings also expose development categories for Semantics/SEO, Animations/Transitions, Accessibility, WPO, Responsive Design, and Markup/Meta-data. Treat these concerns as connected. A visual concept loses value when users cannot read, navigate, control, or load it.

## Hard Gates

- **Identity:** The result expresses a project-specific visual thesis and recognizable identity anchors.
- **Transferability:** Prominent treatments fail to transfer unchanged to an unrelated brand.
- **Accessibility and usability:** Core content and tasks have semantic structure, accessible names, roles, and states, logical focus, visible and unobscured focus, sufficient contrast, readable zoom/reflow, reduced-motion handling, and non-hover input paths.
- **Performance and resilience:** Heavy media and effects have loading, failure, and reduced-capability paths; core content remains usable without them.
- **Content integrity:** Claims, logos, metrics, awards, testimonials, and product behavior come from verified sources or carry clear placeholder labels.

Block the review when a core route or task fails, a core control is inaccessible, evidence is fabricated, or an effect removes the only usable content path. Record other gate failures as high-priority findings rather than hiding them inside a weighted average.

## Evidence Rules

- Capture desktop and mobile views plus key interactions when browser tools are available.
- Without rendered evidence, inspect source and assets, state the limitation, and avoid a numeric visual score.
- Distinguish an observed failure from a plausible risk. Cite the route, viewport, state, element, or code that supports each finding.
- Treat automated accessibility and Lighthouse results as partial evidence, not proof of overall quality.

## Review Method

1. State the inferred direction brief and the evidence that supports it.
2. Run the hard gates before discussing polish.
3. Review each criterion with a concrete strength, weakness, and highest-value change.
4. Prioritize the change that improves the weakest high-weight criterion without breaking a gate or erasing identity.
5. If the user asks to compare iterations of the same project and matched rendered evidence exists, score each criterion from 1 to 10 and apply the weights. Match content, viewport, state, and capture conditions; include equivalent interaction states when they affect the comparison.

For optional numeric scoring, use these anchors:

- **1:** the criterion fails or blocks the experience
- **5:** the criterion works but remains generic, inconsistent, or incomplete
- **10:** the evidence shows an exceptional, coherent result with no material weakness in that criterion

Use weighted scores only to compare iterations of the same project. For a single site or unrelated projects, give qualitative criterion assessments without a composite number. Do not rank unrelated brands through one aesthetic standard or imply precision that the evidence cannot support.

## Primary References

- [Awwwards Site of the Day scoring example](https://www.awwwards.com/sites/peden-munk)
- [W3C accessibility principles](https://www.w3.org/WAI/fundamentals/accessibility-principles/)
- [W3C designing for web accessibility](https://www.w3.org/WAI/tips/designing/)
- [WCAG 2.2](https://www.w3.org/TR/wcag/)
