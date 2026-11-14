# Awwwards Skill

An [Agent Skill](https://agentskills.io/specification) for auditing, art-directing, building, and redesigning distinctive websites. It works from the project's audience, content, assets, and constraints to develop a coherent visual and interaction system.

For visually ambitious work, research informs the direction before implementation. Compare approaches grounded in the project's context, then develop composition, typography, media, and behavior across the whole journey. Expressive motion, 3D, unusual navigation, and quiet compositions remain available when they serve the project. Accessibility, responsive composition, performance, and finish are part of art direction.

Independent project; not affiliated with Awwwards and does not predict or guarantee awards.

<img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

## Install

Claude Code and Codex are the primary targets. Keep the `awwwards-skill` folder intact, including `SKILL.md`, `references/`, and `agents/`.

| Environment | Project directory |
| --- | --- |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/awwwards-skill` |
| [Codex](https://learn.chatgpt.com/docs/build-skills) | `.agents/skills/awwwards-skill` |

Claude Code also supports `~/.claude/skills/awwwards-skill`; Codex supports `~/.agents/skills/awwwards-skill`.

### Other clients

The skill uses the shared Agent Skills format. Other clients have their own discovery and tool behavior; consult their documentation for supported locations:

| Environment | Project directory |
| --- | --- |
| [Gemini CLI](https://geminicli.com/docs/cli/using-agent-skills/) | `.gemini/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [GitHub Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) | `.github/skills/awwwards-skill`, `.claude/skills/awwwards-skill`, or `.agents/skills/awwwards-skill` |
| [Windsurf / Cascade](https://docs.windsurf.com/windsurf/cascade/skills) | `.windsurf/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [Cline](https://docs.cline.bot/customization/skills) | `.cline/skills/awwwards-skill` or `.claude/skills/awwwards-skill` |
| [Roo Code](https://roocodeinc.github.io/Roo-Code/features/skills/) | `.roo/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |

Follow the linked client documentation for personal/global locations.

For clients without native skill support, supply `SKILL.md` as task instructions and make its reference files available. Avoid duplicating the body into agent rule files. `agents/openai.yaml` provides optional OpenAI interface metadata; it does not require an MCP server.

## Get Better Results

Supply real copy, brand assets, fonts and usage information, photography, and relevant video or 3D files. Add screenshots or recordings of desired interactions, reference websites, project goals, intended feeling, must-keep/must-avoid decisions, and technical constraints such as browsers, devices, stack, and performance budget.

Explain what interests you in a reference: its pacing, type, framing, transitions, or interaction. The skill inspects that material and reinterprets its mechanisms through your project's identity. It preserves strong existing work and labels missing evidence.

For visually ambitious work, it researches relevant sources before settling on a direction: supplied references, the curated GitHub catalog, and external sources such as Awwwards, Codrops, open-source experiments, and the project's own field. It compares different ways to express the project's purpose and adapts useful concepts and techniques. Curated sources are starting points, with no preferred aesthetic or default dependency. Narrow changes use research only when a concrete uncertainty warrants it; unavailable tools and evidence gaps are reported.

## Invoke

In Codex, use `$awwwards-skill`. In Claude Code, use `/awwwards-skill`. Clients that support automatic selection can match a request to the skill description.

**Build or redesign**

```text
Use $awwwards-skill to redesign this studio site for prospective clients using the supplied copy, fonts, and photography. Preserve the booking flow, implement the direction, and verify responsive behavior.
```

**Visual audit**

```text
Use $awwwards-skill to audit this site without editing files. Inspect its first viewport, full reading path, interactions, and mobile composition. Prioritize findings with evidence and concrete alternatives.
```

**Transform a generic site**

```text
Use $awwwards-skill to turn this template-like product site into an experience grounded in our actual product and audience. Keep verified claims and working flows; implement and verify the strongest changes.
```

**Ambitious portfolio or campaign**

```text
Use $awwwards-skill to build a memorable portfolio from these portraits, films, fonts, and reference recordings. Research relevant work, compare directions grounded in this body of work, and implement a coherent journey across projects, navigation, and mobile layouts. Verify the result within the requested scope.
```

## What's Included

[SKILL.md](SKILL.md) handles scope, context, direction, implementation, and verification. Specialist guidance loads at the relevant decision:

| Reference | Use |
| --- | --- |
| [Visual identity](references/visual-identity.md) | Inspect assets and references; compare and develop directions. |
| [External research](references/external-references.md) | Find, inspect, and adapt relevant work; decide when evidence is sufficient. |
| [Reference catalog](references/reference-catalog.md) | Select relevant GitHub starting points and investigate their techniques. |
| [Critical design audit](references/critical-design-audit.md) | Preserve strengths and prioritize changes in an existing experience. |
| [SLOP patterns](references/slop-patterns.md) | Diagnose generic decisions without banning visual ingredients. |
| [Motion and implementation](references/motion-and-implementation.md) | Choose mechanisms and handle input, media, lifecycle, and failure. |
| [Evaluation framework](references/evaluation-framework.md) | Review quality and technical acceptance with evidence. |
| [Reformulation examples](references/examples.md) | Follow contextual reasoning when a concept remains generic. |

Browser automation, Lighthouse, image generation, and animation/3D libraries are conditional capabilities. Agents report unavailable tools and unverified results.

## Audit and Evaluation

See the [evolution record](evals/evolution.md) for the audit, before/after instruction changes, conceptual trials, executed checks, and limitations. Conceptual trials assess the directions proposed by agents; they do not establish the visual quality of implemented websites or guarantee diversity across future projects.

## Author

[Muski360](https://github.com/Muski360)

## Acknowledgements

The compact structure, pattern catalog, and transformation examples take inspiration from [Stop Slop](https://github.com/hardikpandya/stop-slop) by [Hardik Pandya](https://hvpandya.com).
