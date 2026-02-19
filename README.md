# PE Executive Plugin

A decision-making model for understanding how private equity portfolio company executives think. This plugin is not a comprehensive PE operations manual — it focuses on the mental models, incentive structures, and behavioral patterns that drive executive decisions, so non-executives can understand, anticipate, and work effectively within PE-owned companies.

## What This Plugin Does

- **Brainstorm** deliverables and opportunities through a PE executive's decision framework
- **Review** work products the way a PE board member would evaluate them
- **Explain** PE executive behavior and decisions in plain language for non-executives

## What This Plugin Is Not

This is not an operational playbook for running a PE portfolio company. It does not cover technology strategy, sector-specific models, procurement frameworks, ESG compliance, or market dynamics. It covers how PE executives reason — what they prioritize, what they ignore, and why — grounded in the incentive structures, governance systems, and cultural forces that shape their thinking.

## Components

### Skill: pe-executive-mindset

Core mental model covering the four interlocking pressures that drive PE executive behavior: the exit clock, equity incentives, leverage constraints, and the replacement threat.

Reference material in five areas:

- **Incentive structures** — Compensation mechanics, equity design, hurdle rates, case studies (Petco, SolarWinds, Toys R Us)
- **Governance and monitoring** — Board dynamics, reporting cadence, VCP structure, KPI cascades, adjusted EBITDA and quality of earnings
- **Decision patterns** — Exit clock, leverage effects, buy-and-build, deal-type variation (buyout, growth, distressed, carve-out), motivation dynamics across the deal lifecycle
- **Demographics and culture** — Selection patterns, network effects, cultural norms, shareholder primacy origins, psychological selection effects, key academic works
- **Psychological experience** — Coping patterns, moral injury, moral disengagement, cognitive dissonance, emotional labor, ethical fading, practical resources

### Commands

- `/pe-brainstorm [topic or file]` — Generate deliverables and opportunities from a PE executive perspective. Accepts a topic, a file path for company-specific context, or both.

- `/pe-review [file]` — Review a deliverable through a PE executive's lens. Evaluates strategic alignment, metrics, timeline, and rigor. Provides a direct board-readiness assessment.

- `/pe-explain [decision or concept]` — Explain PE executive decisions and concepts in plain language for non-executives. Connects behavior to structural forces and provides actionable implications.

## Repository Structure

- **skills/** — The core knowledge base (SKILL.md and reference files)
- **commands/** — The three slash commands
- **docs/** — Archive of the source research that informed the plugin. These files are not loaded by the plugin at runtime; they are preserved here for provenance and future reference.

## Deployment

### Claude Code

Install as a plugin:

```
claude plugin install /path/to/pe-executive.plugin
```

Or clone this repo and install from the directory:

```
claude plugin install /path/to/this/repo
```

Once installed, the skill loads automatically when relevant topics come up, and the three commands (`/pe-brainstorm`, `/pe-review`, `/pe-explain`) are available.

### Cowork

Install the `.plugin` file through the Cowork plugin manager. The commands and skill will appear in your session automatically.

### Plain Claude (claude.ai) or ChatGPT

These platforms don't support plugins directly. To use the knowledge base:

1. Create a new Project (Claude) or GPT (ChatGPT)
2. Upload the contents of `skills/pe-executive-mindset/SKILL.md` as project knowledge or custom instructions
3. For deeper context, also upload the five files from `skills/pe-executive-mindset/references/`
4. Optionally paste the contents of the command files (`commands/pe-brainstorm.md`, `commands/pe-review.md`, `commands/pe-explain.md`) into the system instructions to replicate the slash command behavior

The commands won't work as `/slash-commands` on these platforms, but you can achieve the same results by asking directly (e.g., "Brainstorm a 100-day plan for a SaaS acquisition from a PE executive perspective").

## Examples

- `/pe-brainstorm 100-day plan for a SaaS acquisition`
- `/pe-review @board-deck.md`
- `/pe-explain Why is our new CEO replacing the entire leadership team?`
- "How would a PE executive prioritize these three initiatives?"
- "What would a PE board want to see in this quarterly update?"
