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
  <a href="https://discord.gg/FYuV9CbTHR"><img alt="Discord" src="https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white"></a>
  <img alt="Licence" src="https://img.shields.io/badge/licence-Hippocratic%203.0-17160F">
  <img alt="Status" src="https://img.shields.io/badge/status-spec%20complete%20%C2%B7%20building-F0C419?labelColor=17160F">
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

Not "all sixteen services or nothing." Named **forms** boot exactly the slice you
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

## What's inside

Prowlarr · SABnzbd · qBittorrent (VPN-isolated) · Sonarr · Radarr · Lidarr ·
Bindery · Bazarr · **Jellyfin** · **Seerr** · Calibre-Web · Audiobookshelf ·
Recyclarr · Homepage — 19 services, pinned and wired together automatically.

## Status

**The specification is complete; the code is being built in the open.**
Lemonfiber is spec-first — every decision is written down and argued for before a
line is written. Watch it come together, or help build it.

- 📐 **[Read the spec](https://github.com/lemonfiber/spec)** — 795 requirements, and the *why* behind every one
- 🗺️ **[The roadmap](https://github.com/lemonfiber/spec/blob/main/00-overview/roadmap.md)**
- 💬 **[Join the Discord](https://discord.gg/FYuV9CbTHR)**

## Want to help?

You don't need to write code — or even be especially technical:

- 🧪 **Try it and tell us what broke.** Once there's something to run, bug reports and rough edges are gold.
- 📝 **Improve the docs.** Something unclear? Fix it — every repo's docs are open, and a docs PR is a real contribution.
- 🎨 **Design & UX.** The web UI and the brand welcome a good eye.
- 💬 **Hang out on [Discord](https://discord.gg/FYuV9CbTHR).** Answer a question, share your setup, help shape the roadmap.
- ⭐ **Spread the word.** A star or a mention genuinely helps a young project find people.

Prefer to write code? The [spec](https://github.com/lemonfiber/spec) is complete
and the roadmap is open — start with a
[good first issue](https://github.com/lemonfiber/lemonfiber/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).

## The repos

| | |
| --- | --- |
| **[spec](https://github.com/lemonfiber/spec)** | The canonical specification — everything starts here |
| **[lemonfiber](https://github.com/lemonfiber/lemonfiber)** | The `lemonfiber` binary (Rust) |
| **[media-stack](https://github.com/lemonfiber/media-stack)** | The Compose stack it orchestrates |
| **[website](https://github.com/lemonfiber/website)** | The frontpage — built from the org itself |
| **[brand](https://github.com/lemonfiber/brand)** | Logo, colour and type |
| **[homebrew-tap](https://github.com/lemonfiber/homebrew-tap)** | `brew install` |

---

<p align="center">
  <a href="https://nightworks.io">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="../.github/nightworks-white.png">
      <img alt="NightWorks.io" src="../.github/nightworks-dark.png" height="20">
    </picture>
  </a>
  &nbsp;&middot;&nbsp;<a href="https://discord.gg/FYuV9CbTHR"><img alt="Discord" src="../.github/discord.svg" height="20"></a>
</p>
