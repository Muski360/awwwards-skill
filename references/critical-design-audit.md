# Critical Design Audit

Use for an existing-site audit or a substantial redesign. Establish context through [SKILL.md](../SKILL.md); collect evidence before choosing changes. A greenfield brief needs an assessment of content, assets, and feasibility, not a fictional baseline.

## Inspect the Experience

Capture relevant routes, states, and desktop/mobile views when possible. Inspect source and assets when rendering is unavailable, and label visual or runtime conclusions as unverified. Protect successful decisions before proposing replacements.

| Area | Inspect together |
| --- | --- |
| Identity | Intended feeling, visual thesis, typography, originality, and coherent use of brand assets across the opening and subsequent experience |
| Hierarchy and pacing | Reading path, density, spacing, scale, crops, section rhythm, and relationships between text and media |
| Content | Real copy, evidence, labels, actions, repetition, and what the visitor needs next |
| Interaction | Navigation, feedback, motion, transitions, scroll, cursor, touch, keyboard, and recovery |
| Responsive art direction | Small and intermediate compositions, portrait/landscape, reading order, long text, and changes in input |
| Implementation | Semantics, accessibility, loading, rendering cost, dependencies, lifecycle, browser support, and resilience |

Record material findings with an evidence location, impact, disposition, and intended outcome. Use **preserve**, **refine**, **simplify**, **remove**, **replace**, or **introduce**. Do not manufacture findings to fill categories. Distinguish observed failures from inferred risks; use the [evaluation framework](evaluation-framework.md#evidence-and-comparison) for evidence limits and comparisons.

## Copy and Complexity

Treat copy as interface material: preserve the subject, action, constraint, and proof. Remove repeated claims and marketing filler; retain the project's voice. Check errors, labels, confirmations, and help text as well as headlines.

Mentally remove eyebrows, subtitles, and mini-headings. Remove a redundant label when heading, content, and navigation retain the same hierarchy and context; do not replace it with another decorative phrase. Keep useful context, labels beneath expressive headings, and navigable chapter names. Inspect repeated section-intro patterns, preserving meaningful headings and accessible names.

For a prominent treatment, identify what is lost if it disappears. Orientation, hierarchy, feedback, narrative, atmosphere, and identity can all be valuable. Question layers that compete, repeat a message, or impose an unrelated interaction burden. Simplify when the benefit is equivalent; preserve expressive detail when it improves the experience.

For opportunities beyond defect removal, use the direction workflow in [SKILL.md](../SKILL.md).

## 404 and Exceptional States

First establish whether routing/not-found behavior exists and belongs to the task. A custom 404 may repay investment in portfolios, campaigns, editorial, entertainment, brand, or experimental sites. Judge its audience value, visual fit, performance, and maintenance cost; a bespoke treatment is optional.

When justified, extend the site's existing type, imagery, framing, illustration, spatial idea, or motion into the missing-page experience. Keep a plain explanation and an obvious link to useful content available immediately. Test a direct unknown URL, client navigation, refresh, keyboard recovery, and the host/framework's actual not-found response behavior; an `/error` demo alone does not verify routing.

Apply the same judgment to loading, empty, offline, error, and transitional states within scope. Preserve user input and offer a useful recovery action where relevant. Distinguish real progress from a decorative transition; avoid fabricated percentages, artificial waits, or animation that delays recovery.

## Prioritize

Fix failures in core tasks, accessibility, content integrity, and loading resilience first. For other findings, compare expected benefit, severity, reach, and implementation risk. A weak expressive moment may matter greatly to a campaign and little to a utility page; set priority by project impact, not by a preferred aesthetic. Preserve successful decisions and expressive detail when they contribute value.

After authorized edits, revisit affected routes and states. Use [evaluation](evaluation-framework.md) for a finished review or before/after comparison; routine fixes need only checks relevant to the changed behavior.
