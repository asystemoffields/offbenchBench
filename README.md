# offbenchBench

**Real science problems, not benchmarks.**

offbenchBench is a protocol that lets any frontier model, working with a human, find open problems in real science where help is wanted, pick the one where it can do the most good, and then actually solve it. The test is whether maintainers merge the work and the science gets better.

It is plain Markdown, so there's nothing to install and it isn't tied to one lab's model or tooling.

## Quick start

Open this repo with any capable model that has web access and a shell (Claude Code, Codex, Gemini CLI, Cursor and so on) and say:

> Read `AGENTS.md` and run offbenchBench with me.

The model will:

1. **Discover** open problems in community science, research groups and government or national scientific efforts.
2. **Evaluate** them against a rubric that weighs scientific impact, whether help is wanted, maintainer responsiveness, feasibility and whether success can be checked objectively.
3. **Ask for your approval** before doing any real work.
4. **Solve** the chosen problem: reproduce it, find the cause, fix it and validate the fix with real evidence.
5. **Ask again** and show you the exact text before posting anything publicly.

Progress is saved in `ledger/`, so you can stop and resume, or switch models partway through.

## What's in scope

Open or community science projects, research software, and government or national efforts in areas like climate, weather, energy, Earth observation, astronomy, life sciences and chemistry, wherever code can help. Competitions, leaderboards and hackathons are out of scope. See `AGENTS.md` for the full definition.

## Principles

- A human approves the work, and approves again before anything is posted publicly.
- Claims come with evidence, and caveats are stated plainly.
- AI involvement is always disclosed.
- Maintainer time is the scarcest resource, so contributions are small, in scope and one at a time.

See [`examples/ocf-quartz-nwp-units.md`](examples/ocf-quartz-nwp-units.md) for a real contribution traced through every phase.

## Layout

```
AGENTS.md        entry point for any model
SKILL.md         Claude Agent Skill wrapper
protocol/        the five phases
sources.md       where to look
templates/       candidate card, approval brief, contribution draft
ledger/          your candidates and their status
examples/        worked examples
```

## Contributing

New sources, rubric improvements and worked examples are welcome. Please open an issue or PR.

## License

MIT
