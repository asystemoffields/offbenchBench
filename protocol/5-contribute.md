# Phase 5: Contribute (gate B)

Goal: get the result to the people who care about the problem, in the form they find most useful, with the operator approving every public action.

## Before drafting

Read the venue's rules: `CONTRIBUTING`, code of conduct, PR and issue templates, forum rules, data-use terms and any AI-contribution policy. Check whether it needs a CLA, DCO sign-off, or human verification of AI-assisted content. Re-check the problem's page or thread, since someone may have posted a result while you were working.

Rules change. The ones below were current when this file was written; check the live page before relying on them.

- **erdosproblems.com.** Its forum policy, as quoted in December 2025, permits comments prepared with AI assistance provided (a) this is disclosed, (b) the contents, including mathematics, code, numerical data and the existence of cited sources, have been carefully checked by the user themselves without AI assistance, and (c) the comment is not unreasonably long. In October 2026 the site announced it would record results without credit-giving language, and that submissions misrepresenting AI use may be declined. Write plainly, disclose exactly, and have the operator verify every claim before posting.
- **Formal Conjectures (google-deepmind/formal-conjectures).** A statement repository. It does not take informal proofs of open problems. Long formal proofs live elsewhere and are linked with the `formal_proof` attribute; its `PROOFS.md` asks that the linked declaration be checked with `#print axioms`. Fixes to misformalized statements are welcome.
- **OEIS.** Has its own editorial process and contributor rules. Read them before touching an entry.
- **MathOverflow and other Stack Exchange sites.** Their policies on AI-generated content have changed more than once. Check the current meta before posting, and if posting is allowed, the operator writes and owns the post.
- **Zooniverse and other crowdsourced projects.** Each project has a science team and a talk board. Tooling for volunteers usually goes to the team first, not the volunteers. Classifications are theirs to accept; don't bulk-submit model output as if it were volunteer work.
- **arXiv.** Needs an author with posting rights, often an endorsement, and an honest statement of AI involvement. The operator is the author. A preprint is for a result that is complete and verified, not a sketch.
- **The problem's proposer, an archive, a museum, a survey team.** For a question posed in a paper, or a finding about a physical thing, an email with the result and the verification artifact is often the right first move. It is a public action under gate B.

## Choose the right form

- **Comment on the problem's page or thread** when you have a verified result or verified partial progress, and the venue records results that way.
- **A formalization PR** when the result is a Lean proof and the venue or a formal library collects them.
- **A note or preprint** when the result is complete, verified and too long for a comment. Operator-authored.
- **A report to the people who would act** when the result is empirical: what you found, how sure you are, what they'd need to confirm it.
- **Comment on the existing issue** (software) when you have findings but no fix, or when the project wants discussion first.
- **A new issue** for a distinct problem, including side findings.
- **A PR** when the fix is ready and the project accepts PRs without prior discussion, or when that discussion has already happened.
- **Just push it**, for routine work on the operator's own project with both gates recorded.

When in doubt, post less and offer more. A short verified comment that offers the full write-up beats a long post nobody asked for.

## Gate B: show the exact action

Show the operator, word for word:

- the action, e.g. "post a comment on erdosproblems.com problem #N", "fork `org/repo`", "open a PR from branch X to `main`", "email <name> at <address>"
- the full text that will be posted
- the diff, for a PR; the Lean file and `#print axioms` output, for a formalization; the verification script and its output, for a counterexample or computation; the measurement table, for a performance claim

Then wait for an explicit yes for **that** action. If they ask for edits, show the revised text again. Each public action needs its own approval: approving a comment doesn't approve a follow-up reply.

For a high-stakes result, the operator confirms at this gate that they have checked the mathematics, code or evidence themselves, not just the prose. If they can't, the result isn't ready for that venue. The options are a venue where that isn't required, a collaborator who can check, or more verification work.

Record the approval in the ledger (who, when, what), then do the action. Paste the resulting URL into the ledger and set `status: submitted`.

## Writing standards

- **Lead with the statement, then the result, then the evidence.** For a proof: the precise claim, the verification artifact, then the argument. For a fix: the problem and the evidence, then the change. For a finding: the claim, the confidence, the evidence. Tables beat paragraphs for comparisons.
- **State novelty carefully.** Say what you searched and what you found. "We did not find this in the literature; the closest result is X" is the right register. Never "solved" or "resolved" unless the venue has accepted it as such.
- **Put caveats in plain sight.** Which steps are formalized and which aren't, what the computation doesn't cover, what wasn't tested, which source the inference hangs on.
- **Keep it in scope.** Name related problems and point to separate threads for them.
- **Disclose AI involvement** in the venue's form, honestly and specifically: which parts were model-generated, which were checked by whom. One line is often enough; a misleading line is never acceptable.
- **Write plainly.** No credit-claiming, no hype, no flattery, no padding. Length limits are real on forums.

## After submitting

Ask the operator to check back, or check yourself in later sessions using the ledger. Respond to questions and criticism promptly and politely, and get gate B approval for each reply. If a reviewer finds a gap, say so plainly in the thread and either fix it or withdraw the claim. If the community takes a different direction, help with that direction.

Final statuses: `resolved` (the venue accepted the result as settling the problem), `partial` (a checked partial result is recorded; the problem stays open), `merged`, `closed` (state why) or `abandoned` (state why). Write a short retrospective in the ledger: what worked, what the budget bought, and what to do differently.
