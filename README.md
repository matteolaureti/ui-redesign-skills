# UI Redesign Skill for GPT Image

[![skills.sh compatible](https://img.shields.io/badge/skills.sh-compatible-111111)](https://skills.sh)

A modular Agent Skill for redesigning existing user interfaces from screenshots with image generation. It is structured for current GPT-6 Astra / Codex skill guidance: one precise trigger, a lean `SKILL.md`, and domain-specific references loaded only when needed.

> **One output image = one complete redesign.**

## Install

Install with skills.sh:

```bash
npx skills add matteolaureti/ui-redesign-skills
```

This installs the `redesign-ui` skill.

To pull a newer version later:

```bash
npx skills update
```

## Why this exists

Screenshot-based UI redesign often fails in predictable ways:

- the result is only a recolor of the original;
- multiple concepts are packed into one image;
- important functionality disappears for aesthetics;
- dashboards become generic AI/Dribbble concepts;
- mobile apps look like narrow websites;
- requested alternatives reuse the same structure.

`redesign-ui` gives the agent product-design guidance without forcing every task through a large universal prompt.

## Why one skill instead of several competing skills?

GPT-6 Astra is especially sensitive to instructions in skills and other files. OpenAI's current guidance recommends keeping skill descriptions precise and using progressive disclosure for skills with multiple workflows.

Instead of requiring the agent to discover and combine `core + category + explorer`, this repository exposes one clear skill trigger and routes internally to the relevant reference only after the skill is selected.

For example:

- dashboard screenshot → load `dashboard.md`;
- landing page → load `landing-page.md`;
- iPhone/iPad UI → load `ios-app.md`;
- isolated component → load `component.md`;
- multiple directions → additionally load `multiple-directions.md`.

Irrelevant references stay out of context.

## Repository structure

```text
ui-redesign-skills/
├── README.md
├── INSTALL.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── architecture.md
│   └── references.md
├── examples/
│   └── prompts.md
└── skills/
    └── redesign-ui/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── dashboard.md
            ├── landing-page.md
            ├── ios-app.md
            ├── component.md
            └── multiple-directions.md
```

## What triggers the skill

Use `redesign-ui` when the user wants a **visual redesign image** from one or more existing UI screenshots, including dashboards, web apps, landing pages, iOS screens, or individual components.

It is deliberately not intended for:

- implementing a UI in code;
- pixel-perfect screenshot cloning;
- generic image editing unrelated to interface redesign.

That narrow trigger helps prevent the skill from interfering with ordinary coding work in Codex.

## Example

Attach a dashboard screenshot and ask:

> Use $redesign-ui to completely redesign this dashboard. Preserve its purpose and important functionality, but rethink the hierarchy, layout, navigation, density and component structure. Create 4 genuinely different directions as 4 separate output images.

The router loads dashboard guidance plus the multiple-directions reference.

Expected output:

```text
Image 1 → redesign A
Image 2 → redesign B
Image 3 → redesign C
Image 4 → redesign D
```

Never one image containing A + B + C + D unless the user explicitly requests a comparison board.

## Design philosophy

The skill does not prescribe one aesthetic. It prioritizes product purpose, important information and actions, hierarchy, layout, density, typography, component language, and then visual polish.

It also leaves Astra room to make context-sensitive design decisions rather than forcing it through an elaborate step-by-step recipe.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## References

The architecture follows current OpenAI skill guidance and GPT-6 Astra prompting guidance. See [docs/references.md](docs/references.md).

## License

MIT.
