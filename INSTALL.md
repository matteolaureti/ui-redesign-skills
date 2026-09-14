# Installation

This repository uses [skills.sh](https://skills.sh) as the installation method.

## Install

```bash
npx skills add matteolaureti/ui-redesign-skills
```

The repository exposes one installable skill:

```text
redesign-ui-from-screenshots
```

## Update

```bash
npx skills update redesign-ui-from-screenshots
```

You can also update all installed skills with:

```bash
npx skills update
```

After updating, start a fresh agent/Codex session so the new skill contents are loaded.

## Output invariant

The installed skill follows this rule:

> **One output image = one complete redesign.**

If several redesign directions are requested, each direction should be generated as a separate full-size output image unless the user explicitly asks for a combined comparison format.
