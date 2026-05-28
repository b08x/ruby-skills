---
name: remove-plugin
description: Workflow command scaffold for remove-plugin in ruby-skills.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /remove-plugin

Use this workflow when working on **remove-plugin** in `ruby-skills`.

## Goal

Removes an entire plugin and updates all relevant configuration and documentation to reflect the change.

## Common Files

- `plugins/<plugin-name>/**`
- `.claude-plugin/marketplace.json`
- `README.md`
- `CLAUDE.md`
- `plugins/ruby-skills/.claude-plugin/plugin.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Delete the plugin directory and all its files
- Remove the plugin entry from .claude-plugin/marketplace.json
- Update or remove related sections in README.md and CLAUDE.md
- Update plugins/ruby-skills/.claude-plugin/plugin.json if necessary

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.