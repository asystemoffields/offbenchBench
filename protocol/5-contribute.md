# Phase 5: Contribute (gate B)

Goal: get the work to the maintainers in the form they find most useful, with the operator approving every public action.

## Before drafting

Read the project's `CONTRIBUTING`, code of conduct, PR and issue templates, and any AI-contribution policy. Check whether it needs a CLA or DCO sign-off. Re-check the issue thread, since someone may have started on it while you were working.

## Choose the right form

- **Comment on the existing issue** when you have findings but no fix yet, or when the project wants contributors to claim work or discuss an approach first.
- **A new issue** when you found a distinct problem. This applies to side findings from phase 4 too.
- **A PR** when the fix is ready and the project accepts PRs without prior discussion, or when that discussion has already happened.

When in doubt, comment first and offer the PR. Fixing a maintainer's problem their way beats a surprise PR fixing it yours.

## Gate B: show the exact action

Show the operator, word for word:

- the action, e.g. "fork `org/repo`", "open a PR from branch X to `main`" or "comment on #123"
- the full text that will be posted
- the diff, for a PR

Then wait for an explicit yes for **that** action. If they ask for edits, show the revised text again. Each public action needs its own approval: approving the PR text doesn't approve a follow-up comment.

Record the approval in the ledger (who, when, what), then do the action. Paste the resulting URL into the ledger and set `status: submitted`.

## Writing standards

- **Lead with the problem and the evidence**, then the change. Tables beat paragraphs for before/after comparisons.
- **Put caveats in plain sight.** State what you didn't test and where the evaluation is weak.
- **Keep it in scope.** Name related problems and point to separate issues for them.
- **Disclose AI involvement.** One line is fine, such as "Investigated with help from an AI coding assistant." Follow the project's format if it has one.
- **Write plainly.** Don't oversell, flatter the maintainers or pad.

## After submitting

Ask the operator to check back on the PR or issue, or check yourself in later sessions using the ledger. Respond to review promptly and politely, and get gate B approval for each reply. If the maintainers take a different direction, help with that direction. Final statuses are `merged`, `closed` (state why) or `abandoned` (state why). Write a short retrospective in the ledger: what worked, and what to do differently.
