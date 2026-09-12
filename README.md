# Awwwards Skill

An [Agent Skill](https://agentskills.io/specification) for auditing, art-directing, building, and redesigning distinctive websites. It works from the project's audience, content, assets, and constraints to develop a coherent visual and interaction system.

A signature experience pass investigates memorable first viewports and project-specific moments. Expressive typography, media, motion, 3D, cursors, and custom 404 pages are options; the project determines which belong. Accessibility, responsive composition, performance, and finish are part of the design process.

Independent project; not affiliated with Awwwards and does not predict or guarantee awards.

<img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

## Install

Keep the `awwwards-skill` folder intact, including `SKILL.md`, `references/`, and `agents/`. Place it in a supported skill directory:

| Environment | Project directory |
| --- | --- |
| [Codex](https://learn.chatgpt.com/docs/build-skills) | `.agents/skills/awwwards-skill` |
| [Claude Code](https://code.claude.com/docs/en/skills) | `.claude/skills/awwwards-skill` |
| [Gemini CLI](https://geminicli.com/docs/cli/using-agent-skills/) | `.gemini/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [GitHub Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) | `.github/skills/awwwards-skill`, `.claude/skills/awwwards-skill`, or `.agents/skills/awwwards-skill` |
| [Windsurf / Cascade](https://docs.windsurf.com/windsurf/cascade/skills) | `.windsurf/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [Cline](https://docs.cline.bot/customization/skills) | `.cline/skills/awwwards-skill` or `.claude/skills/awwwards-skill` |
| [Roo Code](https://roocodeinc.github.io/Roo-Code/features/skills/) | `.roo/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |

Codex also supports `~/.agents/skills/awwwards-skill`; Claude Code supports `~/.claude/skills/awwwards-skill`. Follow the linked client documentation for other personal/global locations.

For clients without native skill support, supply `SKILL.md` as task instructions and make its reference files available. Avoid duplicating the body into agent rule files. `agents/openai.yaml` provides optional OpenAI interface metadata; it does not require an MCP server.

## Get Better Results

Results improve substantially when you supply real copy, brand assets, fonts and usage information, photography, and relevant video or 3D files. Add screenshots or recordings of desired interactions, reference websites, project goals, intended feeling, must-keep/must-avoid decisions, and technical constraints such as browsers, devices, stack, and performance budget.

Explain what interests you in a reference: its pacing, type, framing, transitions, or interaction. The skill inspects that material and reinterprets its mechanisms through your project's identity. It preserves strong existing work and labels missing evidence.

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
Use $awwwards-skill to build a memorable portfolio from these portraits, films, fonts, and reference recordings. Reinterpret their framing and pacing, develop a signature opening and mobile composition, and consider a matching 404 where worthwhile.
```

## What's Included

[SKILL.md](SKILL.md) handles scope, context, the signature pass, implementation, and verification. Specialist guidance loads when needed:

- [Visual identity](references/visual-identity.md): assets, reference analysis, and art direction.
- [Critical design audit](references/critical-design-audit.md): preservation, changes, and exceptional states.
- [SLOP patterns](references/slop-patterns.md): diagnose generic treatments.
- [Motion and implementation](references/motion-and-implementation.md): native APIs, libraries, input, media, and lifecycle.
- [Evaluation framework](references/evaluation-framework.md): quality, technical acceptance, and optional comparisons.
- [Reformulation examples](references/examples.md): contextual mechanisms and alternatives.

Browser automation, Lighthouse, image generation, and animation/3D libraries are conditional capabilities. Agents report unavailable tools and unverified results.

## Examples

The Before/After images below are intentional repeated banner placeholders, not demonstrated results.

 - Before:
 <img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

 - After:
 <img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />


 - Before:
 <img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

 - After:
 <img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

## Author

[Muski360](https://github.com/Muski360)

## Acknowledgements

The compact structure, pattern catalog, and transformation examples take inspiration from [Stop Slop](https://github.com/hardikpandya/stop-slop) by [Hardik Pandya](https://hvpandya.com).
