---
name: documentation-update-with-scripted-content
description: Workflow command scaffold for documentation-update-with-scripted-content in notte.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /documentation-update-with-scripted-content

Use this workflow when working on **documentation-update-with-scripted-content** in `notte`.

## Goal

Updates documentation, often regenerating or inlining content using scripts, and updates SDK reference and example/test files.

## Common Files

- `docs/src/**/*.mdx`
- `docs/src/scripts/**/*.py`
- `docs/src/sdk-reference/**/*.mdx`
- `docs/src/testers/**/*.py`
- `docs/src/snippets/**/*.mdx`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Modify or add documentation files in docs/src/
- Run or update scripts in docs/src/scripts/ to generate or inline content
- Update SDK reference files in docs/src/sdk-reference/
- Update example or tester files in docs/src/testers/ or docs/src/snippets/

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.