# Awwwards Skill

An [Agent Skill](https://agentskills.io/specification) for coding agents that art-direct distinctive brand-facing websites without generic visual SLOP.

The skill derives typography, composition, imagery, motion, and effects from project evidence. It keeps accessibility, responsive behavior, loading resilience, and performance inside the art-direction process.

This project is independent and has no affiliation with Awwwards. It uses public Awwwards evaluation categories as a review lens and does not predict or guarantee awards.

<img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

## Install

Keep the `awwwards-skill` folder intact and place it in a skill directory supported by your agent. The folder name must continue to match `name: awwwards-skill` in `SKILL.md`.

| Environment | Skill directory |
|---|---|
| [Codex](https://learn.chatgpt.com/docs/build-skills) | Project `.agents/skills/awwwards-skill` or user `~/.agents/skills/awwwards-skill` |
| [Claude Code](https://code.claude.com/docs/en/skills) | Project `.claude/skills/awwwards-skill` or personal `~/.claude/skills/awwwards-skill` |
| [Gemini CLI](https://geminicli.com/docs/cli/using-agent-skills/) | `.gemini/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [Cursor](https://cursor.com/docs/skills) | `.cursor/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [GitHub Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) | `.github/skills/awwwards-skill`, `.claude/skills/awwwards-skill`, or `.agents/skills/awwwards-skill` |
| [Windsurf / Cascade](https://docs.windsurf.com/windsurf/cascade/skills) | `.windsurf/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |
| [Cline](https://docs.cline.bot/customization/skills) | `.cline/skills/awwwards-skill` or project `.claude/skills/awwwards-skill` |
| [Roo Code](https://docs.roocode.com/features/skills) | `.roo/skills/awwwards-skill` or `.agents/skills/awwwards-skill` |

Several agents recognize `.agents/skills`, so one checked-in copy can serve a mixed-tool team. Claude Code needs its `.claude/skills` path.

For [claude.ai custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills), upload the complete folder as a ZIP. Project Knowledge can act as a manual fallback, but it does not provide automatic skill discovery. In any environment without native Agent Skills support, supply `SKILL.md` as task instructions and keep `references/` available for the routing links.

Do not duplicate the skill body into `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, or editor rule files. Those files load under different rules and would create competing copies. `agents/openai.yaml` contains optional OpenAI/ChatGPT interface metadata; other clients can ignore it.

## Invoke

Codex:

```text
Use $awwwards-skill to redesign this landing page around a project-specific visual thesis.
```

Claude Code:

```text
/awwwards-skill audit this portfolio's art direction and do not edit files.
```

Automatic invocation also works when a request matches the skill description:

```text
Turn this conventional campaign site into a distinctive editorial experience, then verify the responsive and reduced-motion states.
```

## What the Skill Does

- separates build, concept, narrow-change, and read-only audit modes
- creates a compact direction brief from brand, content, audience, assets, and constraints
- detects transferable visual treatments and reformulates them around project evidence
- treats motion, WebGL, 3D, and heavy media as justified progressive enhancements
- verifies the static core, accessibility, responsive behavior, failure states, and available project checks

The skill rejects blind imitation of awarded websites. It extracts mechanisms such as pacing, crop, type scale, scene transitions, or interaction rhythm and rebuilds them from the current project.

## Structure

```text
awwwards-skill/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── evaluation-framework.md
│   ├── examples.md
│   ├── motion-and-implementation.md
│   ├── slop-patterns.md
│   └── visual-identity.md
└── README.md
```

`SKILL.md` owns mode selection, the direction brief, hard requirements, reference routing, and delivery. Each reference owns one conditional topic:

- [`visual-identity.md`](references/visual-identity.md): derive a project-specific visual system
- [`slop-patterns.md`](references/slop-patterns.md): diagnose generic treatments and choose reformulations
- [`motion-and-implementation.md`](references/motion-and-implementation.md): choose and verify motion, media, WebGL, and 3D
- [`evaluation-framework.md`](references/evaluation-framework.md): run evidence-based audits or compare iterations
- [`examples.md`](references/examples.md): study reformulation patterns when a concept remains generic

Browser automation, Lighthouse, image generation, Motion for React, GSAP, Three.js, and React Three Fiber are conditional capabilities, not skill dependencies. When a tool is unavailable, the skill requires agents to report the gap instead of inventing verification.

## Examples

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
