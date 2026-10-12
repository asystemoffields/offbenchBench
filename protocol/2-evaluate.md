# Phase 2: Evaluate

Goal: score each `discovered` candidate, then produce a ranked shortlist of the **top 3–5** for the operator.

Read the issue thread in full, glance at the relevant code, and check recent commit and PR activity. Spend about 5–15 minutes per candidate. If a candidate needs more than that to understand, that tells you something about its feasibility score.

## Scoring rubric

Score each dimension from 1 to 5, and write one sentence of evidence for each score. A score without evidence is a guess, so mark it `?` instead.

| Dimension | Weight | 1 | 3 | 5 |
|---|---|---|---|---|
| **Scientific impact** | ×3 | Cosmetic, or affects few users | Real improvement to a used tool | Changes results people rely on, e.g. wrong units or wrong outputs in operational or published science |
| **Wanted** | ×2 | Open issue, no maintainer signal | Maintainer confirmed it | Maintainer explicitly asked for help with it |
| **Maintainer responsiveness** | ×2 | No responses in months | Responds within weeks | Active this week; reviews PRs |
| **Feasibility** | ×2 | Needs unavailable data, hardware or deep domain expertise | Doable with effort and some domain reading | Clear path; can reproduce locally |
| **Verifiability** | ×2 | Success is a matter of opinion | Tests or a manual check can confirm it | Objective evidence is possible: a test, a backtest, comparison to reference data |
| **Leverage** | ×1 | One-off | Unblocks a few users | Unblocks other work, other users or downstream projects |
| **Operator fit** | ×1 | Outside what they can review | Partly | Squarely in their skills or interests |

**Total** = the weighted sum, out of 65. Count `?` as 2 and flag it.

### Judgment calls the numbers don't capture

- **Prefer depth over polish.** A correctness bug in a scientific calculation beats a docs typo, even when the typo is easier.
- **Look for hidden size.** An issue that looks small can hide a larger problem. In the OCF example, a dependency bug sat next to a units bug that was quietly degrading forecasts. Say so if you suspect it.
- **Watch for crowding.** If several newcomers are circling the same `good first issue`, your contribution adds little.
- **Check your own competence honestly.** If the domain needs expertise you don't have, say what reading would close the gap, and lower the feasibility score.

## Output

Update each card's **Evaluation** section and set `status: scored`. Then build the shortlist:

- Rank by total, but explain any case where your recommended order differs from the raw scores.
- Mark the top 3–5 candidates `status: proposed`.
- Move on to phase 3. Don't start solving anything yet.
