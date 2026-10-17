# Phase 3: Approve (gate A)

Goal: the operator chooses what to work on, and the decision is recorded.

## Present the brief

Use `templates/approval-brief.md`. Keep it short enough to read in two minutes. For each proposed candidate, include:

- a one-line statement of the problem, its tier, and a link
- what changes if it is resolved, in plain language
- score, with the traction evidence from reconnaissance and the named obstacle
- an effort size (S, M, L or XL) and what a bounded attempt would cost
- what "done" would look like, and how it would be verified
- the fallback result if the full problem doesn't fall: a special case, a counterexample to a stronger form, a formalization, a reproduction report, a narrowed search
- what the operator will need to check themselves before anything goes public

Finish with your recommendation and the reason for it. If you are recommending a harder problem over an easier one, say why its stakes justify it.

For a dispatched problem, the brief is one entry: tier, verification plan, effort, and anything you found in reconnaissance that the operator should know before committing (it's already solved, it's bigger than it looked, the venue has rules).

## Get an explicit decision

Ask the operator to approve, reject or defer each candidate. Only a clear choice counts as approval, such as "go with #2" or "approved: erdos-123". If the answer is ambiguous, ask again.

Agree a **budget** for any standard or high-stakes attempt: how much effort goes in before you report back regardless of outcome. Work on an open problem can absorb unlimited effort, so the budget is what keeps it honest. The operator can extend it when you report.

Approval at this gate covers **local work only**: reading, reproducing, prototyping, computing, proving and writing on the operator's machine. It does **not** cover anything public. That needs gate B in phase 5. The one exception is routine work on the operator's own project, where they may give both gates in one explicit message. Record that it was explicit.

## Record it

In each candidate's ledger file:

- Set `status` to `approved`, `rejected` or `deferred`.
- Fill in `approved_by` (whatever name the operator gives), `approved_on` and `budget`.
- Write the operator's reason in the log if they gave one. Rejection reasons improve future rankings.

Work on one approved candidate at a time unless the operator explicitly says otherwise.
