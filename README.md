# offbenchBench

**Real problems, not benchmarks.**

offbenchBench is a protocol that lets any frontier model, working with a human, take on real work that nobody has written a grader for, and do it to a standard the people who care about the problem would accept. The work can be anything from a performance fix in a hobby game to a crowdsourced-science pipeline to an open conjecture. The protocol is the same shape at every level; what scales with the stakes is how much verification it demands.

It is plain Markdown, so there's nothing to install and it isn't tied to one lab's model or tooling.

## Quick start

Open this repo with any capable model that has web access and a shell (Claude Code, Codex, Gemini CLI, Cursor and so on) and say either:

> Read `AGENTS.md` and run offbenchBench with me.

or, if you already have a problem:

> Read `AGENTS.md`. I've got a problem for you: <describe it>.

The model will:

1. **Discover** candidate problems, or take the one you brought.
2. **Evaluate** them: set the stakes tier, spend a bounded reconnaissance actually trying each shortlisted one, and score what it found. Feasibility is measured, not guessed.
3. **Ask for your approval** and a budget before doing real work.
4. **Solve** the chosen problem: pin the statement down, check what is known, attack it, and verify the result to a standard a stranger could check.
5. **Ask again** and show you the exact text before posting anything publicly.

Progress is saved in `ledger/`, so you can stop and resume, or switch models partway through.

## What's in scope

Anything real, that code, computation, analysis or proof can move, and where the work is welcome. That covers open problems in mathematics and science, research and community software, crowdsourced and citizen-science projects, empirical puzzles with open data, and the operator's own projects. It does not cover work that requires deceiving anyone, and when the model goes looking on its own it skips competitions and bounties. See `AGENTS.md` for the full definition and the stakes tiers.

## Principles

- Aim at the problem where a result would matter most, not the one most likely to go smoothly.
- A human approves the work, and approves again before anything is posted publicly.
- Novelty is checked against the literature, never assumed from a list's "open" status.
- Every claim comes with the artifact that lets a stranger check it: a formal proof, a certificate, a failing test, a measurement with its method.
- Caveats are stated plainly, and AI involvement is always disclosed.
- Other people's time is the scarcest resource, so contributions are in scope, one at a time, and no longer than they need to be.

Two worked references: [`examples/ocf-quartz-nwp-units.md`](examples/ocf-quartz-nwp-units.md), a real software contribution traced through every phase, and [`examples/erdos-ai-precedents.md`](examples/erdos-ai-precedents.md), what public AI attempts at Erdős problems have taught about high-stakes claims.

## Layout

```
AGENTS.md        entry point for any model: scope, stakes tiers, the rules
SKILL.md         Claude Agent Skill wrapper
protocol/        the five phases
sources.md       where to look
templates/       candidate card, approval brief, contribution draft
ledger/          your candidates and their status
examples/        worked examples and precedents
```

## Contributing

New sources, rubric improvements, precedents and worked examples are welcome. Please open an issue or PR.

## License

MIT
