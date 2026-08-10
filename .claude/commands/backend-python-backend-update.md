---
name: backend-python-backend-update
description: Workflow command scaffold for backend-python-backend-update in LocalAI--.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /backend-python-backend-update

Use this workflow when working on **backend-python-backend-update** in `LocalAI--`.

## Goal

Update or refactor logic in multiple backend/python/*/backend.py files, often to change a common pattern or configuration across several backends.

## Common Files

- `backend/python/*/backend.py`
- `backend/python/*/requirements-*.txt`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify the pattern or configuration to be changed across backends.
- Edit backend.py files in each relevant backend/python/*/ directory to apply the change.
- Optionally update related requirements-*.txt files if dependencies are affected.
- Document or reference the change in the commit message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.