# Awwwards Skill

An art direction skill for AI coding agents that build distinctive, high-impact web experiences without generic visual SLOP.

<img width="2170" height="725" alt="Awwwards Skill banner" src="https://github.com/user-attachments/assets/52fe72d6-cb6b-43ca-8b99-a22e9e1484fd" />

## What This Is

AI-generated interfaces repeat patterns: purple gradients, glass cards, oversized headlines, pill-shaped controls, floating 3D objects, and animation stacks with no connection to the brand.

Awwwards Skill teaches an AI coding agent to detect those patterns, remove weak treatments, and build a visual system from the project’s content, audience, materials, and goals.

The skill focuses on:

- project-specific visual identity
- editorial composition and typography
- purposeful motion and interaction
- responsive and accessible implementation
- performance-aware effects, media, and 3D
- evidence-based visual review

This project is independent and has no affiliation with Awwwards. It uses public Awwwards evaluation categories as a review lens and does not predict or guarantee awards.

## Skill Structure

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

`SKILL.md` contains the core workflow and mandatory rules. The reference files provide detailed guidance when the agent needs to make or review a specific design decision.

## Quick Start

### Codex

Copy the `awwwards-skill` folder into your Codex skills directory:

```text
$CODEX_HOME/skills/awwwards-skill
```

Invoke it in a request:

```text
Use $awwwards-skill to redesign this landing page around a distinct visual thesis.
```

### Claude

Add the folder as a skill in a Claude environment that supports skills. For Claude Projects or environments without skill discovery, upload `SKILL.md` and the `references/` directory as project knowledge.

The `agents/openai.yaml` file supplies Codex interface metadata. Claude and other agents can ignore it.

### Other Agentic Systems

Load `SKILL.md` as system or project instructions and keep the `references/` files available through the agent’s file or retrieval tools.

The agent needs access to the target codebase. Browser automation, Lighthouse, GSAP, Framer Motion, Three.js, and React Three Fiber remain conditional capabilities, not required dependencies.

## Example Prompts

```text
Use $awwwards-skill to turn this conventional portfolio into a distinct editorial experience.
```

```text
Audit this landing page for visual SLOP, then reformulate every high-severity pattern.
```

```text
Create a visual thesis, identity anchors, and motion grammar before changing the frontend.
```

```text
Review this implementation for art direction, usability, accessibility, responsive behavior, and performance.
```

## What It Rejects

The skill treats a fashionable visual device as SLOP when it lacks a relationship to the brand, content, or interaction.

| SLOP pattern | Why it fails | Reformulation |
|---|---|---|
| Unmotivated gradient | Color fills empty space without brand evidence | Derive color from material, imagery, state, data, or a defined light source |
| Missing visual identity | Safe typography and stock components fit unrelated brands | Define a visual thesis and two or three identity anchors |
| Default card grid | Equal containers flatten hierarchy | Use editorial grouping, media, dividers, lists, or spatial hierarchy |
| Glassmorphism by default | Blur decorates routine content | Use transparency only when layers or material logic require it |
| Decorative 3D | Rendering cost adds spectacle without meaning | Model a product form, process, data relationship, or brand artifact |
| Effect stack | Glow, grain, parallax, cursor effects, and marquees compete | Choose one signature motif and one supporting motion behavior |
| Template typography | A giant neutral headline acts as the full concept | Build a type voice through width, rhythm, crop, spacing, and imagery |
| Generic copy | Vague claims could describe any company | Name the product, audience, action, constraint, or result |

See [`references/slop-patterns.md`](references/slop-patterns.md) for the full catalog.

## Workflow

1. Inspect the project, content, assets, stack, and constraints.
2. Write a creative brief with a visual thesis, identity anchors, emotional target, content spine, interaction thesis, and technical budget.
3. Build the typography, color, composition, imagery, material, and motion systems from project evidence.
4. Compose the page around a clear narrative instead of a component inventory.
5. Implement the semantic and responsive core before complex effects.
6. Add motion or 3D only when it serves hierarchy, feedback, continuity, or product understanding.
7. Run the SLOP audit and reformulate transferable treatments.
8. Verify accessibility, responsive behavior, loading, performance, and project checks.

## Reference Guides

- [`visual-identity.md`](references/visual-identity.md): derive a visual system from brand and project evidence.
- [`slop-patterns.md`](references/slop-patterns.md): identify generic visual treatments and reformulate them.
- [`examples.md`](references/examples.md): study eight SLOP-to-distinctive transformations.
- [`motion-and-implementation.md`](references/motion-and-implementation.md): choose CSS, GSAP, Framer Motion, Three.js, or React Three Fiber based on need.
- [`evaluation-framework.md`](references/evaluation-framework.md): review design, usability, creativity, content, accessibility, and implementation quality.

## Evaluation

The review framework uses the categories displayed on official Awwwards site listings:

| Criterion | Weight |
|---|---:|
| Design | 40% |
| Usability | 30% |
| Creativity | 20% |
| Content | 10% |

The skill adds identity, SLOP, accessibility, performance, and content gates. A broken core route or inaccessible interaction blocks the review even when the visual score looks strong.

Use the weighted result to compare iterations of the same project. Do not present it as an official Awwwards score.

## Design Principle

A treatment earns its place when it reinforces a brand idea, improves hierarchy or interaction, and justifies its technical cost. Remove it when it does none of those jobs.

## Author

[Muski360](https://github.com/Muski360)

## Acknowledgements

The concise repository structure, explicit pattern catalog, and transformation examples take inspiration from [Stop Slop](https://github.com/hardikpandya/stop-slop) by [Hardik Pandya](https://hvpandya.com).
