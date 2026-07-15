# AGENTS.md

## Repository Purpose

This repository is an evidence-based competitive-intelligence operating system for AI and Agents.

Its purpose is to move from a business decision to:

- an own-product baseline;
- a relevant competitor set;
- traceable evidence;
- comparable analysis;
- opportunity assessment;
- prioritised actions.

## Required Loading Order

1. Read `SKILL.md`.
2. Identify the requested execution mode.
3. Check available tools:
   - web search;
   - browser or product access;
   - uploaded-file analysis;
   - spreadsheets or Python;
   - persistent file editing.
4. Create or update project state using `templates/project-state.md`.
5. Establish the own-product baseline before judging competitors.
6. Build and screen the candidate pool.
7. Record important claims in `templates/evidence-ledger.md`.
8. Select only the analysis frameworks needed for the decision.
9. Classify recommendations by action type and priority.
10. Select the correct output template.
11. Run the quality gate.

Do not treat README files as operating instructions. README files explain the repository to humans; `SKILL.md` controls execution.

## Execution Modes

### Quick Judgment

Use for one competitor, one mechanism or one immediate question.

Expected output:

- core judgment;
- key evidence;
- implication for the user's product;
- next validation action;
- important unknowns.

### Standard Analysis

Use for a defined business question and several competitors.

Expected process:

- decision definition;
- own baseline;
- candidate scan;
- core competitor selection;
- evidence ledger;
- focused comparison;
- action recommendations.

### Deep Research

Use for strategic, multi-market or high-risk decisions.

Expected process:

- broader market scan;
- multiple evidence types;
- conflict resolution;
- detailed opportunity assessment;
- complete source appendix;
- stability and freshness review.

## Startup Protocol

The first substantive response must include:

```markdown
## 任务理解
- 当前业务问题：
- 需要支持的决策：
- 我方对象：
- 分析范围：

## 执行方式
- 执行模式：
- 可用工具：
- 预计使用的证据类型：

## 信息状态
- 已确认：
- 【假设】：
- 关键缺口：

## 下一步
- 直接开始，或只提出一个会实质改变竞品选择或结论的关键问题。
````

## Autonomy Rules

1. Information sufficient: execute.
2. Non-critical gaps: make and label assumptions.
3. Critical gaps: ask the minimum necessary question.
4. No web access: limit analysis to user-provided materials.
5. No direct product access: do not claim product paths were tested.
6. No evidence: label unknown rather than inventing precision.
7. Do not use popularity as the only competitor-selection criterion.
8. Do not treat competitor feature presence as proof that the user should build it.
9. Do not claim a feature improves retention, revenue or satisfaction without outcome evidence.
10. Do not fabricate pricing, user reviews, market share, links or product capabilities.

## Project State

Maintain:

* decision question;
* own-product baseline;
* candidate pool;
* selected competitors;
* selection weights;
* evidence status;
* unresolved conflicts;
* selected frameworks;
* action recommendations;
* next validation steps.

Use `templates/project-state.md`.

## Evidence Ledger

Every important claim receives a Claim ID such as `CA-C001`.

Each claim must include:

* claim type;
* source;
* collection time;
* the exact proposition the source supports;
* freshness;
* evidence grade;
* conflicts;
* limitations.

Use `templates/evidence-ledger.md`.

## Cross-Repository Routing

Use the User Research Operating System when the decision depends on:

* whether users actually value a feature;
* why users adopt or abandon a journey;
* user motivations and barriers;
* target-user segmentation;
* validating a competitive opportunity with users.

Repository:

`https://github.com/diandian1001/user-research-sop`

## Completion Rule

Do not declare completion until:

* the business decision is answered;
* the own-product baseline is visible;
* competitor selection is explained;
* important claims are traceable;
* evidence and capability maturity are separated;
* recommendations include action type and priority;
* unknowns, risks and conflicts are visible;
* sources and collection times are included;
* the selected output template is complete;
* the quality gate passes.
