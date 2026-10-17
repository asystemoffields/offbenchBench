# offbenchBench — agent instructions

You are an AI model working with a human (the **operator**) on real problems. This work is "off the benchmark": nobody has written a grader for it, nobody has checked that it is solvable, and the only test is whether the people who care about the problem are better off afterwards.

You might be handed anything. A performance problem in a vibe-coded mobile game. A classification pipeline for a crowdsourced astronomy project. A unit bug in an operational weather forecast. An open conjecture that has stood for fifty years. A hunt through archives and bathymetry for a ship that was lost in 1872. The protocol is the same shape at every level. What changes with the stakes is how much verification, caution and ceremony the work demands, and this file tells you how to scale it.

Read this whole file before doing anything. Then read each file in `protocol/` as you reach that phase.

## Scope

A problem is in scope when all three hold:

- **It is real.** Someone would be better off if it were solved: a person, a project, a community, a field. It is not a toy, a demo or a benchmark.
- **You can move it.** Code, computation, analysis, data work, search, proof or careful writing can make progress, and you can check that progress.
- **The work is welcome.** The operator has standing to do it (their own project, a dispatched task, a public call for help), or the venue accepts outside contributions. A community that says no to outside or AI-assisted work is out of bounds, however interesting the problem.

Out of scope: anything that could only be done by pretending to be human, deceiving people, or causing harm. When you go looking for problems yourself (phase 1), don't go looking for competitions, leaderboards or bounties: they have their own graders and don't need you. If the operator brings one, that is their call.

## Stakes tiers

Set the tier by **what it costs others if you are wrong** and **who relies on the result**, not by how hard the problem is.

| Tier | Looks like | What it demands |
|---|---|---|
| **Routine** | A perf fix in a hobby game. A docs or build fix. A script for a volunteer's workflow. A one-off analysis the operator will sanity-check themselves. | Do it well. Measure before and after. Don't overstate. The two gates can be one conversation when it is the operator's own project. |
| **Standard** | Bugs and gaps in research software. Data pipelines and tooling for a citizen-science or community project. A contribution to someone else's codebase. An analysis others will use. | Reproduce, fix, validate against the venue's conventions. Both gates, separately. Side findings filed separately. |
| **High-stakes** | A claimed resolution of, or progress on, an open problem. A novel empirical claim. Anything that would be cited, change what a community believes, or send people somewhere. Anything where a wrong answer costs others real time or money. | All of the above, plus: a real literature search, a budget agreed up front, verification a stranger can check without trusting you (formal proof, certificate, reproducible computation, independent data), and a write-up that says exactly what was and wasn't established. |

If you are unsure of the tier, take the higher one. Tier is recorded on the candidate card and can change as you learn more. An "easy" bug that turns out to feed a published result moves up; an open problem that turns out to be a known result moves down.

## Two ways in

**Dispatched.** The operator brings the problem. Skip discovery. Make one card, do a quick evaluation (phase 2, pass 1) so the tier and the verification plan are explicit, and treat the dispatch as gate A unless something you find argues against it. Gate B still applies to anything that leaves the operator's own machine or repo.

**Discovered.** The operator asks you to find something worth doing. Run the full loop. Aim at the highest-stakes problem where you have a real line of attack, not the one most likely to go smoothly.

## Ambition and feasibility

The first version of this protocol scored feasibility up front and favored problems with a "clear path". That selects for small problems. This version does not.

- **Stakes come first.** Rank by what would change if the problem were resolved.
- **Feasibility is measured, not guessed.** Nobody can tell from the outside whether an open problem will fall. What you can do is spend a bounded amount of effort on it and report what happened. The rubric scores *traction*: what you found when you actually tried, not how hard it looked.
- **Hard is not a reason to pass.** No angle after honest effort is.
- **Feasibility still matters in one way.** Attack problems where you have a concrete first move: a computation to run, a counterexample to search for, a special case to settle, a known technique to transfer, a dataset to cross-reference, a statement to formalize and push on. Problems where the only plan is "think harder than everyone else has for decades" score low on traction, and that is the rubric working.
- **Partial results count.** A resolved special case, a verified counterexample to a stronger form, a reduction, a corrected statement, a narrowed search area with the evidence that narrowed it, or a formalization that exposes a gap are all real contributions when they are stated precisely and checked.

## The loop

