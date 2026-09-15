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
  <img alt="Platforms" src="https://img.shields.io/badge/macOS%20%C2%B7%20Linux%20%C2%B7%20Windows-E07A17?labelColor=17160F">
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

## Run only the part you need

Not "all twenty services or nothing." Named **forms** boot exactly the slice you
want — the rest stays off.

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

## And on the phone, when you are not at the machine

The CLI, the TUI and the web UI all run on the machine the stack runs on. That is
the right place to set it up and the wrong place to be standing when the
downloads stop at eleven at night.

The **companion** is the fourth surface: it pairs with a machine over your own
network, pins the certificate that machine presents, and shows what is running,
what stopped, and what the household asked for. It is one app serving two
people — which one it is for is decided by the credential that signs in, never
by which build was installed. Setup still happens at the machine; a phone cannot
perform the act that makes a phone able to perform acts.

## What's inside

Prowlarr · FlareSolverr · NZBHydra2 · SABnzbd · Gluetun · qBittorrent
(VPN-isolated) · Sonarr · Radarr · Lidarr · Bindery · Bazarr · **Jellyfin** ·
**Seerr** · Calibre-Web-Automated · Audiobookshelf · Navidrome · Recyclarr ·
Unpackerr · Homepage · Caddy — twenty services, pinned and wired together
automatically.

## Status

**The specification is complete, and the binary ships.**
Lemonfiber is spec-first — every decision is written down and argued for before a
line is written. Watch it come together, or help build it.

- 📐 **[Read the spec](https://github.com/lemonfiber/spec)** — every requirement, and the *why* behind every one
- 🗺️ **[The roadmap](https://github.com/lemonfiber/spec/blob/main/00-overview/roadmap.md)**, and the [releases](https://github.com/lemonfiber/lemonfiber/releases) that say where it has reached
- 💬 **[Join the Discord](https://discord.nightworks.io)**

## Want to help?

You don't need to write code — or even be especially technical:

- 🧪 **Try it and tell us what broke.** There is something to run now — bug reports and rough edges are gold.
- 📝 **Improve the docs.** Something unclear? Fix it — every repo's docs are open, and a docs PR is a real contribution.
- 🎨 **Design & UX.** The web UI and the brand welcome a good eye.
- 💬 **Hang out on [Discord](https://discord.nightworks.io).** Answer a question, share your setup, help shape the roadmap.
- ⭐ **Spread the word.** A star or a mention genuinely helps a young project find people.

Prefer to write code? The [spec](https://github.com/lemonfiber/spec) is complete
and the roadmap is open — start with a
[good first issue](https://github.com/lemonfiber/lemonfiber/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).

## The repos

Grouped by what they are for, because a single list of fifteen tells you where
nothing is.

### The specification

Everything starts here. Nothing is built that is not written down first.

| | |
| --- | --- |
| **[spec](https://github.com/lemonfiber/spec)** | Every requirement, and the argument behind each one |

### What runs

| | |
| --- | --- |
| **[lemonfiber](https://github.com/lemonfiber/lemonfiber)** | The binary — CLI, TUI and the local HTTP API the surfaces read (Rust) |
| **[lemonfiber-media-stack](https://github.com/lemonfiber/lemonfiber-media-stack)** | The twenty-service Compose stack it orchestrates, pinned by digest |

### The surfaces

Four ways to reach one machine. Each renders the core's answers and decides
nothing the core has not already decided.

| | |
| --- | --- |
| **[lemonfiber-web](https://github.com/lemonfiber/lemonfiber-web)** | The operator console and the household view, over the local API |
| **[lemonfiber-companion](https://github.com/lemonfiber/lemonfiber-companion)** | The phone, on the network rather than on the host — Blade compiled to SwiftUI and Jetpack Compose, no web view |

The CLI and the TUI are the binary's own and live with it.

### Extending it

A plugin is declarative data — a manifest, its recorded responses, and the
proofs those responses satisfy. Nothing in one is executable, and nothing in one
can be.

| | |
| --- | --- |
| **[plugin-template](https://github.com/lemonfiber/plugin-template)** | The one an author copies. It validates and proves unmodified |
| **[plugin-komga](https://github.com/lemonfiber/plugin-komga)** | Komga — comics and manga |
| **[plugin-uptime-kuma](https://github.com/lemonfiber/plugin-uptime-kuma)** | Uptime Kuma — endpoint monitoring |
| **[lemonfiber-plugins](https://github.com/lemonfiber/lemonfiber-plugins)** | Where a plugin is registered to be found. Publishing one needs nothing but a git repository; the registry is a convenience and a review, never a dependency |

### Talking to it

| | |
| --- | --- |
| **[sdk-ts](https://github.com/lemonfiber/sdk-ts)** | The TypeScript client, generated from the contract |
| **[sdk-php](https://github.com/lemonfiber/sdk-php)** | The PHP client, generated from the same one |

### Getting it

| | |
| --- | --- |
| **[homebrew-tap](https://github.com/lemonfiber/homebrew-tap)** | `brew install` |

### The public face

| | |
| --- | --- |
| **[website-lemonfiber.app](https://github.com/lemonfiber/website-lemonfiber.app)** | The frontpage, built from this org at build time |
| **[website-docs.lemonfiber.app](https://github.com/lemonfiber/website-docs.lemonfiber.app)** | The documentation site, rendered over the spec and each repo's own docs |
| **[brand](https://github.com/lemonfiber/brand)** | Logo, colour and type. Marks proprietary; tokens open |

### The org itself

| | |
| --- | --- |
| **[.github](https://github.com/lemonfiber/.github)** | These community health files, inherited by every repo above |

The documentation site is a placeholder; the other ten carry code or content.

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
