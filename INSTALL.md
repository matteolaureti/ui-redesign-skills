# Installation

This repository uses [skills.sh](https://skills.sh) as the primary installation method.

## Install the full collection

```bash
npx skills add matteolaureti/ui-redesign-skills
```

This installs all valid skills discovered in the repository.

## Install a single skill

### Core redesign skill

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill ui-redesign-core
```

Use for general screenshot-based UI redesign.

### Dashboard redesign

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill dashboard-redesign
```

Use for SaaS dashboards, admin panels, analytics interfaces and operational workspaces.

### Landing page redesign

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill landing-page-redesign
```

Use for product landing pages, SaaS marketing sites and conversion-focused web pages.

### iOS app redesign

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill ios-app-redesign
```

Use for iPhone and iPad interface redesign.

### Component redesign

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill component-redesign
```

Use when redesigning only one card, panel, table, modal, FAQ, pricing block, navigation element or localized section.

### Design direction explorer

```bash
npx skills add https://github.com/matteolaureti/ui-redesign-skills --skill design-direction-explorer
```

Use when generating several substantially different redesign directions.

## Recommended combinations

### General UI redesign

```text
ui-redesign-core
```

### Dashboard

```text
ui-redesign-core
dashboard-redesign
```

### Landing page

```text
ui-redesign-core
landing-page-redesign
```

### iOS app

```text
ui-redesign-core
ios-app-redesign
```

### Single component

```text
ui-redesign-core
component-redesign
```

### Multiple dashboard directions

```text
ui-redesign-core
dashboard-redesign
design-direction-explorer
```

### Multiple landing-page directions

```text
ui-redesign-core
landing-page-redesign
design-direction-explorer
```

### Multiple iOS directions

```text
ui-redesign-core
ios-app-redesign
design-direction-explorer
```

## Update installed skills

```bash
npx skills update
```

New installations always fetch the current repository contents.

## Repository rule

Every skill in this collection follows the same output invariant:

> **One output image = one complete redesign.**

If multiple redesign directions are requested, each direction should be generated as a separate full-size output image rather than combined into a contact sheet.
