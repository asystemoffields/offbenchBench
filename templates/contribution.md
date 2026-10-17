# Contribution draft

Adapt this to the venue's own template, length limit and rules if it has them. Delete any section that doesn't apply. Two shapes are given: one for a result on an open problem or puzzle, one for a change to software or data.

---

## A. Result on an open problem or puzzle (comment, note, report or preprint)

### Statement

<The precise claim established, with definitions, in the same form as the problem's source. If it is a partial result, say exactly what part.>

### Verification

<What a reader can check without trusting us: the Lean file and `#print axioms` output; the counterexample and the script that checks it against the statement; the reproducible computation and its certificate; the sources with provenance and the inference chain. Links.>

### Argument

<The proof or reasoning, written out in full. For a long proof, a summary here and the full text linked.>

### Relation to known work

<What was searched and what was found. The closest prior results and how this differs. "We did not find this in the literature" is the strongest novelty claim to make.>

### Caveats

<Which steps are formalized and which are not. What the computation does not cover. Which inference rests on a single source. What remains open.>

<AI disclosure in the venue's form, specific about which steps the model did and who checked them. Example: "The argument was found with the assistance of an AI model; the proof was formalized in Lean and every step was checked by the author.">

---

## B. Change to software or data (issue or PR body)

<For a PR: "Fixes #N">

### Summary

<1–3 sentences: what was wrong, and what this changes.>

### Cause

<The root cause, with file and line references or upstream links.>

### Evidence

<Reproduction before and after; version matrix; before/after metrics with uncertainty; comparison against reference data. Prefer tables.>

### Options considered

<If more than one fix was reasonable: each option, its evidence, and why this one.>

### Testing

<New tests, and confirmation that they fail without the fix. Full suite result. Any failures that also occur on main.>

### Caveats and not in this change

<What wasn't tested, where the evaluation is weak, and related problems with links to separate issues.>

*(Investigated with help from an AI coding assistant.)*
