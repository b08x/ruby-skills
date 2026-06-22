```markdown
# ruby-skills Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns and workflows for the `ruby-skills` repository, a TypeScript codebase designed to manage and extend Ruby-related skills as plugins. It documents conventions for file structure, code style, and the processes for adding, updating, or removing skills and plugins. The guide is intended for contributors looking to maintain consistency and efficiency when working within this repository.

## Coding Conventions

**File Naming**
- Use **PascalCase** for file names.
  - Example: `SkillManager.ts`, `RubyParser.test.ts`

**Imports**
- Use **relative import paths**.
  - Example:
    ```typescript
    import { SkillManager } from './SkillManager';
    ```

**Exports**
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    export function addSkill(skill: Skill) { ... }
    export const SKILL_VERSION = '1.0.0';
    ```

**Commit Messages**
- Freeform, no strict prefixing.
- Average commit message length: ~53 characters.

## Workflows

### Add or Update Skill
**Trigger:** When introducing a new Ruby skill or updating an existing one.
**Command:** `/add-skill`

1. **Create or update** `SKILL.md` in `plugins/ruby-skills/skills/<skill-name>/`.
2. **Register the skill** by updating `plugins/ruby-skills/.claude-plugin/plugin.json`.
3. **Reflect the change** in `.claude-plugin/marketplace.json`.
4. **Document the skill** and its usage in `README.md` and `CLAUDE.md`.

**Example directory structure:**
```
plugins/ruby-skills/skills/
  └── MyNewSkill/
      └── SKILL.md
```

**Example plugin registration:**
```json
// plugins/ruby-skills/.claude-plugin/plugin.json
{
  "skills": [
    "MyNewSkill",
    ...
  ]
}
```

### Remove Plugin
**Trigger:** When deprecating or removing a plugin that is no longer needed.
**Command:** `/remove-plugin`

1. **Delete** the plugin directory and all its files (e.g., `plugins/<plugin-name>/`).
2. **Remove the plugin entry** from `.claude-plugin/marketplace.json`.
3. **Update or remove** related sections in `README.md` and `CLAUDE.md`.
4. **Update** `plugins/ruby-skills/.claude-plugin/plugin.json` if necessary.

**Example:**
```bash
rm -rf plugins/old-plugin/
```
Then remove all references to `old-plugin` in the relevant JSON and Markdown files.

## Testing Patterns

- **Test files** follow the pattern: `*.test.*`
  - Example: `SkillManager.test.ts`
- **Testing framework** is not explicitly specified; check existing test files for conventions.
- Place test files alongside or near the code they test.

**Example test file:**
```typescript
// SkillManager.test.ts
import { addSkill } from './SkillManager';

describe('addSkill', () => {
  it('should add a new skill', () => {
    // test implementation
  });
});
```

## Commands

| Command        | Purpose                                                        |
|----------------|----------------------------------------------------------------|
| /add-skill     | Add or update a Ruby skill, including documentation and metadata. |
| /remove-plugin | Remove an entire plugin and update all related configuration.     |
```
