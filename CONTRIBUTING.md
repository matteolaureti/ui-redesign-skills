# Contributing

Contributions are welcome.

The goal of this repository is to build reusable, specialized UI-redesign skills rather than a collection of aesthetic presets.

## Good contributions

A useful new skill should represent a distinct design problem, product surface or workflow, for example:

- Android app redesign;
- e-commerce redesign;
- dense admin/data interface redesign;
- onboarding and form redesign;
- settings and billing redesign;
- accessibility-focused redesign.

A style such as “glass dashboard”, “blue dashboard” or “minimal dashboard” usually should **not** become its own skill. Those are visual directions, not reusable product-design domains.

## Skill structure

Each skill should normally contain a `SKILL.md` with:

1. clear name and description;
2. job-to-be-done;
3. expected inputs;
4. a step-by-step workflow;
5. domain-specific rules;
6. output requirements;
7. final quality checks.

Keep skills focused and composable.

## Required guardrail

Any skill that can generate multiple redesign concepts must preserve this rule:

> **One output image = one redesign.**

If the user requests multiple concepts, they should be produced as separate output images unless the user explicitly asks for a contact sheet or comparison board.

## Pull requests

When proposing a new skill:

- explain what design problem it solves;
- explain why the problem is not already covered by another skill;
- include realistic usage examples;
- avoid duplicating the entire core skill;
- keep model-specific assumptions to a minimum unless the skill explicitly targets a model capability.
