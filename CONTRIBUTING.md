# Contributing

Contributions are welcome.

The repository is intentionally structured as one routed skill with progressively disclosed references. Prefer improving that structure over adding another installable skill.

## Before adding a new skill

Ask whether the new behavior has a genuinely different trigger from:

> visual redesign of an existing UI screenshot into image output

If it is only another UI surface, product category, or redesign mode, add a focused file under `skills/redesign-ui/references/` and route to it from `SKILL.md`.

Create a separate installable skill only when the task is meaningfully different and should trigger independently.

## Skill design principles

Follow current OpenAI skill guidance:

- keep the frontmatter description short and precise enough for reliable triggering;
- keep `SKILL.md` focused on essential workflow and routing;
- move variant-specific detail into one-level-deep `references/` files;
- do not duplicate the same instructions in the root and references;
- assume the model can reason about routine intermediate decisions;
- add constraints when they materially change the result, not as generic handholding;
- preserve explicit user instructions over default skill heuristics.

## Good reference additions

Useful additions could cover:

- Android applications;
- e-commerce/product pages;
- dense data/admin interfaces when dashboard guidance is insufficient;
- onboarding and forms;
- settings and billing;
- accessibility-specific redesign considerations.

A style such as “glass”, “blue”, “minimal”, or “dark” should normally remain a design direction rather than becoming its own reference or skill.

## Required output rule

Any contribution must preserve:

> **One output image = one redesign.**

Several concepts should be separate output images unless the user explicitly requests a combined comparison format.

## Pull requests

Explain:

- what redesign case the change improves;
- why existing guidance does not already cover it;
- what realistic prompt or screenshot scenario should trigger the new guidance;
- whether the root router needs to change.

Prefer small, evidence-driven changes after real usage tests.
