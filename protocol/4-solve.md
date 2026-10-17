# Phase 4: Solve

Goal: a result you can show evidence for. Set `status: in-progress`.

For an open problem, that means a proof, a construction, a counterexample or a computation that settles the question or a precisely stated part of it. For an empirical puzzle, a conclusion with its evidence, its uncertainty and the alternatives it rules out. For software, data or performance work, a change that is reproduced, fixed and validated. All of it checked to the standard in section 4, scaled to the tier.

Work in a local clone or workspace outside this repo, for example `work/<slug>/`, which is gitignored. Don't fork yet: a fork is public and needs gate B.

Track the budget agreed at gate A. When it runs out, go to section 6 whatever state the work is in.

## 1. Pin it down

**Open problem.** Write the statement out formally, with every definition, every quantifier and the exact source wording beside it. If there are several readings, pick one, say which, and note the others. If a Lean toolchain is available, state it in Lean against Mathlib, or check the statement in Formal Conjectures if it is there. A formal statement catches misreadings before they cost weeks, and it is the artifact a verifier will want later.

**Empirical puzzle.** Write down the claim you would be making if you succeeded, what evidence would establish it, what evidence would refute it, and what the competing explanations are. Decide now what would count as "found", "narrowed" and "ruled out".

**Software, data, performance.** Reproduce the problem on the current default branch, and record the exact commands, versions, inputs and output. For performance: a baseline measurement with its method, on hardware you name. If you can't reproduce it, stop and report that. Narrow it to the smallest case that shows the problem and identify the cause.

## 2. Know what is known

At standard and high-stakes tiers, do the literature and record search properly now, not just the phase 2 version. Look for: the problem's own page, forum and comments; papers that cite the source; surveys; the OEIS for any sequence that appears; related problems on the same list; recent preprints, since AI-assisted results are now arriving fast; prior survey, expedition or archival reports for a puzzle. Record every query and what it returned in the ledger. Read the closest results. One of them may contain the key lemma, the dataset, or the whole answer.

For any change that touches a scientific calculation, find the correct behavior in a primary source: a paper, a standard, a spec, the data provider's documentation. Cite it.

## 3. Attack

Pick strategies that give concrete feedback, and keep notes on each:

- **Compute.** Small cases, exhaustive search up to a bound, numerical experiments, profiles. Look at the data before theorizing.
- **Hunt a counterexample.** To the statement, and to natural stronger forms. A verified counterexample to a stronger form is a result.
- **Settle a special case.** The smallest nontrivial parameter, the symmetric case, the case the source calls "easy but unwritten".
- **Reduce.** Show the problem follows from, or is equivalent to, something known or better understood.
- **Transfer a technique.** The tool that cracked a neighboring problem often applies with modification.
- **Cross-reference.** Two independent sources that agree are worth more than one that is confident. For a puzzle, the result is usually in the join between datasets nobody put side by side.
- **Formalize as you go.** For a proof, writing it in Lean while you build it finds the gaps while they are cheap.
- **Certify a computation.** Where a finite check settles it, produce a certificate someone can re-check independently of your code.

When there is more than one reasonable approach, write them down as options, say which you are pursuing and why, and change course when the evidence says to. Record that too.

For software: match the project's style and conventions, make the smallest change that fixes the cause properly, don't refactor, and write down other problems for separate issues. For performance: change one thing at a time and measure each.

## 4. Verify

Match the evidence to the claim. The standard, at every tier, is that someone who doesn't trust you can check it. The tier sets how far you go.

| Claim | Evidence |
|---|---|
| "This is a proof" | The full argument written out with no step left as "clearly". Then, where at all practical, a formalization in Lean 4 against Mathlib with `#print axioms` showing no `sorryAx`. Where it is not practical: an adversarial check by an independent session or model given only the statement and the proof and told to find the error, and the operator's own reading of every step. |
| "This is a counterexample" | The object itself, and a script that checks it against the formal statement, not against your understanding of it. Run it. Include the output. |
| "The computation settles it" | Reproducible code, the exact inputs and versions, the output, and where possible a certificate checkable by an independent tool. State what the computation covers and what it doesn't. |
| "This is a partial result" | The exact statement established, at the same precision as the full problem, and a clear line between it and what remains open. |
| "It is here" / "this is what happened" | Every source with provenance; which are independent; the inference chain step by step; the uncertainty; the alternatives considered and why they are less likely; what observation would settle it. |
| "It no longer crashes" | A reproduction that fails before and passes after; the full test suite passes. |
| "It's more correct" | Comparison against a reference: a known value, independent data or the spec. |
| "It's faster" | Before/after on the same hardware and inputs, repeated, with variance; the method; and confirmation that behavior is unchanged. |
| "Results improved" | A before/after metric on a fair evaluation, with uncertainty, and the evaluation's limits stated. |

Before calling anything a proof, try to break it: find the step that uses each hypothesis, check inequalities at the boundary, check small cases against the general claim, check that the claimed object satisfies the definition as written rather than as remembered. Most wrong proofs by models fail at an unjustified "similarly" or a quantifier swap. Look there first.

Before calling anything found, try to explain the evidence another way. If you can, you haven't found it.

Then check novelty again against what section 2 turned up. If the result is known, say so. A clear account of a known result found independently, with a formalization, can still be worth posting, but it is not described as new.

For software: add tests, confirm each **fails without the fix**, and run the whole suite. Write down any failures that also happen without your change.

## 5. Write it up

Draft the post, PR, note, report or preprint with `templates/contribution.md`. Save the draft, your notes, the search queries and the commands you ran in the candidate's ledger file, or link to them from there. Then go to phase 5.

## 6. When the budget runs out or you get stuck

Stop and report to the operator. Say precisely what was established, what wasn't, what was tried and where it broke. Update the ledger.

This is a normal ending, not a failure. The honest options are:

- **Ask for more budget**, with a specific reason to think it would help.
- **Post the partial result**, if it meets the verification standard, via phase 5.
- **Post the reconnaissance**, where the venue welcomes it: what was tried, what the obstacle is, any computation or search that narrows the problem. Only where this helps the next person and the venue's rules allow it.
- **Record and stop.** Set `status: abandoned` with the account in the ledger, so the next session doesn't repeat the work.

Never stretch a partial result into a full one to avoid this section.
