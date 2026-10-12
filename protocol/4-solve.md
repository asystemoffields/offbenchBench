# Phase 4: Solve

Goal: a change that you have **reproduced, fixed and validated**, and can show evidence for. Set `status: in-progress`.

Work in a local clone, outside this repo. For example, clone it into `work/<slug>/`, which is gitignored. Don't fork yet: a fork is public and needs gate B.

## 1. Reproduce

- Before changing anything, reproduce the problem on the current default branch, and record the exact commands, versions and output.
- If you can't reproduce it, stop and report that. This finding is useful too, and it may become the contribution: "Can't reproduce on main at `abc123` with X, Y, Z."
- Narrow it down. Find the smallest case that shows the problem, and identify the cause instead of fixing the symptom. Check which versions are affected if that matters. The version matrix in OCF #377 is an example.

## 2. Understand the science

For any change that touches a scientific calculation, find out the correct behavior from a primary source. That could be the model's training data spec, a paper, a standard (units, CF conventions) or the upstream data provider's docs. Cite it in your notes.

If there is more than one reasonable fix, write them down as options. Evaluate them, recommend one, and explain why.

## 3. Fix

- Match the project's style, structure and testing conventions. Make the smallest change that fixes the cause properly.
- Don't refactor along the way. If you find another problem, write it down for a separate issue.
- Add tests, and check that each one **fails without the fix**. A test that passes either way proves nothing.

## 4. Validate

Match the evidence to the claim you are making:

| Claim | Evidence |
|---|---|
| "It no longer crashes" | A reproduction that fails before and passes after; the full test suite passes |
| "It's more correct" | Comparison against a reference: a known value, independent data or the spec |
| "Results improved" | A before/after metric on a fair evaluation, with uncertainty (e.g. a paired bootstrap CI) and the evaluation's limits stated |

Run the project's whole test suite, not only your new tests. Write down any failures that also happen without your change.

## 5. Write it up

Draft the issue or PR text with `templates/contribution.md`. Save the draft, your notes and the commands you ran in the candidate's ledger file, or link to them from there. Then go to phase 5.

## If you get stuck

If the problem is much larger than scored, needs expertise or data you don't have, or turns out to be someone else's bug upstream, stop. Report to the operator honestly and update the ledger. An upstream report or a well-documented "here's what I found" is a legitimate result, and often a valuable one.
