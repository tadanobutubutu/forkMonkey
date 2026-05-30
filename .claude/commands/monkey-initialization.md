---
name: monkey-initialization
description: Workflow command scaffold for monkey-initialization in forkMonkey.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /monkey-initialization

Use this workflow when working on **monkey-initialization** in `forkMonkey`.

## Goal

Initializes a new monkey by creating all relevant data and SVG files.

## Common Files

- `README.md`
- `monkey_data/dna.json`
- `monkey_data/history.json`
- `monkey_data/monkey.svg`
- `monkey_data/stats.json`
- `monkey_evolution/YYYY-MM-DD_HH-MM_monkey.svg`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create or reset README.md with initial information.
- Create monkey_data/dna.json with starting DNA.
- Create monkey_data/history.json with initial history.
- Create monkey_data/monkey.svg with the initial monkey image.
- Create monkey_data/stats.json with initial stats.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.