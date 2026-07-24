<!--
  The spec is canonical. Every change cites a spec identifier that already
  exists on spec@main. See:
  https://github.com/lemonfiber/spec/blob/main/50-governance/contributing.md
-->

## What & why

<!-- One or two sentences. What does this change do, and why? -->

## Spec citation

<!--
  Cite the requirement(s), ADR, or governance rule this implements.
  These MUST also appear as a `Spec:` trailer in at least one commit, e.g.

      Spec: B2-R1, B2-R2

  - Implementing something specified? Cite it.
  - Changing behaviour? The spec PR must be merged FIRST, then cite the new ID.
  - Routine maintenance (deps, formatting, CI)? Cite GOV-R12.
-->

Spec:

## Checklist

- [ ] Cites a spec identifier that exists on `spec@main`, in a commit trailer and above
- [ ] If behaviour changed, the spec PR merged first
- [ ] No requirement IDs in code comments (they go in commits/PRs only)
- [ ] Tests pass and the [definition of done](https://github.com/lemonfiber/spec/blob/main/40-quality/definition-of-done.md) is met
