# Security policy

## Reporting a vulnerability

**Please do not report security vulnerabilities through public issues.**

Instead, use GitHub's private vulnerability reporting on the affected repository
(the **Security** tab → **Report a vulnerability**), or reach the maintainers
privately via [Discord](https://discord.nightworks.io).

Include, where you can:

- The repository and version affected
- A description of the vulnerability and its impact
- Steps to reproduce
- Any suggested remediation

We aim to acknowledge reports promptly and will keep you informed as we work on a
fix.

## The one that matters most

lemonfiber's threat model is documented in full in the spec
([40-quality/security.md](https://github.com/lemonfiber/spec/blob/main/40-quality/security.md)).
The single highest-severity class is **VPN egress leakage** — a
misconfiguration exposing a user's home IP to torrent peers. The stack verifies
this empirically at runtime, but reports of ways it can be defeated are especially
valuable.

## Scope

In scope: the `lemonfiber` binary, the stack definitions, credential handling, the
VPN isolation path, the local HTTP API and the clients that speak to it, and the
web UI.

Out of scope (stated in the threat model, not defended): nation-state adversaries,
physical access to the host, a compromised host operating system, and a malicious
operator on their own machine.

## Disclosure

Security fixes may be merged ahead of their spec change under the maintainer
[override](https://github.com/lemonfiber/spec/blob/main/50-governance/overrides.md),
precisely because a public spec PR describing a vulnerability must not precede its
patch. The spec is corrected immediately after.
