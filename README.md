# UI Redesign Skills for GPT Image

[![skills.sh compatible](https://img.shields.io/badge/skills.sh-compatible-111111)](https://skills.sh)

A composable set of Agent Skills for redesigning existing user interfaces from screenshots with GPT Image / ChatGPT Images.

> **One output image = one complete redesign.**

If you ask for eight redesigns, the intended result is eight separate images — never one contact sheet containing eight tiny concepts.

## Recommended install

Install the **complete collection** with skills.sh:

```bash
npx skills add matteolaureti/ui-redesign-skills
```

**This is the recommended setup for most users.** The collection is designed to work as a system: `ui-redesign-core` provides the common redesign foundation, while the more specific skills add domain-specific guidance for dashboards, landing pages, iOS apps, components, and multi-direction exploration.

Once the collection is installed, the agent can use the appropriate skills for the task instead of requiring you to install modules one by one.

### Advanced: install a single skill

Only do this if you intentionally want a partial installation:

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill ui-redesign-core
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill dashboard-redesign
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill landing-page-redesign
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill ios-app-redesign
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill component-redesign
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill design-direction-explorer
```

See [INSTALL.md](INSTALL.md) for recommended combinations and update instructions.

## Why this exists

Screenshot-based UI redesign often fails in predictable ways:

- the result is only a recolor of the original;
- multiple concepts are packed into one image;
- important functionality disappears for aesthetic reasons;
- every surface becomes a rounded card;
- dashboards become generic Dribbble-style SaaS mockups;
- mobile apps look like responsive websites;
- different requested concepts are almost identical.

These skills turn screenshot redesign into a repeatable workflow with explicit product-design reasoning and quality checks.

## Skills

| Skill | Purpose |
|---|---|
| `ui-redesign-core` | Foundation for screenshot analysis, hierarchy, layout, typography, surfaces, brand handling, accessibility and anti-AI-slop rules. |
| `dashboard-redesign` | SaaS dashboards, admin panels, analytics interfaces and operational workspaces. |
| `landing-page-redesign` | Product landing pages, SaaS marketing sites and conversion-focused web experiences. |
| `ios-app-redesign` | Native-feeling iPhone and iPad redesigns with platform-aware navigation and layout. |
| `component-redesign` | Redesigns one card, section, table, modal, FAQ, pricing block or localized UI component. |
| `design-direction-explorer` | Produces several genuinely different redesign directions while keeping one concept per image. |

## How the collection composes

The full collection is the recommended installation. Conceptually, tasks usually combine the core skill with the relevant specialization:

```text
Dashboard
ui-redesign-core + dashboard-redesign

Landing page
ui-redesign-core + landing-page-redesign

iOS app
ui-redesign-core + ios-app-redesign

Single component
ui-redesign-core + component-redesign

Multiple dashboard directions
ui-redesign-core + dashboard-redesign + design-direction-explorer
```

There is no invented dependency or `import` syntax between the skills. Each specialized skill carries the critical guardrails it needs to remain useful independently, while the collection is designed to give the agent the complete set of tools to choose from.

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

## Example

Input:

> Redesign the attached dashboard. Keep the same product functionality, but rethink the visual hierarchy and layout. Generate 8 different directions.

The intended skill combination is:

```text
ui-redesign-core
dashboard-redesign
design-direction-explorer
```

Expected output behavior:

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

The repository is intentionally model-light rather than tightly coupled to one version, so the skills can evolve with image-generation capabilities.

## Updating

Pull newer versions of installed skills with:

```bash
npx skills update
```

## Design philosophy

These skills do not prescribe one aesthetic. They are intended to improve **product-design reasoning**, not turn every interface into the same fashionable style.

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

Useful additions could include skills for Android, e-commerce, data-heavy admin interfaces, onboarding and forms, settings and billing, brand-led redesign, and accessibility-focused redesign.

## References

See [docs/references.md](docs/references.md).

## License

MIT.
