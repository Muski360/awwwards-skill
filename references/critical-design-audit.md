# Critical Design Audit

Use for an existing-site audit or a substantial redesign. Follow the context profile in [SKILL.md](../SKILL.md); collect evidence before choosing changes. A greenfield brief needs an assessment of content, assets, and feasibility, not a fictional baseline.

## Inspect the Experience

Capture relevant routes, states, and desktop/mobile views when possible. Inspect source and assets when rendering is unavailable, and label visual or runtime conclusions as unverified. Protect successful decisions before proposing replacements.

| Area | Inspect together |
| --- | --- |
| Identity and first impression | Intended feeling, first viewport, dominant subject, visual thesis, typography, originality, and coherent use of brand assets |
| Hierarchy and pacing | Reading path, density, spacing, scale, crops, section rhythm, and relationships between text and media |
| Content | Real copy, evidence, labels, actions, repetition, and what the visitor needs next |
| Interaction | Navigation, feedback, motion, transitions, scroll, cursor, touch, keyboard, and recovery |
| Responsive art direction | Small and intermediate compositions, portrait/landscape, reading order, long text, and changes in input |
| Implementation | Semantics, accessibility, loading, rendering cost, dependencies, lifecycle, browser support, and resilience |

Record material findings with evidence, impact, disposition, and intended outcome. Use **preserve**, **refine**, **simplify**, **remove**, **replace**, or **introduce**. Do not manufacture findings to fill categories.

## Copy and Complexity

Treat copy as interface material: preserve the subject, action, constraint, and proof. Remove repeated claims and marketing filler; retain the project's voice. Check errors, labels, confirmations, and help text as well as headlines.

For a prominent treatment, identify what is lost if it disappears. Orientation, hierarchy, feedback, narrative, atmosphere, and identity can all be valuable. Question layers that compete, repeat a message, or impose an unrelated interaction burden. Simplify when the benefit is equivalent; preserve expressive detail when it improves the experience.

Use the signature experience pass in [SKILL.md](../SKILL.md) to investigate opportunities beyond defect removal.

## 404 and Exceptional States

First establish whether routing/not-found behavior exists and belongs to the task. A custom 404 may repay investment in portfolios, campaigns, editorial, entertainment, brand, or experimental sites. Judge its audience value, visual fit, performance, and maintenance cost; a bespoke treatment is optional.

When justified, extend the site's existing type, imagery, framing, illustration, spatial idea, or motion into the missing-page experience. Keep a plain explanation and an obvious link to useful content available immediately. Test a direct unknown URL, client navigation, refresh, keyboard recovery, and the host/framework's actual not-found response behavior; an `/error` demo alone does not verify routing.

Apply the same judgment to loading, empty, offline, error, and transitional states within scope. Preserve user input and offer a useful recovery action where relevant. Distinguish real progress from a decorative transition; avoid fabricated percentages, artificial waits, or animation that delays recovery.

## Prioritize and Re-Audit

Fix failures in core tasks, accessibility, content integrity, and loading resilience first. For other findings, compare expected benefit, severity, reach, and implementation risk. Keep accessibility and performance constraints active while developing visual identity and polish.

After edits, revisit the affected routes and states with comparable evidence. Confirm preserved strengths, a clearer content path, a stronger project identity, and usable reduced-capability paths. Refine or remove changes that do not improve the experience. Report uncertainty rather than awarding yourself a pass from source inspection alone.
