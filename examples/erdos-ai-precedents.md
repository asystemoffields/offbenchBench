# Precedents: AI attempts at Erdős problems

This is not a contribution of ours. It is a short case file of public AI attempts at problems on erdosproblems.com, kept here because they show, better than any rubric, what separates a result from a claim. It applies to every high-stakes attempt, not only in mathematics.

Dates and details below come from the linked pages and from secondary coverage, as read in October 2026. Check the primary sources before citing any of it, and check the live site rules before posting there: they have changed more than once.

## The site

erdosproblems.com, run by Thomas Bloom, catalogues problems posed by Paul Erdős, each with a status, references and a forum thread. Until mid-2026 a companion wiki (github.com/teorth/erdosproblems/wiki) maintained by Terence Tao tracked AI contributions. The wiki sorted them into: AI standalone; AI alongside literature (a matching paper found afterwards); AI building on literature; AI collaborating with humans; and secondary contributions such as literature search, formalization, rewriting and computation. Each was marked full resolution, partial progress, incorrect, or unverified, and whether a Lean formalization existed. Its own disclaimers are worth keeping: "Many problems on the site lack a thorough literature review," and "Absence of past progress may reflect obscurity rather than difficulty." The wiki says it is no longer updated, with data as of 30 June 2026.

## Case 1: "GPT-5 solved ten Erdős problems" (October 2025)

Researchers at OpenAI posted that GPT-5 had found solutions to ten problems the site listed as open. Bloom replied that the posts were "seriously inconsistent with the facts": the model had found existing papers, and "open" on the site meant only that he was not personally aware of a solution. The posts were deleted, and one of the researchers acknowledged the model "only found solutions already in the literature".

What the protocol takes from it: rule 3 in `AGENTS.md`. A list's status is a statement about the list maintainer's knowledge. Literature search is real and useful work, and the wiki recorded it as such, but it has to be described as what it is.

## Case 2: problem #1026 (December 2025)

Tao wrote up the sequence of events around problem #1026 on his blog ("The story of Erdős problem #1026", 8 December 2025). That post is where the forum's AI policy was quoted: comments prepared with AI assistance are permitted provided this is disclosed, the contents (including mathematics, code, numerical data and the existence of cited sources) have been carefully checked by the user themselves without AI assistance, and the comment is not unreasonably long. Read the post for the full account of how a model's output became an accepted entry and where the human checking happened.

What the protocol takes from it: the venue's rules are specific, and "checked by the user themselves" is the operator's job at gate B, not the model's.

## Case 3: problem #728 (January 2026)

A proof produced by Harmonic's Aristotle system, working in Lean, from an informal argument by GPT-5.2 Pro, was written up as a preprint (arXiv:2601.07421, "Resolution of Erdős Problem #728: a writeup of Aristotle's Lean proof"). Anyone with a Lean toolchain can check the result, which is why it could be accepted quickly.

What the protocol takes from it: rule 4. The formal proof is the artifact. The write-up exists so that humans can understand it; acceptance rests on the kernel.

## Case 4: AlphaProof Nexus (2026)

Google DeepMind reported a system that attempted 353 open Erdős problems and resolved 9 of them, with Lean proofs published in a public repository (github.com/google-deepmind/alphaproof-nexus-results), along with 44 OEIS conjectures (preprint arXiv:2605.22763). Secondary coverage described the preprint as not yet independently validated at the time.

What the protocol takes from it: the base rate. A strong, specialized system with a large budget resolved a few percent of what it attempted. Expect most attempts to end in section 6 of `protocol/4-solve.md`, and make sure what comes out of them is still useful.

## The site's direction (October 2026)

In a guest post on Tao's blog ("Changes to the Erdős problems web site", 6 October 2026), Bloom wrote that the site would keep recording results but stop using credit-giving language for them, human or AI; that papers should acknowledge their sources and honestly disclose how AI was used; and that submissions misrepresenting AI use may be declined. He noted that most comments the site now receives announce AI-generated proofs. The forum thread "AI Contributions 3" points to guidelines from the IAS Advisory Group on Mathematics and Artificial Intelligence (AGMAI) on the responsible release of AI-generated mathematics.

What the protocol takes from it: the community's scarce resource is verification time, not ideas. Post less, check more, claim nothing.

## Sources

- erdosproblems.com, and its forum threads "AI Contributions", "AI Contributions 2" and "AI Contributions 3"
- github.com/teorth/erdosproblems/wiki/AI-contributions-to-Erdős-problems
- terrytao.wordpress.com: "The story of Erdős problem #1026" (8 December 2025); "Changes to the Erdős problems web site" (6 October 2026, guest post by Thomas Bloom)
- arxiv.org/abs/2601.07421; arxiv.org/abs/2605.22763
- github.com/google-deepmind/formal-conjectures; github.com/google-deepmind/alphaproof-nexus-results
- Press coverage of the October 2025 retraction, e.g. the-decoder.com, "Leading OpenAI researcher announced a GPT-5 math breakthrough that never happened"
