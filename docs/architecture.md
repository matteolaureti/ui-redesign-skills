# Skill architecture

## Why several small skills?

OpenAI's guidance describes skills as reusable workflows that can include a name, description, instructions and supporting resources. It also recommends smaller building blocks for complex workflows rather than one enormous end-to-end skill.

This repository therefore separates:

- universal redesign reasoning;
- product-specific reasoning;
- exploration behavior.

## Layers

### Layer 1 — Core

`ui-redesign-core`

Contains universal screenshot-redesign behavior.

### Layer 2 — Domain

Examples:

- `dashboard-redesign`
- `landing-page-redesign`
- `ios-app-redesign`
- `component-redesign`

These answer a different question:

> What does excellent redesign mean for this particular product surface?

### Layer 3 — Exploration

`design-direction-explorer`

Controls diversity when several concepts are requested.

It does not replace the domain skill. It changes how the design space is explored.

## No fake dependency mechanism

The repository does not invent an `import`, `extends`, or dependency syntax for `SKILL.md`.

Skills are written to be composable when a host supports multiple skills, but each specialized skill also carries its critical output guardrails so that it remains useful independently.

## Information hierarchy

A redesign workflow should generally reason in this order:

1. product purpose;
2. primary user task;
3. required information/actions;
4. information hierarchy;
5. global composition;
6. density;
7. typography;
8. component language;
9. palette and surfaces;
10. polish;
11. final quality checks.

## Output invariant

The most important repository-wide invariant is:

> ONE OUTPUT IMAGE = ONE REDESIGN.

Multiple concepts are multiple outputs, not multiple miniature interfaces inside one canvas.
