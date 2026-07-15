# Competitive Analysis Workflow V3.0

**Evidence-Driven Competitive Analysis Skill for AI Agents**

[中文版](README_zh.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-7c5cfc.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/diandian1001/competitive-analysis-workflow?style=social)](https://github.com/diandian1001/competitive-analysis-workflow)
[![Version](https://img.shields.io/badge/Version-V3.0-10b981.svg)](https://github.com/diandian1001/competitive-analysis-workflow)

Give this repo to any AI agent (ChatGPT, Claude, Hermes), tell it your business decision, and it will guide evidence-driven competitor screening, analysis, opportunity evaluation, and prioritized recommendations.

> **V3.0** replaces rigid step-by-step prompting with evidence governance, decision criteria, and platform-aware execution.

---

## 30-Second Example

> ⚠️ **以下为结构示意，不代表实际竞品调研结论。** 展示使用该 Workflow 时可以产出什么结构的分析。

**Business question:**
> *"Our service-oriented WeChat Official Account is transitioning. Which operational mechanisms should we keep to sustain user return visits?"*

**What the workflow produces:**

| Output | Structure (illustrative) |
|--------|--------------------------|
| **Core judgment** | [Based on evidence evaluation — filled after actual analysis] |
| **Core competitors** | Candidate pool → screened to core competitors with documented selection rationale |
| **Key facts** | 【事实·A】Competitor official page confirms check-in feature exists 【事实·B】Direct product testing confirms check-in accessible within 1 tap 【推断·D】Check-in may serve as a return trigger, but lacks usage data to verify contribution rate 【待验证】Actual return-visit rate and reward cost for check-in users |
| **Evidence grades** | Grade distribution depends on available sources — see [Evidence Rubric](references/evidence-rubric.md) |
| **Open questions** | 【待验证】Would users return for "usage reports" without explicit push notifications? 【待验证】Is check-in stickiness transferable across industries? |
| **Recommendations** | **P0/P1/P2** prioritized by evidence strength, user value, and strategic fit — specific actions filled after analysis |

→ [Full example](examples/终端方向竞品分析.md) | [Quick analysis example](examples/quick-analysis-example.md)

---

## Core Capabilities

- Three modes: quick judgment, standard analysis, deep research
- Candidate-pool screening before selecting core competitors
- A/B/C/D evidence confidence levels (see [Evidence Rubric](references/evidence-rubric.md))
- Separation of facts, inferences, open questions, and recommendations
- Functional matrix, user journey, value curve, SWOT/TOWS
- Opportunity evaluation across user value, strategic fit, cost, timing, and risk
- Platform guidance for ChatGPT, Claude, and Hermes
- Quality checks against stale data, home-team bias, false precision, and feature copying

---

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

---

## Usage

### Option 1: With an AI Agent (Recommended)

Provide `SKILL.md` or the repository URL to an AI agent and state your business decision:

```text
Use this Skill to analyze [your topic].
The goal is to support [decision], prioritizing [key concerns].
```

### Option 2: Platform-Specific

- **ChatGPT**: Use `skills/chatgpt.md` as Custom Instructions or paste it directly
- **Claude**: Use `skills/claude.md` as Project Knowledge
- **Hermes**: Use `skills/hermes.md` as a Skill file

### Option 3: Manual

Open `SKILL.md` and follow the phases manually. Use `templates/` for structured note-taking.

The core skill is tool-agnostic. If a platform lacks browsing, file analysis, code execution, or agent orchestration, it must state the limitation and narrow its conclusions.

---

## Repository Structure

```
.
├── SKILL.md                     ← Core skill (V3.0)
├── README.md                    ← This file (English)
├── README_zh.md                 ← Chinese documentation
├── CHANGELOG.md
├── LICENSE
├── skills/                      ← Platform-specific adaptations
│   ├── chatgpt.md
│   ├── claude.md
│   └── hermes.md
├── references/                  ← Detailed methodology
│   ├── competitor-selection.md
│   ├── evidence-rubric.md
│   ├── analysis-frameworks.md
│   └── quality-checklist.md
├── templates/                   ← Reusable templates
│   ├── 分析目标卡.md             ← Analysis scoping card
│   ├── 竞品档案卡.md             ← Competitor profile card
│   ├── Pattern分类表.md          ← Pattern discovery & evaluation
│   └── output-template.md        ← Unified result template
├── examples/                    ← Worked examples
│   ├── quick-analysis-example.md
│   └── 终端方向竞品分析.md
└── evaluation/                  ← Benchmark & testing
    └── benchmark.md
```

---

## When to Use (and When Not To)

### Suitable For

- Product feature and service capability comparison
- User journey, conversion, and retention analysis
- Content and operational mechanism analysis
- Business model and pricing research
- Market opportunity scanning
- Strategic positioning and differentiation assessment

### Not Suitable / High Risk

| Scenario | Why | What to Do Instead |
|----------|-----|-------------------|
| No ability to access external information (no browsing, no search) | Evidence will be limited to user-provided materials only | State the limitation upfront; output as "preliminary analysis based on provided materials only" |
| Industry data is highly confidential or paywalled | Core evidence will be unavailable | Narrow scope to publicly observable signals; flag significant gaps |
| Requires real-time pricing or policy data but cannot browse live sources | Risk of using stale data for time-sensitive decisions | Explicitly timestamp all price/policy claims; mark as "stale — verify before use" |
| "Competitor" itself is poorly defined | Analysis without clear scope produces noise | Refuse to proceed until the user clarifies who they're comparing against and why |
| User wants to directly copy a competitor's features | This workflow evaluates opportunities, not clones products | Redirect: "Let's evaluate whether this feature makes sense for YOUR users and strategy" |
| Evidence is insufficient but a precise market conclusion is demanded | Fills gaps with speculation, violating core principles | Report what IS known, label unknowns explicitly, refuse to fabricate precision |
| The user has no decision to make — just "curious what competitors are doing" | Analysis without a decision anchor produces unfocused output | Ask: "What decision would this analysis inform?" before starting |

---

## V3.0 Key Changes from V2.0

| Old Rule | V3.0 |
|----------|------|
| Ask one question at a time | Execute directly when information is sufficient |
| Confirm every phase | Only confirm when ambiguity changes the conclusion |
| Pick 5–8 competitors directly | Build a candidate pool first, then screen 3–6 core |
| "Competitor has X, we don't" = opportunity | First evaluate user value, strategic fit, cost, risk |
| High/Medium/Low confidence | A/B/C/D evidence grades |
| Fixed fill-in-the-blank report | Adapt output to audience (executive, product, ops, research) |
| Must fill every Pattern slot | Honestly state when no patterns are found |
| One-size-fits-all execution | Platform capability mapping and limitation disclosure |

---

## Author

**Diandian** — User Researcher, psychology background. Focused on AI workflows, user research, and data-driven decision making.

---

## License

MIT
