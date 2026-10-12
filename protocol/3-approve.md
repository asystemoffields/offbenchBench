# Phase 3: Approve (gate A)

Goal: the operator chooses what to work on, and the decision is recorded.

## Present the brief

Use `templates/approval-brief.md`. Keep it short enough for the operator to read in two minutes. For each proposed candidate, include:

- a one-line summary and a link
- why it matters scientifically, in plain language
- score and main risks
- an estimated effort size (S, M or L) and what the operator will need to review
- what "done" would look like, and how it would be verified

Finish with your recommendation and the reason for it.

## Get an explicit decision

Ask the operator to approve, reject or defer each candidate. Only a clear choice counts as approval, such as "go with #2" or "approved: ocf-quartz-377". If the answer is ambiguous, ask again.

Approval at this gate covers **local work only**: reading, reproducing, prototyping and writing code on the operator's machine. It does **not** cover anything public. That needs gate B in phase 5.

## Record it

In each candidate's ledger file:

- Set `status` to `approved`, `rejected` or `deferred`.
- Fill in `approved_by` (whatever name the operator gives) and `approved_on`.
- Write the operator's reason in the log if they gave one. Rejection reasons improve future rankings.

Work on one approved candidate at a time unless the operator explicitly says otherwise.
