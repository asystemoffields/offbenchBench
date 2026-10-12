# Phase 1: Discover

Goal: a list of **10–30 candidate problems**, each saved as a card in `ledger/`. Discovery should be wide and cheap. Don't evaluate deeply yet; that is phase 2.

## Ask the operator first (briefly)

- Are there fields or kinds of institution they care about, or should you search everywhere?
- What languages and tooling can they review? For example, Python yes, Fortran no.
- About how much time can they put into reviewing the work?

If they don't have a preference, search everywhere. Fit to the operator comes in at scoring time.

## Where to look

Start from `sources.md`, which lists starting points and search queries. Treat it as a map, not an exhaustive list. Projects move, and some links will be stale.

Signals that help is wanted, from strongest to weakest:

1. A maintainer explicitly asks for help on a specific problem ("we'd welcome a PR", "help wanted", "anyone know how to…").
2. An issue is labeled `help wanted`, `good first issue`, `contributions welcome` or `needs: volunteer`.
3. A bug or gap is confirmed by a maintainer but has no assignee and no linked PR.
4. A project has a published roadmap or call for contributors, such as a funding call, grant deliverables or a GSoC idea list.
5. An open issue on an active project that accepts outside PRs (the minimum bar).

Also good: known-wrong behavior in scientific code, such as unit mismatches, silently dropped data, broken reproducibility or failing CI on main. These matter more than they look, and maintainers usually welcome a well-evidenced fix.

## Quick filters (drop a candidate immediately if any apply)

- It is closed, assigned, has a linked open PR, or someone said "I'm working on this" recently (roughly within 60 days) and nothing says they stopped.
- The project says no outside or AI-assisted contributions.
- The repo is archived, or a maintainer hasn't responded to anything in about 12 months.
- It is out of scope under `AGENTS.md` (competition, purely commercial, no code angle).
- It needs access the operator doesn't have, such as private data, special hardware or institutional accounts. Note this rather than drop it if the operator might have the access.

## Record each candidate

Copy `templates/candidate.md` to `ledger/<slug>.md`. Use slugs like `<org>-<repo>-<issue#>` or `<project>-<short-topic>`. Fill in the **Discovery** section only, set `status: discovered`, and add a log line.

Write down what you actually saw: the issue URL, the last maintainer activity date, any linked discussions. Phase 2 depends on these facts being accurate.
