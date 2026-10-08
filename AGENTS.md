# AGENTS.md — .github

> **Start at the roadmap and board on [lemonfiber.app](https://lemonfiber.app),
> rendered from the report of where every unreleased version stands. Then the
> rules** every repository shares:
> [working in the repositories](https://github.com/lemonfiber/spec/blob/main/50-governance/working-in-the-repositories.md)
> and [the rules for agents](https://github.com/lemonfiber/spec/blob/main/50-governance/ai-contributors.md).
> This file holds only what is true of this repository.

## What this repo is

Org-wide community health files, inherited by every repo. Dependency policy is
not among them — Dependabot has no org-level preset, so each repo carries its own
`.github/dependabot.yml`. Canonical here; the governance *rules* they reflect
live in the spec's 50-governance. A change here is a governed change — cite a
spec identifier (`GOV-R2`). See README.md.

## Before you push

```sh
just ci
```

`typos` and `lychee`, which is everything CI reads in this repository's own
tree. It turns this clone's git hooks on as its first step. The jobs `just ci`
does not run are named in the `justfile` beside the recipe, with what covers
each.
