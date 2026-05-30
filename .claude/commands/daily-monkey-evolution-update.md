---
name: daily-monkey-evolution-update
description: Workflow command scaffold for daily-monkey-evolution-update in forkMonkey.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /daily-monkey-evolution-update

Use this workflow when working on **daily-monkey-evolution-update** in `forkMonkey`.

## Goal

Updates the monkey's daily evolution by modifying data files and generating a new SVG representing the monkey's current state.

## Common Files

- `README.md`
- `monkey_data/history.json`
- `monkey_data/stats.json`
- `monkey_data/dna.json`
- `monkey_data/monkey.svg`
- `monkey_evolution/YYYY-MM-DD_HH-MM_monkey.svg`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update README.md with the latest evolution info or stats.
- Update monkey_data/history.json with new historical data.
- Update monkey_data/stats.json with new statistics.
- Optionally update monkey_data/dna.json and monkey_data/monkey.svg if there are genetic or visual changes.
- Generate a new SVG in monkey_evolution/ with the current date and time.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.