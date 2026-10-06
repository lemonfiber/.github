<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="../.github/logo-on-ink.svg">
    <img alt="lemonfiber" src="../.github/logo.svg" height="96">
  </picture>
</p>

<h1 align="center">Self-host your media &mdash; without becoming a sysadmin</h1>

<p align="center">
  A fully open-source, self-hosted media automation stack &mdash; that sets
  <em>itself</em> up, runs in the exact slice you need, and <b>proves</b> it's
  working instead of hoping.
</p>

<p align="center">
  <a href="https://discord.nightworks.io"><img alt="Discord" src="https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white"></a>
  <img alt="Licence" src="https://img.shields.io/badge/licence-Hippocratic%203.0-17160F">
  <img alt="Status" src="https://img.shields.io/badge/status-building%20in%20the%20open-F0C419?labelColor=17160F">
  <img alt="Platforms" src="https://img.shields.io/badge/macOS%20%C2%B7%20Linux-E07A17?labelColor=17160F">
</p>

---

## The problem it kills

Self-hosting your own media works brilliantly — *once it's running*. Getting
there means a weekend of pasted Reddit compose files, six web UIs, hand-copied API
keys, and a nagging doubt that your VPN is actually hiding your IP. Then it breaks
in a way nothing warns you about, and you never touch it again.

**Lemonfiber is one small binary that does all of that for you** — and then keeps
watch.

```console
$ lemonfiber
  ┌─ lemonfiber ───────────────────────────────┐
  │  No configuration found.                   │
  │  Run first-time setup?             [Y/n]   │
  └────────────────────────────────────────────┘
```

## Try it

