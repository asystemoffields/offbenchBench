# Phase 1: Discover

Goal: candidate problems saved as cards in `ledger/`. If the operator **dispatched** a problem, this phase is one card: fill in what you know, note what you don't, and go to phase 2. If the operator asked you to **find** something, aim for **10–30 candidates**, searched wide and cheap. Don't evaluate deeply yet; that is phase 2.

## Ask the operator first (briefly)

- Is there a problem already in hand, or should you go looking? If looking: which fields, communities or kinds of problem? Science, mathematics, software, crowdsourced projects, puzzles with open data, or everywhere?
- What can they check themselves? A proof, a Lean file, a Python diff, a GIS layer, a game's frame-time trace? The operator must be able to verify the result before it goes public, so this bounds what can be *contributed*, not what can be *attempted*.
- How much effort should reconnaissance get per shortlisted candidate in phase 2? Default: a bounded session of a few hours of model time.
- Roughly how much time can they put into reviewing?

If they have no preference, search everywhere.

## Where to look

Start from `sources.md`. Treat it as a map, not an exhaustive list. Projects move, lists go stale, and some links will be dead.

### Open problems: signals that a problem is a good target

1. It has a precise statement, or one can be pinned down from the source.
2. It is on a maintained list with a recorded status and a place to report results (erdosproblems.com, Formal Conjectures, the OEIS, a problem garden, a paper's open-questions section with a reachable author).
3. Its difficulty is unknown rather than known. Problems that many strong people have attacked for decades with nothing to show are poor targets. Problems that are obscure, recently posed, or sitting at the edge of a tool that just got better (large computation, SAT and SMT solvers, formal libraries, model-assisted search) are good ones.
4. There is a concrete first move: a finite search, a special case, a reformulation, an object to construct, a technique from a neighboring area, a dataset nobody has cross-referenced.
5. The result would be used: cited, built on, or would change what a community believes or does.

### Software, data and community projects: signals that help is wanted

1. A maintainer or project lead explicitly asks for help on a specific problem.
2. An issue is labeled `help wanted`, `good first issue`, `contributions welcome` or similar.
3. A bug or gap is confirmed by a maintainer but has no assignee and no linked PR.
4. A published roadmap, funding call, volunteer call or GSoC idea list.
5. An open issue on an active project that accepts outside PRs (the minimum bar).

Known-wrong behavior in code people rely on, such as unit mismatches, silently dropped data, broken reproducibility, or a method that doesn't do what the paper says, matters more than it looks. So does a crowdsourced project whose volunteers are doing by hand what a script could do for them.

### Empirical puzzles

Lost objects, unexplained observations, unidentified signals, unattributed documents. These are in scope when there is open data to work with and a community or institution that would act on a result (an archive, a museum, a survey team, a project's science team). They are high-stakes by default: a wrong answer sends people to the wrong place. Record who would act on the result and what they would need to see.

## Quick filters (drop a candidate immediately if any apply)

- **Already solved.** The list marks it solved, the thread reports a solution, or a quick search finds one. Record what you searched; a deeper search comes in phase 2.
- **Actively claimed.** Someone announced a solution or said "I'm working on this" recently (roughly within 60 days) and nothing says they stopped. For software: assigned, or has a linked open PR.
- **The venue says no.** The project, list, forum or data owner does not accept outside or AI-assisted contributions, or its data terms forbid the use.
- **Dead venue.** The repo is archived, the list is unmaintained with nowhere to report, or nobody has responded in about 12 months.
- **Out of scope** under `AGENTS.md`.
- **Inaccessible.** Needs private data, special hardware, site access or institutional accounts the operator lacks. Note rather than drop if the operator might have access.

Do **not** drop a candidate because it looks hard. That is what reconnaissance in phase 2 is for.

## Record each candidate

Copy `templates/candidate.md` to `ledger/<slug>.md`. Use slugs like `erdos-123`, `oeis-A000001-conj`, `<org>-<repo>-<issue#>`, `zooniverse-<project>-<topic>` or `<project>-<short-topic>`. Fill in the **Discovery** section only, set `status: discovered`, give a provisional tier, and add a log line.

Write down what you actually saw: the URL, the stated status and its date, the last activity on the page or thread, any linked discussion, literature or data. Phase 2 depends on these facts being accurate.
