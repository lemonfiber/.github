# lemonfiber

A fully open-source, self-hosted media automation stack you can run in narrow
slices — *"just search"*, *"just download"*, *"everything"* — driven by a single
cross-platform binary that sets itself up.

No Plex, no proprietary tiers, no phone-home. The *arr ecosystem, Jellyfin and
Seerr, orchestrated by one tool that proves it's working rather than assuming it.

## The repos

| Repo | What it is |
|------|-----------|
| **[spec](https://github.com/lemonfiber/spec)** | The canonical specification. Everything starts here. |
| **[cli](https://github.com/lemonfiber/cli)** | The `lemonfiber` binary — CLI, TUI and web UI. Rust. |
| **[media-stack](https://github.com/lemonfiber/media-stack)** | The Docker Compose stack it orchestrates. |
| **[brand](https://github.com/lemonfiber/brand)** | Design system — logo, colour, type tokens. |
| **[homebrew-tap](https://github.com/lemonfiber/homebrew-tap)** | `brew install` formulae. |

## How this project works

**The spec is canonical.** No change lands in any repo unless it references
something in [`spec`](https://github.com/lemonfiber/spec) that already exists
there — enforced automatically. This keeps the specification ahead of the code
rather than trailing behind it. See
[contributing](https://github.com/lemonfiber/spec/blob/main/50-governance/contributing.md).

## Licence

Code is [Hippocratic License 3.0](https://firstdonoharm.dev/) — ethical-source,
source-available, deliberately not OSI-approved. Docs are CC BY-SA 4.0. The brand
marks are proprietary (trademark protection); the tokens are open.

---

Created and maintained by **[NightWorks.io](https://nightworks.io)** ·
Join us on **[Discord](https://discord.gg/daQmY23ym)**
