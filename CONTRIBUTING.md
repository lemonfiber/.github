# Contributing to Lemonfiber

Thank you for wanting to contribute. This project works a little differently from
most, and understanding the one core rule up front will save you a round-trip.

## You don't have to write code

The most valuable contributions often aren't code:

- **Try it and report what broke** — clear bug reports save everyone time.
- **Fix or improve docs** — spot something unclear and fix it; a docs PR counts.
- **Design & UX feedback** — on the web UI or the brand.
- **Help others** on [Discord](https://discord.nightworks.io), and shape the roadmap.
- **Spread the word** — a star or a mention helps a young project.

Non-code changes still follow the one rule below (they cite a spec identifier, or
`GOV-R12` for routine docs), but they're just as welcome as code. If you're not
sure how to file something, ask on Discord — we'll help.

## The one rule

**The [spec](https://github.com/lemonfiber/spec) is canonical. Every change cites
something in it that already exists.**

A specification that trails its implementation is useless — so here the spec leads.
Every commit to an implementation repo — `lemonfiber`, `media-stack`,
`lemonfiber-web`, `sdk-ts`, `sdk-php`, `brand`, `website`, `homebrew-tap` and this
one — references a spec identifier (a requirement like `A2-R4`, an `ADR-0006`, or
a governance rule like `GOV-R12`), and that identifier must already be merged in
the spec.

## Which case are you in?

**Implementing something already specified** — find the requirement, cite it:

```
feat: health-gate service startup

Spec: B2-R1, B2-R2
```

Put the same IDs in your PR body. That's it.

**Changing how the product behaves** — open a small PR against
[`spec`](https://github.com/lemonfiber/spec) *first*. Usually one requirement row
and a short paragraph. Once it merges, cite the new ID in your implementation PR.

**Routine maintenance** (dependencies, formatting, CI) — cite `GOV-R12`.

## Full guide

The complete contributor guide lives in the spec:
**[50-governance/contributing.md](https://github.com/lemonfiber/spec/blob/main/50-governance/contributing.md)**.

It covers finding the right identifier, the change lifecycle, what the CI checks,
and what to do if your PR is closed (it's sequenced, not rejected — reopening is
one click).

## Before you open a PR

- Your change cites a spec identifier, in a commit trailer **and** the PR body.
- If it changed behaviour, the spec PR merged first.
- Tests pass, and the [definition of done](https://github.com/lemonfiber/spec/blob/main/40-quality/definition-of-done.md) is met.
- No requirement IDs in code comments — they go in commits and PRs only.

## Questions

Ask in [Discord](https://discord.nightworks.io), or open an issue. If you're unsure
which repo an issue belongs in, file it anywhere — routing is our job, not yours.
