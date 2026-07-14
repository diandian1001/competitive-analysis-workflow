# Competitive Analysis Workflow V3.0

[中文版](README_zh.md)

An **evidence-based competitive analysis skill for AI agents**. It starts from a business decision and guides competitor screening, evidence collection, framework selection, opportunity evaluation, and prioritized recommendations.

> V3.0 replaces rigid step-by-step prompting with evidence governance, decision criteria, and platform-aware execution.

## Core capabilities

- Three modes: quick judgment, standard analysis, deep research
- Candidate-pool screening before selecting core competitors
- A/B/C/D evidence confidence levels
- Separation of facts, inferences, open questions, and recommendations
- Functional matrix, user journey, value curve, SWOT/TOWS
- Opportunity evaluation across user value, strategic fit, cost, timing, and risk
- Platform guidance for ChatGPT, Claude, and Hermes
- Quality checks against stale data, home-team bias, false precision, and feature copying

## Workflow

```text
Define the decision
→ Build a candidate pool
→ Select core competitors
→ Collect and grade evidence
→ Choose analysis frameworks
→ Identify patterns
→ Evaluate opportunities
→ Prioritize actions
→ Run quality checks
```

## Usage

Provide `SKILL.md` or the repository to an AI agent and state the business decision, scope, and audience.

Platform notes:

- ChatGPT: `skills/chatgpt.md`
- Claude: `skills/claude.md`
- Hermes: `skills/hermes.md`

The core skill is tool-agnostic. If a platform lacks browsing, file analysis, code execution, or agent orchestration, it must state the limitation and narrow its conclusions.

## Repository structure

```text
.
├── SKILL.md
├── skills/
├── references/
├── templates/
├── examples/
├── CHANGELOG.md
├── LICENSE
├── README.md
└── README_zh.md
```

## License

MIT
