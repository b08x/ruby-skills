---
name: add-or-update-skill
description: Workflow command scaffold for add-or-update-skill in ruby-skills.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-or-update-skill

Use this workflow when working on **add-or-update-skill** in `ruby-skills`.

## Goal

Adds a new skill or updates an existing skill in the ruby-skills plugin, including documentation and marketplace metadata.

## Common Files

- `plugins/ruby-skills/skills/*/SKILL.md`
- `plugins/ruby-skills/.claude-plugin/plugin.json`
- `.claude-plugin/marketplace.json`
- `README.md`
- `CLAUDE.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create or update SKILL.md in plugins/ruby-skills/skills/<skill-name>/
- Update plugins/ruby-skills/.claude-plugin/plugin.json to register the skill
- Update .claude-plugin/marketplace.json to reflect the new or changed skill
- Update README.md and CLAUDE.md to document the skill and its usage

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.