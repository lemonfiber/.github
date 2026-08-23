# lemonfiber/.github

Org-wide community health files and the org's dependency policy, inherited by
every repository in the [lemonfiber](https://github.com/lemonfiber) organisation.
Maintained here once so they never drift between repos.

<p align="center">
  <a href="https://scorecard.dev/viewer/?uri=github.com/lemonfiber/.github"><img alt="OpenSSF Scorecard" src="https://api.scorecard.dev/projects/github.com/lemonfiber/.github/badge"></a>
</p>

| File | Applies to |
| ---- | ---------- |
| `profile/README.md` | The org profile page |
| `CONTRIBUTING.md` | Every repo without its own |
| `CODE_OF_CONDUCT.md` | Every repo |
| `SECURITY.md` | Every repo |
| `SUPPORT.md` | Every repo without its own |
| `.github/PULL_REQUEST_TEMPLATE.md` | Every repo's PRs |
| `.github/ISSUE_TEMPLATE/` | Every repo's issues |
| `default.json` | Every repo's Renovate config, via `"extends": ["github>lemonfiber/.github"]` |
| `typos.toml`, `.markdownlint.jsonc` | **This repo only** — see below |

These are canonical here. The governance *rules* they reflect live in
[lemonfiber/spec/50-governance](https://github.com/lemonfiber/spec/tree/main/50-governance);
this repo is the distribution mechanism, not the source of the rules.

## The two lint configs are not inherited

`typos.toml` and `.markdownlint.jsonc` are the exception, and it is worth knowing
which way round it is. The hygiene gate checks out **the calling repository** and
lints that tree, so the copy that governs a run is the one in the repo being
checked — not the copy here. A repo without one gets each tool's defaults.

They sit here because this repo needs them like any other, and they are a
reasonable thing to copy when starting a repo. They are not distributed, and
editing them here changes nothing anywhere else.

Changing any of these is a governed change like any other — cite a spec identifier
([GOV-R2](https://github.com/lemonfiber/spec/blob/main/50-governance/canonical-spec.md)).

---

<p align="center">
  <a href="https://nightworks.io">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset=".github/nightworks-white.png">
      <img alt="NightWorks.io" src=".github/nightworks-dark.png" height="20">
    </picture>
  </a>
  &nbsp;&middot;&nbsp;<a href="https://discord.nightworks.io"><img alt="Discord" src=".github/discord.svg" height="20"></a>
</p>