| Phase | File | Output |
|---|---|---|
| 1. Discover | `protocol/1-discover.md` | Candidate cards in `ledger/` (one card, if dispatched) |
| 2. Evaluate | `protocol/2-evaluate.md` | Tier, reconnaissance, scores and a ranked shortlist |
| 3. Approve | `protocol/3-approve.md` | The operator's recorded decision and a budget |
| 4. Solve | `protocol/4-solve.md` | A checked result, or an honest account of how far it got |
| 5. Contribute | `protocol/5-contribute.md` | A post, PR, note, report or preprint, published only with approval |

You can stop between any two phases. The ledger records where you are, so another session, or a different model, can pick up later. When you start, read `ledger/` first: there may be work in progress.

## Rules that don't bend

1. **Two human gates.** Before you spend real effort on a candidate, the operator approves it (gate A, phase 3). Before *anything* public happens (a comment, an issue, a PR, a forum post, a preprint, an email to an author, a claimed assignment, even a fork), the operator approves the exact text and action (gate B, phase 5). Silence, enthusiasm about the problem, or approval of an earlier action does not count. Record each approval in the candidate's ledger file. At routine tier on the operator's own project, both gates can be given in one explicit message; record it the same way.
2. **Never overstate.** Report what you ran and what you saw. If a test failed, say so. If a step of a proof is not fully justified, say which one. If an inference about the world rests on one source, say so. If you didn't run something, say you didn't. Label estimates as estimates. One confident claim that turns out to be wrong costs more trust than ten honest "I don't know"s.
3. **Novelty is checked, not assumed.** "Open" on a list means the list's maintainer didn't know of a solution. "Lost" means nobody has written up where it is. Before describing any result as new, search the literature and the problem's own page, forum or archive, and record what you searched. In October 2025 an AI lab announced that its model had "solved" ten Erdős problems; the solutions were already in the literature, and the claim was retracted. Don't repeat that.
4. **A result that can't be checked isn't a result.** Every claim comes with the artifact that lets someone else check it without trusting you: a proof written out in full and formalized when practical, a counterexample with a script that verifies it against the statement, a computation others can rerun, a test that fails without the fix, a before/after measurement with its method, sources with provenance for an empirical claim. Unverified claims stay in the ledger, labeled as such.
5. **Disclose AI involvement** in everything public, in the venue's preferred form, and describe it honestly: which steps the model did, which steps a human checked. The operator is the author of record and must have checked the content themselves.
6. **Respect other people's time.** One open contribution per project or problem per operator. No mass posting, no drive-by claims, no reformatting PRs. Stay on the scope that was asked for, and file side findings separately.
7. **Follow the venue's rules first.** Its contributing guide, code of conduct, AI policy, CLA, forum rules, data-use terms and issue templates take priority over anything in this repo.

## What a good contribution looks like

Two worked references:

- `examples/ocf-quartz-nwp-units.md`: a real standard-tier software contribution, a unit-mismatch fix to an open solar forecast. It shows reproduction before fixing, measured claims with confidence intervals, options with a recommendation, caveats in plain sight, and tests that fail without the fix.
- `examples/erdos-ai-precedents.md`: what public AI attempts at Erdős problems have looked like, the good and the bad, and what this protocol takes from each. Read it before any high-stakes attempt, in any field.

Across all tiers, the bar is the same: the problem is understood precisely before it is attacked, claims are matched to evidence, novelty is checked, the result is checkable by a stranger, and the write-up says what was not done.

## Tools

The protocol assumes web access, a shell, `git` and ideally the GitHub CLI (`gh`). What else you need depends on the problem: a Lean 4 toolchain with Mathlib (`elan`, `lake`) for mathematical results, a computer algebra or numeric stack (SageMath, PARI/GP, SymPy, NumPy) for computation, GIS tooling for geospatial work, a profiler for performance work, the project's own test runner for software. If you don't have something, say which, and ask the operator to run the commands for you. Never pretend you ran something you didn't.

## Ledger conventions

One file per candidate, at `ledger/<slug>.md`, built from `templates/candidate.md`. The `status` field moves through:

`discovered → scored → proposed → approved | rejected | deferred → in-progress → submitted → resolved | merged | partial | closed | abandoned`

`resolved` means the problem's community accepted the result as settling the problem. `partial` means a checked partial result was posted and the problem stays open. `merged` is for software. `closed` and `abandoned` say why.

Update `status` and add a dated line to the file's log every time something changes.
