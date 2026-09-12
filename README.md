# UI Redesign Skills for GPT Image

A composable set of Agent Skills for redesigning existing user interfaces from screenshots with GPT Image / ChatGPT Images.

The repository is built around a simple rule:

> **One output image = one complete redesign.**

If you ask for eight redesigns, the intended result is **eight separate images**, never one contact sheet containing eight tiny concepts.

## Why this exists

Image models are already good at generating polished UI concepts, but screenshot redesign often fails in predictable ways:

- the result is only a recolor of the original;
- multiple concepts are packed into one image;
- important functionality disappears for aesthetic reasons;
- every surface becomes a rounded card;
- dashboards become generic Dribbble-style SaaS mockups;
- mobile apps look like responsive websites;
- different requested concepts are almost identical.

These skills turn screenshot redesign into a repeatable workflow with explicit product-design reasoning and quality checks.

## Structure

```text
ui-redesign-skills/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── architecture.md
│   └── references.md
├── examples/
│   └── prompts.md
└── skills/
    ├── ui-redesign-core/
    │   └── SKILL.md
    ├── dashboard-redesign/
    │   └── SKILL.md
    ├── landing-page-redesign/
    │   └── SKILL.md
    ├── ios-app-redesign/
    │   └── SKILL.md
    ├── component-redesign/
    │   └── SKILL.md
    └── design-direction-explorer/
        └── SKILL.md
```

## The skills

### `ui-redesign-core`

The foundation. Use it for almost any screenshot-based redesign.

It defines:

- screenshot analysis;
- preservation of product meaning;
- redesign intensity;
- hierarchy, typography, surfaces and layout;
- realistic UI rendering;
- anti-AI-slop rules;
- brand handling;
- accessibility-aware visual decisions;
- the mandatory one-image-one-redesign rule.

### `dashboard-redesign`

For SaaS dashboards, admin panels, operational tools and analytics interfaces.

Adds guidance for:

- information density;
- KPI hierarchy;
- tables and lists;
- filters;
- navigation;
- status and anomalies;
- activity feeds;
- operational actions;
- master-detail layouts;
- avoiding “a grid of cards with charts” as the default answer.

### `landing-page-redesign`

For marketing websites and product landing pages.

Adds guidance for:

- narrative and conversion hierarchy;
- hero sections;
- product demonstrations;
- social proof;
- pricing;
- trust;
- section rhythm;
- avoiding the standard AI SaaS-page sequence.

### `ios-app-redesign`

For iPhone and iPad UI redesign.

Adds guidance for:

- safe areas;
- adaptive layout;
- Dynamic Type;
- navigation stacks;
- toolbars;
- tab bars;
- sheets and modality;
- native-feeling controls;
- avoiding “desktop web UI squeezed into a phone”.

### `component-redesign`

For redesigning a single card, section, table, modal, FAQ, pricing block, navigation element or other isolated component.

It deliberately prevents the model from needlessly redesigning the entire surrounding product.

### `design-direction-explorer`

A companion skill for generating several genuinely different redesign directions.

It forces structural diversity across outputs while preserving:

> **one concept per image**

## Recommended composition

There is no assumed technical `import` mechanism between skills. Each skill is usable on its own.

For best results, combine the relevant skills conceptually:

```text
ui-redesign-core + dashboard-redesign
ui-redesign-core + landing-page-redesign
ui-redesign-core + ios-app-redesign
ui-redesign-core + component-redesign

ui-redesign-core + dashboard-redesign + design-direction-explorer
```

The domain skills repeat only the most important guardrails so they remain useful even when used independently.

## Example

Input:

> Redesign the attached dashboard. Keep the same product functionality, but rethink the visual hierarchy and layout. Generate 8 different directions.

Recommended skills:

```text
ui-redesign-core
dashboard-redesign
design-direction-explorer
```

Expected behavior:

```text
Image 1 → one complete redesign
Image 2 → one complete redesign
Image 3 → one complete redesign
...
Image 8 → one complete redesign
```

Not:

```text
One image → 8 miniature redesigns
```

## GPT Image

The skills are designed for reference-led image workflows: the attached UI screenshot acts as a functional and informational source, while the model is allowed to reinterpret the visual design according to the requested redesign intensity.

They are intentionally model-light rather than being tightly coupled to one version. They can be used with current GPT Image / ChatGPT Images workflows and adapted as image-generation capabilities evolve.

For high-fidelity editing, explicitly tell the model what must remain recognizable and what may change. For complete redesigns, preserve product meaning and important content while allowing the visual composition to be rebuilt.

## Installation

Use the `SKILL.md` file from the skill you want to install or provide it to a product that supports the Agent Skills format.

A practical starting point is:

1. install or load `ui-redesign-core`;
2. add one domain-specific skill;
3. add `design-direction-explorer` only when you want several distinct concepts.

## Design philosophy

These skills do not prescribe one aesthetic.

They are intended to improve **product-design reasoning**, not turn every interface into the same fashionable style.

The system prioritizes:

1. product purpose;
2. important information and actions;
3. information hierarchy;
4. layout;
5. density;
6. typography;
7. component language;
8. visual polish.

Color is not the first design decision.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

Useful additions could include skills for:

- Android;
- e-commerce;
- data-heavy admin interfaces;
- onboarding and forms;
- settings and billing;
- brand-led redesign;
- accessibility-focused redesign.

## References

See [docs/references.md](docs/references.md).

## License

MIT.
