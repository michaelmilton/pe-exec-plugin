# PE Executive Plugin

A Claude Code plugin that enables PE portfolio company executive reasoning.

## Project Structure

- `skills/pe-executive-mindset/SKILL.md` - Core skill definition with PE mental models, decision frameworks, and value creation levers
- `skills/pe-executive-mindset/references/` - Detailed reference material (incentives, governance, decision patterns, demographics, psychological experience)
- `commands/` - User-invocable commands (`pe-brainstorm`, `pe-review`, `pe-explain`)
- `docs/` - Archival research used to develop the plugin (not loaded at runtime)
- `pe-executive-guide.md` - Single-file deployment artifact for Claude Projects and ChatGPT

## Conventions

- This is a content-only plugin (markdown files, no code to build or test)
- Skill and command files use markdown with YAML frontmatter
- Reference files are plain markdown

## Update Strategy

The plugin has two distribution formats that must stay in sync:

- **Plugin format** (for Claude Code and Cowork): `SKILL.md` + `references/*.md` + `commands/*.md`
- **Single-file format** (for Claude Projects and ChatGPT): `pe-executive-guide.md`

When updating content, edit the plugin source files first (`skills/` and `commands/`), then regenerate `pe-executive-guide.md` by combining all source files into a single document. The guide follows the same structure: Part I maps to SKILL.md, Parts II-VI map to the five reference files, and the "How to Use This Guide" section at the top adapts the command instructions for non-plugin platforms.
