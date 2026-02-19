# PE Executive Plugin

A Claude Code plugin that enables PE portfolio company executive reasoning.

## Project Structure

- `.claude-plugin/plugin.json` - Plugin manifest (name, version, description)
- `skills/pe-executive-mindset/SKILL.md` - Core skill definition with PE mental models, decision frameworks, and value creation levers
- `skills/pe-executive-mindset/references/` - Detailed reference material (incentives, governance, decision patterns, demographics, psychological experience)
- `commands/` - User-invocable commands (`pe-brainstorm`, `pe-review`, `pe-explain`)
- `docs/` - Archival research used to develop the plugin

## Conventions

- This is a content-only plugin (markdown files, no code to build or test)
- The `.plugin` build artifact is gitignored; build it with the plugin packaging tool when needed
- Skill and command files use markdown with YAML frontmatter
- Reference files are plain markdown
