# PE Executive Plugin

Reason like a private equity portfolio company executive. This plugin gives Claude deep knowledge of PE incentive structures, governance systems, decision-making patterns, and cultural dynamics — enabling it to brainstorm deliverables, review work products, and explain PE thinking to non-executives.

## Components

### Skill: pe-executive-mindset

Core knowledge base covering:

- How PE executives think (incentive-driven decision framework)
- Value creation levers (revenue growth, margin expansion, buy-and-build, working capital, management upgrade)
- Governance context (board dynamics, reporting cadence, VCP structure)
- Key metrics (EBITDA, FCF, MOIC, IRR, Rule of 40)
- The 100-day playbook

Detailed reference material in four areas:

- Incentive structures (compensation mechanics, equity design, hurdle rates)
- Governance and monitoring (board authority, reporting, KPI cascades)
- Decision patterns (exit clock, leverage effects, growth vs. extraction)
- Demographics and culture (selection patterns, network effects, cultural norms)

### Commands

- `/pe-brainstorm [topic or file]` — Generate deliverables and opportunities from a PE executive perspective. Accepts a topic, a file path for company-specific context, or both.

- `/pe-review [file]` — Review a deliverable through a PE executive's lens. Evaluates strategic alignment, metrics, timeline, and rigor. Provides a direct board-readiness assessment.

- `/pe-explain [decision or concept]` — Explain PE executive decisions and concepts in plain language for non-executives. Connects behavior to structural forces and provides actionable implications.

## Usage

Install the plugin, then use the commands or ask questions that reference PE executive thinking. The skill loads automatically when relevant topics come up.

Examples:

- `/pe-brainstorm 100-day plan for a SaaS acquisition`
- `/pe-review @board-deck.md`
- `/pe-explain Why is our new CEO replacing the entire leadership team?`
- "How would a PE executive prioritize these three initiatives?"
- "What would a PE board want to see in this quarterly update?"
