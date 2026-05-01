# ECC for Codex CLI

This supplements the root `AGENTS.md` with a repo-local ECC baseline.

## Repo Skill

- Repo-generated Codex skill: `.agents/skills/LocalAI--/SKILL.md`
- Claude-facing companion skill: `.claude/skills/LocalAI--/SKILL.md`
- Keep user-specific credentials and private MCPs in `~/.codex/config.toml`, not in this repo.

## MCP Baseline

Treat `.codex/config.toml` as the default ECC-safe baseline for work in this repository.
The generated baseline enables GitHub, Context7, Exa, Memory, Playwright, and Sequential Thinking.

## Multi-Agent Support

- Explorer: read-only evidence gathering
- Reviewer: correctness, security, and regression review
- Docs researcher: API and release-note verification

## Workflow Files

- `.claude/commands/backend-python-backend-update.md`
- `.claude/commands/gallery-model-metadata-update.md`
- `.claude/commands/importer-logic-and-test-update.md`

Use these workflow files as reusable task scaffolds when the detected repository workflows recur.