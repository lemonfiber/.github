# AGENTS.md — .github

> **Start at the report** of where every unreleased version stands: the summary
> of the newest run of the spec's [`state` workflow](https://github.com/lemonfiber/spec/actions/workflows/state.yml),
> or `just goals <version>` in a spec checkout.
> **Then the rules every repository shares:**
> [working in the repositories](https://github.com/lemonfiber/spec/blob/main/50-governance/working-in-the-repositories.md)
> and [the rules for agents](https://github.com/lemonfiber/spec/blob/main/50-governance/ai-contributors.md).
> This file holds only what is true of `.github`.

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
tree. It turns this clone's git hooks on as its first step, and
`.githooks/commit-msg` then refuses a commit that CI would refuse — a
non-conventional subject, a missing sign-off, a missing `Spec:` citation, or a
trailer crediting an assistant. The jobs `just ci` does not run are named in the
`justfile` beside the recipe, with what covers each.
