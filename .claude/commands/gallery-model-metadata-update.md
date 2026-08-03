---
name: gallery-model-metadata-update
description: Workflow command scaffold for gallery-model-metadata-update in LocalAI--.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /gallery-model-metadata-update

Use this workflow when working on **gallery-model-metadata-update** in `LocalAI--`.

## Goal

Add or update model metadata, tags, or entries in the gallery by editing index.yaml.

## Common Files

- `gallery/index.yaml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit gallery/index.yaml to add or update model entries or tags.
- Include detailed descriptions and file references as needed.
- Commit with a message referencing the models and changes.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.