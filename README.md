# AI Competitive Intelligence Operating System V4.0

**A portable, executable and traceable evidence-based competitive intelligence package**

[中文版](README_zh.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-7c5cfc.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/diandian1001/competitive-analysis-workflow?style=social)](https://github.com/diandian1001/competitive-analysis-workflow)
[![Version](https://img.shields.io/badge/Version-V4.0-10b981.svg)](https://github.com/diandian1001/competitive-analysis-workflow)

Give this repository to an AI or Agent and state the business decision it must support. It establishes the own-product baseline first, screens relevant competitors with decision-specific weights, manages a Claim-level evidence ledger, and produces comparisons, opportunity judgments and executable actions.

| Entry | File | Best for |
|---|---|---|
| Repository-aware Agent | `AGENTS.md` | Agents that can inspect a repository |
| Skill / System Instructions | `SKILL.md` | Platforms supporting Projects, Skills or system instructions |
| Any AI Chat | `PORTABLE.md` | Models that cannot reliably read a full GitHub repository |

Clear tasks execute directly. The AI asks a question only when missing information would materially change competitor selection, evidence scope or the decision conclusion.

---

## Start in One Prompt

### Repository Mode

```text
Read AGENTS.md and use this repository to complete the following competitive analysis:
[paste the business problem and decision]
```

### Skill Mode

```text
Use SKILL.md in Standard Analysis Mode to complete:
[paste the business problem and decision]
```

### Any AI Mode

Copy the full contents of `PORTABLE.md`, then append the task.

---

## 30-Second Example

> ⚠️ **The following is a structural illustration, not actual competitive analysis conclusions.** It shows the output format this workflow can produce.

**Business question:**
> *"Our service-oriented WeChat Official Account is transitioning. Which operational mechanisms should we keep to sustain user return visits?"*

**What the workflow produces:**

| Output | Structure (illustrative) |
|--------|--------------------------|
| **Core judgment** | [Based on evidence evaluation — filled after actual analysis] |
| **Core competitors** | Candidate pool → screened to core competitors with documented selection rationale |
| **Key facts** | 【事实/Fact·A】Competitor official page confirms check-in feature exists 【事实/Fact·B】Direct product testing confirms check-in accessible within 1 tap 【推断/Inference·D】Check-in may serve as a return trigger, but lacks usage data to verify contribution rate 【待验证/Unverified】Actual return-visit rate and reward cost for check-in users |
| **Evidence grades** | Grade distribution depends on available sources — see [Evidence Rubric](references/evidence-rubric.md) |
| **Open questions** | 【待验证/Unverified】Would users return for "usage reports" without explicit push notifications? 【待验证/Unverified】Is check-in stickiness transferable across industries? |
| **Recommendations** | **P0/P1/P2** prioritized by evidence strength, user value, and strategic fit — specific actions filled after analysis |

→ [Full example](examples/终端方向竞品分析.md) | [Quick analysis example](examples/quick-analysis-example.md)

---

## Core Capabilities

- Three modes: quick judgment, standard analysis, deep research
- Own-product baseline covering users, scenarios, capabilities, metrics, constraints and risks
- Dynamic candidate pools based on execution mode and information gain
- Weighted competitor selection aligned to the business decision
- Claim-level evidence ledger with source, time, grade, conflicts and limitations
- A/B/C/D evidence confidence levels (see [Evidence Rubric](references/evidence-rubric.md))
- Separation of facts, inferences, open questions, and recommendations
- Functional matrix, user journey, value curve, SWOT/TOWS
- Separate action types (BUILD / VALIDATE / MONITOR / REJECT) from priority (P0 / P1 / P2 / P3)
- Quick, standard and deep output templates
- Persistent project state and cross-workflow routing
- Cross-platform repeated-run Benchmark with source verification
- Platform guidance for ChatGPT, Claude, and Hermes
- Quality checks against stale data, home-team bias, false precision, and feature copying

---

## Workflow

```text
Define the decision
→ Establish the own-product baseline
→ Build a candidate pool
→ Select core competitors using decision-specific weights
→ Build the Claim-level evidence ledger
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
├── AGENTS.md                    ← Repository loading and execution protocol
├── PORTABLE.md                  ← Single-file package for any AI
├── SKILL.md                     ← Core operating system (V4.0)
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
│   ├── project-state.md
│   ├── evidence-ledger.md
│   ├── output-quick.md
│   ├── output-standard.md
│   ├── output-deep.md
│   ├── 分析目标卡.md             ← Analysis scoping card
│   ├── 竞品档案卡.md             ← Competitor profile card
│   ├── Pattern分类表.md          ← Pattern discovery & evaluation
│   └── output-template.md        ← Output template index
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

## V4.0 Core Upgrades

- **Own-product baseline first**: understand users, scenarios, capabilities, metrics and constraints before judging competitors
- **Dynamic candidate pool**: size follows execution mode and information gain
- **Weighted selection**: decision-specific weights replace fixed equal-weight `/14` scoring
- **Claim-level evidence ledger**: every important claim traces to its source, time and limitations
- **Action and priority separation**: BUILD, VALIDATE, MONITOR or REJECT × P0, P1, P2 or P3
- **Three output templates**: quick judgment, standard analysis and deep research
- **Project state management**: persist scope, baseline, competitors, evidence and next action
- **Portable single-file package**: copy `PORTABLE.md` directly into any AI chat
- **Agent loading protocol**: `AGENTS.md` defines repository reading and execution order
- **Cross-workflow routing**: user-value and behavior hypotheses route to the AI User Research Operating System

## Changelog

| Version | Date | Changes |
|---|---|---|
| V3.0 | 2026-07 | Evidence governance, opportunity evaluation and platform-aware execution |
| V4.0 | 2026-07 | Execution packaging: own-product baseline, weighted selection, evidence ledger, action types, portable file and Agent protocol |

---

## Author

**Diandian** — User Researcher, psychology background. Focused on AI workflows, user research, and data-driven decision making.

---

## License

MIT
