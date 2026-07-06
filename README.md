# Competitive Analysis Workflow

[![License: MIT](https://img.shields.io/badge/License-MIT-7c5cfc.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/diandian1001/competitive-analysis-workflow?style=social)](https://github.com/diandian1001/competitive-analysis-workflow)

[中文版](README_zh.md)

A **standardized competitive analysis workflow** — a five-phase framework for market research, product strategy, and content direction validation.

> From "gut feeling" to "proven method" — a repeatable, evaluable, and collaborative process.

---

## Why This Exists

Most teams do competitive analysis this way:

- Ad-hoc every time, quality depends on who's doing it
- No structured output, no reusable framework
- "Should we pursue this direction?" answered by intuition, not data
- New team member starts from scratch

This workflow ensures **anyone with basic domain knowledge can produce competitive analysis with a consistent quality baseline** by following the process.

---

## Workflow Overview

```
Phase 1        Phase 2         Phase 3         Phase 4          Phase 5
Define Goal → Select Targets → Build Framework → Find Patterns → Conclusions
```

| Phase | Core Action | Output |
|-------|------------|--------|
| Phase 1 Define Goal | Answer "why, who, what" | Analysis Goal Card |
| Phase 2 Target Selection | Three-layer funnel (direct / indirect / benchmark) | Competitor Profile Card |
| Phase 3 Build Framework | Choose: Comparison Matrix / User Journey / SWOT / Value Curve | Analysis Matrix |
| Phase 4 Find Patterns | Fill data, identify 4 types of opportunities | Pattern Classification Table |
| Phase 5 Conclusions | Judgment + Gap + Path + Risk | Conclusion Report |

---

## Quick Start

### 1. Clone

```bash
git clone https://github.com/diandian1001/competitive-analysis-workflow.git
cd competitive-analysis-workflow
```

### 2. Follow the Process

1. Copy `templates/Analysis_Goal_Card.md`, fill in your analysis objective
2. Copy `templates/Competitor_Profile_Card.md`, build a profile for each competitor
3. Copy `templates/Pattern_Classification.md`, fill in data and find patterns
4. See `examples/Terminal_Direction_Analysis.md` for a complete walkthrough

### 3. Output Report

Conclusion-first structure:

```
I. Core Verdict (one sentence)
II. Key Findings (3-5 points, with data)
III. Gap Analysis
IV. Recommended Path
V. Risk Flags
```

---

## Core Tools

### Three-Layer Funnel for Target Selection

| Layer | Selection Criteria | Example |
|-------|-------------------|---------|
| Direct Competitors | Same industry × Same channel × Same business | Other brands' service accounts in the same sector |
| Indirect Competitors | Different industry × Same user group × Same scenario | E-commerce platform corresponding channels |
| Benchmarks | Different industry × Strategies worth borrowing | Brands with strong private domain operations |

### Four Pattern Types

| Pattern | Meaning | Action |
|---------|---------|--------|
| They have + We don't | Opportunity | Evaluate whether to build |
| They have + We do poorly | Gap | Needs improvement |
| Everyone has + Everyone does it poorly | Industry challenge | Invest cautiously |
| We have + They don't | Differentiation | Strengthen it |

### Four Analysis Frameworks

- **Framework A: Feature/Content Comparison Matrix** — Most basic, good for feature comparison
- **Framework B: User Journey Comparison** — Good for conversion path analysis
- **Framework C: SWOT Differentiation** — Good for conclusion phase
- **Framework D: Value Curve Comparison** — Good for differentiation positioning, radar charts

---

## Repository Structure

```
competitive-analysis-workflow/
├── README.md                          # This file (English)
├── README_zh.md                       # 中文版说明文档
├── SKILL.md                           # Full workflow (Hermes Agent Skill format)
├── LICENSE                            # MIT License
├── templates/
│   ├── Analysis_Goal_Card.md          # Phase 1 template
│   ├── Competitor_Profile_Card.md     # Phase 2 template
│   └── Pattern_Classification.md      # Phase 4 template
└── examples/
    └── Terminal_Direction_Analysis.md # Full case study (carrier service account)
```

---

## Use Cases

- Operational strategy validation ("Should we pursue this direction?")
- Product feature competitive comparison ("What do competitors have that we don't?")
- Content strategy research ("How are competitors doing content?")
- Market opportunity scanning ("Is there room in this space?")

---

## Common Pitfalls

| Pitfall | Prevention |
|---------|-----------|
| Goal too vague, no clear next step | Phase 1 must output an Analysis Goal Card |
| Listing without analyzing, no comparison or judgment | Use frameworks to force comparison, find patterns |
| Only looking at direct competitors, missing cross-industry benchmarks | Three-layer funnel, cover at least two layers |
| Drawing conclusions with insufficient data | Every conclusion must be backed by data |
| Vague conclusions, not actionable | Every recommendation must have a concrete first step |

---

## Author

**Diandian** — User Researcher, 2+ years UX Research experience

- Psychology background, skilled in quantitative research (survey design, K-Means clustering, session analysis)
- Research areas: user profiling, conversion funnel analysis, competitive strategy

---

## License

[MIT License](./LICENSE)
