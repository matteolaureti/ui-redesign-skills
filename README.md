# UI Redesign Skill for GPT Image

[![skills.sh compatible](https://img.shields.io/badge/skills.sh-compatible-111111)](https://skills.sh)

A modular Agent Skill for redesigning existing user interfaces from screenshots with image generation. It uses one precise trigger, a lean router, a strong universal design brain, and domain-specific references loaded only when needed.

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
- requested alternatives reuse the same structure or visual style.

`redesign-ui` gives the agent concrete product-design judgment without forcing every task through one enormous universal prompt.

## Architecture

The skill uses a layered guidance model.

### 1. Universal design brain

Every redesign loads:

```text
references/design-principles.md
```

This contains the shared art direction for typography, hierarchy, layout, surfaces, components, realism, branding, accessibility, and anti-AI-slop review.

### 2. Conditional domain guidance

The router then loads only the references relevant to the task:

- dashboard screenshot → `dashboard.md`;
- landing page → `landing-page.md`;
- iPhone/iPad UI → `ios-app.md`;
- isolated component → `component.md`;
- strong visual rethink → `visual-directions.md`;
- multiple directions → `multiple-directions.md` + `visual-directions.md`.

This preserves strong design guidance without filling context with unrelated domain instructions.

## Repository structure

```text
ui-redesign-skills/
├── README.md
├── INSTALL.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── architecture.md
│   ├── references.md
│   └── testing.md
├── examples/
│   └── prompts.md
└── skills/
    └── redesign-ui/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── design-principles.md
            ├── dashboard.md
            ├── landing-page.md
            ├── ios-app.md
            ├── component.md
            ├── visual-directions.md
            └── multiple-directions.md
```

## What triggers the skill

Use `redesign-ui` when the task is a **visual redesign image** based on one or more existing UI screenshots, including dashboards, web apps, landing pages, iOS screens, or individual components.

It is deliberately not intended for:

- implementing a UI in code;
- pixel-perfect screenshot cloning;
- generic image editing unrelated to interface redesign.

That narrow trigger helps prevent the image-design skill from interfering with ordinary frontend coding work.

## Example

Attach a dashboard screenshot and ask:

> Use $redesign-ui to completely redesign this dashboard. Preserve its purpose and important functionality, but rethink the hierarchy, layout, navigation, density and component structure. Create 4 genuinely different directions as 4 separate output images.

The skill loads the universal design principles, dashboard guidance, multiple-directions guidance, and visual-direction exploration.

Expected output:

```text
Image 1 → redesign A
Image 2 → redesign B
Image 3 → redesign C
Image 4 → redesign D
```

The directions should differ in both structure and art direction where appropriate — not merely rearrange the same palette, typography, surfaces, and visual mood.

Never one image containing A + B + C + D unless a comparison board is explicitly requested.

## Testing

The repository includes a test plan covering explicit invocation, implicit discovery, domain routing, multiple directions, component scope control, and a negative coding-trigger test.

See [docs/testing.md](docs/testing.md).

## Design philosophy

The skill does not prescribe one aesthetic. It prioritizes product purpose, important information and actions, hierarchy, layout, density, typography, component language, and then visual polish.

The universal design brain is intentionally opinionated about recurring generated-UI problems such as generic card grids, unnecessary pills, purple-blue AI gradients, decorative analytics, excessive glass, weak typography, and layouts that prioritize presentation over actual product use.

For strong or multi-direction redesigns, the skill also treats the current screenshot's palette, typography, surfaces, imagery strategy, and visual mood as redesignable implementation choices rather than automatic constraints. Brand identity can be preserved without cloning the current visual system.

At the same time, the router and domain references leave the model room to make context-sensitive design decisions rather than forcing every product through the same layout recipe.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## References

The architecture follows current OpenAI skill guidance and GPT-6 Astra prompting guidance. See [docs/references.md](docs/references.md).

## License

MIT.
