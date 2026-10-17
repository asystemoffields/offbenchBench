# Phase 2: Evaluate

Goal: set each candidate's tier, score it, and produce a ranked shortlist of the **top 3–5** for the operator. For a dispatched problem, the goal is a tier, a verification plan and an honest estimate, on one card.

This phase has two passes: a quick triage of everything, then a bounded reconnaissance on what survives. Feasibility is scored from the reconnaissance, not from how the problem looks.

## Pass 1: quick triage (5–15 minutes each)

Read the problem page, issue thread or dispatch in full, and glance at the literature, data or code. Set the **tier** (routine, standard or high-stakes; see `AGENTS.md`), and score **Stakes**, **Verifiability** and **Open** provisionally. Drop anything that fails the phase 1 filters on closer reading. Carry the top 5–8 by stakes into pass 2. A dispatched routine task can skip pass 2 and go to phase 3.

## Pass 2: reconnaissance (bounded)

Spend the budget the operator set (default: a few hours of model time) on each carried candidate. The purpose is to learn what actually happens when you try, so that the traction score is evidence rather than a guess.

For an open problem or an empirical puzzle:

1. **Pin the statement.** Write the question out precisely, with every definition. If the source is ambiguous, record each reading. Many "open" problems have a weaker and a stronger form, and only one is open. Many "mysteries" dissolve once the claim is stated exactly.
2. **Check it is open.** Search the literature and the record: the problem's page and forum, arXiv, Google Scholar, zbMATH or MathSciNet if available, the OEIS, surveys, archives, prior expedition or survey reports. Record the queries. A list's "open" means its maintainer didn't know of a solution.
3. **Find the first move.** Try the obvious attacks long enough to learn something: compute small cases, look for a counterexample, try the natural special case, see whether a standard tool from a neighboring area applies, cross-reference the two datasets, formalize the statement. Write down what worked, what didn't and why.
4. **Name the obstacle.** State the specific thing that stands between the first move and a full result.

For a software, data or performance problem, reconnaissance means reproducing it: run the code, confirm the behavior, measure the baseline, locate the cause if it is quick.

Stop at the budget. Going over it on one candidate is phase 4 work and needs gate A.

## Scoring rubric

Score each dimension from 1 to 5, and write one sentence of evidence for each score. A score without evidence is a guess, so mark it `?` instead.

| Dimension | Weight | 1 | 3 | 5 |
|---|---|---|---|---|
| **Stakes** | ×3 | Cosmetic, or affects few people | A real result people would use or cite; a used tool gets meaningfully better | Resolves a named open problem, changes results people rely on, or settles a question a community has acted on |
| **Verifiability** | ×3 | Success is a matter of opinion, or checking it requires trusting the claimant | A written argument a specialist can check; a test or manual check can confirm a fix | A stranger can check it mechanically: a formal proof, a certificate, a test that fails without the fix, a measurement with its method, independent data |
| **Open** | ×2 | Status unconfirmed, or the venue's rules on AI or outside work are unclear | Open per the list and a shallow search; the venue accepts contributions | Open after a real literature search; the venue asks for results and sets clear rules |
| **Traction** | ×2 | No angle after the reconnaissance budget | A concrete approach with a specific, named obstacle | A line of attack with partial results already in hand |
| **Leverage** | ×1 | One-off | Unblocks a few people or a related question | Unblocks other problems, other users or downstream work |
| **Operator fit** | ×1 | Outside what they can check themselves | Partly | Squarely in what they can verify and sign |

**Total** = the weighted sum, out of 60. Count `?` as 2 and flag it.

### Judgment calls the numbers don't capture

- **The rubric is not a safety filter.** Pick the highest-stakes candidate with a credible line of attack, not the one most likely to go smoothly. Two candidates with the same total: take the higher stakes.
- **Traction 1 is a finding, not a failure.** A problem where honest effort finds no angle gets a low score and a note saying what was tried. That note is useful to the next person.
- **Prefer depth over polish.** A correctness bug in a calculation beats a docs typo. A partial result on a real problem beats a complete result on a trivial one.
- **Look for hidden size.** A small-looking issue can hide a larger one. An obscure problem can be open because nobody looked rather than because it is hard. Say so when you suspect either.
- **Watch for crowding.** If a problem's thread has had a dozen AI-generated "solutions" this month, your contribution adds little unless it is checked to a standard theirs weren't.
- **Check your own competence honestly.** If the domain needs expertise you don't have, say what reading would close the gap, and reflect it in the traction score and the obstacle, not by dropping the candidate.
- **Routine work still gets a plan.** A perf fix in a hobby game doesn't need a literature search, but it does need a baseline measurement and a definition of done. Write them on the card.

## Output

Update each card's **Evaluation** section, including the tier, the reconnaissance notes and the verification plan, and set `status: scored`. Then build the shortlist:

- Rank by total, but explain any case where your recommended order differs from the raw scores.
- Mark the top 3–5 candidates `status: proposed` (or the one dispatched candidate).
- Move on to phase 3. Don't continue solving anything yet.