Lemonfiber runs on macOS and Linux and needs Docker.
[Install it](https://docs.lemonfiber.app/start/install/), run `lemonfiber`, and
answer the setup questions. [Your first stack](https://docs.lemonfiber.app/start/your-first-stack/)
walks through it.

## Run only the part you need

Not "all twenty services or nothing." Named **forms** start exactly the part you
want; the rest stays off.

```bash
lemonfiber up search      # just find things.  3 containers.
lemonfiber up dl          # just download a link you have.
lemonfiber up tv          # search → download → organise → subtitle.
lemonfiber up full        # the lot.
```

## Three promises

<table>
<tr>
<td width="33%" valign="top">

### 🍋 Genuinely open

No closed-source media server, no paid tier, no phone-home. Every service is
open-source and runs on **your** hardware. Jellyfin, the *arr apps, Seerr — the
good stuff, all of it yours.

</td>
<td width="33%" valign="top">

### ✂️ Runs in slices

"Just search." "Just download." "Everything." One config, one data folder, no
separate installs — boot the shape that fits the moment.

</td>
<td width="33%" valign="top">

### 🔒 Correct by construction

It **tests** hardlinks instead of assuming them. It compares public IPs to *prove*
your VPN isn't leaking. Silence means healthy — and it means it.

</td>
</tr>
</table>

## Set up once, everyone else just watches

You run the setup. Your household never sees Lemonfiber at all — they get **one
link, one account**: ask for something in Seerr, and it turns up in Jellyfin on
the TV. That's the whole experience.

## Watch and fix it from anywhere in the house

Set it up and run it from the command line, the terminal dashboard or the web
console on the machine itself. A **companion app** for phones is in
development: it pairs with your machine over your own network and shows what is
running, what stopped and what the household asked for.

## What's inside

Prowlarr · FlareSolverr · NZBHydra2 · SABnzbd · Gluetun · qBittorrent
(VPN-isolated) · Sonarr · Radarr · Lidarr · Bindery · Bazarr · **Jellyfin** ·
**Seerr** · Calibre-Web-Automated · Audiobookshelf · Navidrome · Recyclarr ·
Unpackerr · Homepage · Caddy: twenty open-source services, each pinned to a
version and wired together automatically.

## Status

Lemonfiber is before 1.0, and every release is a pre-release. It is built
spec-first: every requirement, and the reasoning behind it, is written down
before the code.

- 📖 **[The documentation](https://docs.lemonfiber.app)**: install, run, fix, and build on it
- 📐 **[The specification](https://github.com/lemonfiber/spec)**: every requirement, and the *why* behind each one
- 🗺️ **[The roadmap](https://docs.lemonfiber.app/project/roadmap/)**, and the [releases](https://github.com/lemonfiber/lemonfiber/releases) so far
- 💬 **[Join the Discord](https://discord.nightworks.io)**

## Want to help?

You don't need to write code — or even be especially technical:

- 🧪 **Try it and tell us what broke.** There is something to run now — bug reports and rough edges are gold.
- 📝 **Improve the docs.** Something unclear? Fix it — every repo's docs are open, and a docs PR is a real contribution.
- 🎨 **Design & UX.** The web UI and the brand welcome a good eye.
- 💬 **Hang out on [Discord](https://discord.nightworks.io).** Answer a question, share your setup, help shape the roadmap.
- ⭐ **Spread the word.** A star or a mention genuinely helps a young project find people.

Prefer to write code? Read [how change gets in](https://github.com/lemonfiber/.github/blob/main/CONTRIBUTING.md),
then start with a
[good first issue](https://github.com/lemonfiber/lemonfiber/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).

## The repos

Grouped by what they are for.

### The specification

Everything starts here. Nothing is built that is not written down first.

| | |
| --- | --- |
| **[spec](https://github.com/lemonfiber/spec)** | Every requirement, and the argument behind each one |

### What runs

| | |
| --- | --- |
| **[lemonfiber](https://github.com/lemonfiber/lemonfiber)** | The `lemonfiber` tool: command line, terminal dashboard, and the local web API everything else talks to (Rust) |
| **[lemonfiber-media-stack](https://github.com/lemonfiber/lemonfiber-media-stack)** | The Docker Compose stack it runs. Works with plain `docker compose` too |
| **[lemonfiber-request-gate](https://github.com/lemonfiber/lemonfiber-request-gate)** | A small service in the stack that lets Seerr ask Sonarr, Radarr and Jellyfin for a fixed set of things, and nothing more |
| **[lemonfiber-decline](https://github.com/lemonfiber/lemonfiber-decline)** | A small service in the stack that lets somebody turn down an invitation to the household |

### Ways to use it

The command line and the terminal dashboard are part of `lemonfiber` itself.

| | |
| --- | --- |
| **[lemonfiber-web](https://github.com/lemonfiber/lemonfiber-web)** | The web console for the person who runs the stack, and a view for the rest of the household. `lemonfiber ui` serves it |
| **[lemonfiber-companion](https://github.com/lemonfiber/lemonfiber-companion)** | The phone app, in development. Native on iOS and Android, no web view |

### Building on it

| | |
| --- | --- |
| **[sdk-ts](https://github.com/lemonfiber/sdk-ts)** | TypeScript client for the local web API |
| **[sdk-php](https://github.com/lemonfiber/sdk-php)** | PHP client for the same API |
| **[sdk-python](https://github.com/lemonfiber/sdk-python)** | Python client for the same API, synchronous and asynchronous |
| **[integration-home-assistant](https://github.com/lemonfiber/integration-home-assistant)** | The stack's health, controls and a member's library in Home Assistant |
| **[integration-mcp](https://github.com/lemonfiber/integration-mcp)** | An MCP server, so an AI assistant can use the web API through a scoped key |

### Extending it

A plugin adds a service to the stack as declarative data: a manifest, recorded
responses, and checks those responses must pass. Nothing in a plugin runs as
code.

| | |
| --- | --- |
| **[plugin-template](https://github.com/lemonfiber/plugin-template)** | Copy this to write a plugin. It validates unmodified |
| **[plugin-komga](https://github.com/lemonfiber/plugin-komga)** | Komga: comics and manga |
| **[plugin-uptime-kuma](https://github.com/lemonfiber/plugin-uptime-kuma)** | Uptime Kuma: endpoint monitoring |
| **[plugin-plex](https://github.com/lemonfiber/plugin-plex)** | Plex: a worked example that asks for more than plugins may do today, so it cannot be installed yet |
| **[lemonfiber-plugins](https://github.com/lemonfiber/lemonfiber-plugins)** | The reviewed catalogue where plugins are listed so people can find them. A plugin needs only a git repository; the catalogue is optional |

### Getting it

| | |
| --- | --- |
| **[homebrew-tap](https://github.com/lemonfiber/homebrew-tap)** | The Homebrew tap. It holds a placeholder formula, so `brew install` installs nothing yet; use the installer in the [install guide](https://docs.lemonfiber.app/start/install/) |

### The public face

| | |
| --- | --- |
| **[website-lemonfiber.app](https://github.com/lemonfiber/website-lemonfiber.app)** | [lemonfiber.app](https://lemonfiber.app), built from this organisation's live state |
| **[website-docs.lemonfiber.app](https://github.com/lemonfiber/website-docs.lemonfiber.app)** | [docs.lemonfiber.app](https://docs.lemonfiber.app), the documentation and the specification in one site |
| **[brand](https://github.com/lemonfiber/brand)** | Logo, colour and type. The marks are proprietary; the tokens are open |

### The organisation

| | |
| --- | --- |
| **[.github](https://github.com/lemonfiber/.github)** | The community health files every repository above inherits |

Lemonfiber is made by [NightWorksIO](https://nightworks.io).

---

<p align="center">
  <a href="https://nightworks.io">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="../.github/nightworks-white.png">
      <img alt="NightWorks.io" src="../.github/nightworks-dark.png" height="20">
    </picture>
  </a>
  &nbsp;&middot;&nbsp;<a href="https://discord.nightworks.io"><img alt="Discord" src="../.github/discord.svg" height="20"></a>
</p>
