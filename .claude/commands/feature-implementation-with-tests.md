---
name: feature-implementation-with-tests
description: Workflow command scaffold for feature-implementation-with-tests in notte.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-implementation-with-tests

Use this workflow when working on **feature-implementation-with-tests** in `notte`.

## Goal

Implements a new feature or fixes a bug in the core or SDK, and adds/updates corresponding tests.

## Common Files

- `packages/notte-*/src/notte_*/**/*.py`
- `tests/**/*.py`
- `docs/src/testers/**/*.py`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Modify or add implementation files in packages/notte-* (e.g., notte-core, notte-sdk, notte-browser)
- Update or add corresponding test files in tests/ or docs/src/testers/

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.