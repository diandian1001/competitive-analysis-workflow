# AI 竞品与竞争情报操作系统 V4.0

**Evidence-Based Competitive Intelligence Agent — 可移植、可执行、可追踪**

[English](README.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-7c5cfc.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/diandian1001/competitive-analysis-workflow?style=social)](https://github.com/diandian1001/competitive-analysis-workflow)
[![Version](https://img.shields.io/badge/Version-V4.0-10b981.svg)](https://github.com/diandian1001/competitive-analysis-workflow)

把这个仓库交给 AI 或 Agent，并告诉它需要支持的业务决策。它会先建立我方基线，再筛选真正相关的竞品，建立 Claim 级证据账本，完成对比、机会评估和行动建议。

本仓库提供三种入口：

| 入口 | 文件 | 适用场景 |
|---|---|---|
| Agent 仓库模式 | `AGENTS.md` | Hermes、Codex、Claude Code 等能够读取仓库的 Agent |
| Skill 模式 | `SKILL.md` | 支持系统指令、Project Knowledge 或 Skill 的平台 |
| 任意 AI 便携模式 | `PORTABLE.md` | 无法可靠读取完整 GitHub 仓库的普通 AI |

> 清晰任务直接执行。只有缺失信息会实质改变竞品选择、证据范围或决策结论时才提问。

---

## 一句话启动

### 仓库模式

```text
读取 AGENTS.md，并使用这个仓库完成以下竞品分析：
[粘贴业务问题和决策]
```

### Skill 模式

```text
使用 SKILL.md，以标准分析模式完成：
[粘贴业务问题和决策]
```

### 任意 AI 模式

复制 `PORTABLE.md` 全文并追加任务。

---

## 30 秒看懂

> ⚠️ **以下为结构示意，不代表实际竞品调研结论。** 展示使用该 Workflow 时可以产出什么结构的分析。

**业务问题：**
> *"服务型公众号转型后，应该保留哪些运营机制，才能维持用户回访？"*

**这个 Workflow 会输出什么：**

| 输出类型 | 结构（示意） |
|---------|-------------|
| **核心判断** | [基于证据评估后填入 —— 实际分析后生成] |
| **核心竞品** | 候选池 → 筛选为核心竞品，附选择理由 |
| **关键事实** | 【事实·A】竞品官方页面确认签到功能存在 【事实·B】实测确认签到入口可在 1 步内到达 【推断·D】签到可能承担回访触发作用，但缺少使用数据验证贡献率 【待验证】签到用户的真实回访率和奖励成本 |
| **证据等级分布** | 取决于实际可获得来源 —— 详见[证据规则](references/evidence-rubric.md) |
| **待验证问题** | 【待验证】无主动推送时，用户是否会回访查看"使用报告"？ 【待验证】签到粘性是否跨行业可迁移？ |
| **行动建议** | **P0/P1/P2** 按证据强度、用户价值和战略适配排序 —— 具体行动在分析后填入 |

→ [完整案例](examples/终端方向竞品分析.md) | [快速判断示例](examples/quick-analysis-example.md)

---

## 核心能力

- 三种模式：快速判断、标准分析、深度研究
- 我方基线：先记录用户、场景、能力、指标、资源和风险约束
- 动态候选池：根据执行模式和信息增益决定数量
- 加权竞品筛选：权重随业务决策变化
- Claim 级证据账本：重要主张关联来源、时间、等级、冲突和局限
- 证据分级：A/B/C/D 四级置信度（详见[证据规则](references/evidence-rubric.md)）
- 事实分层：事实、推断、待验证、建议
- 多框架分析：功能矩阵、用户旅程、价值曲线、SWOT/TOWS
- 动作与优先级分离：BUILD / VALIDATE / MONITOR / REJECT × P0 / P1 / P2 / P3
- 三种输出：快速判断、标准分析、深度研究
- 项目状态：持续记录范围、基线、竞品、证据和下一步
- 跨工作流路由：用户价值与行为假设转交用户研究操作系统
- Benchmark：跨平台、重复运行并核验来源
- 平台适配：ChatGPT、Claude、Hermes
- 质量审查：防止过期信息、主场偏差、伪精确和机械跟随

---

## 工作流程

```text
定义决策问题
→ 建立我方基线
→ 建立候选池
→ 使用决策权重筛选核心竞品
→ 建立 Claim 级证据账本
→ 选择分析框架
→ 识别 Pattern
→ 评估机会与优先级
→ 输出行动建议
→ 质量审查
```

---

## 怎么使用

### 方式一：交给 AI Agent（推荐）

把仓库地址或 `SKILL.md` 提供给 AI，然后说明业务问题：

```text
使用这个 Skill，分析[你的主题]。
目标是支持[决策]，优先关注[关键维度]。
```

### 方式二：按平台适配

- **ChatGPT**：将 `skills/chatgpt.md` 作为 Custom Instructions 或直接粘贴
- **Claude**：将 `skills/claude.md` 添加为 Project Knowledge
- **Hermes**：将 `skills/hermes.md` 作为 Skill 文件使用

### 方式三：手动使用

打开 `SKILL.md`，按阶段手动执行。配合 `templates/` 中模板做结构化记录。

核心方法不绑定工具。平台没有联网、文件或代码能力时，AI 必须说明限制，不得假装完成验证。

---

## 目录

```
.
├── AGENTS.md                    ← Agent 仓库加载与执行协议
├── PORTABLE.md                  ← 任意 AI 可用的单文件便携版
├── SKILL.md                     ← 核心操作系统（V4.0）
├── README.md                    ← 英文说明文档
├── README_zh.md                 ← 中文说明文档（本文件）
├── CHANGELOG.md
├── LICENSE
├── skills/                      ← 平台适配
│   ├── chatgpt.md
│   ├── claude.md
│   └── hermes.md
├── references/                  ← 详细方法论
│   ├── competitor-selection.md
│   ├── evidence-rubric.md
│   ├── analysis-frameworks.md
│   └── quality-checklist.md
├── templates/                   ← 可复用模板
│   ├── project-state.md
│   ├── evidence-ledger.md
│   ├── output-quick.md
│   ├── output-standard.md
│   ├── output-deep.md
│   ├── 分析目标卡.md             ← 分析范围界定
│   ├── 竞品档案卡.md             ← 竞品信息采集
│   ├── Pattern分类表.md          ← 模式发现与评估
│   └── output-template.md        ← 输出模板索引
├── examples/                    ← 填写示例
│   ├── quick-analysis-example.md
│   └── 终端方向竞品分析.md
└── evaluation/                  ← 测试与基准
    └── benchmark.md
```

---

## 适用范围与失败场景

### 适合用

- 产品功能与服务能力对比
- 用户旅程、转化与留存分析
- 内容和运营机制拆解
- 商业模式与定价研究
- 市场机会扫描
- 战略定位与差异化判断

### 不适合 / 高风险

| 场景 | 原因 | 替代方案 |
|------|------|---------|
| 缺少外部信息访问能力（不能联网搜索、不能浏览网页） | 证据将仅限于用户提供的材料 | 提前声明限制，输出标注"仅基于已提供材料的初步分析" |
| 行业数据高度保密或需付费获取 | 核心证据无法获取 | 缩小范围到公开可观察信号；标注重大信息缺口 |
| 需要实时价格或政策信息但无法联网 | 时间敏感决策使用过期数据的风险 | 所有价格/政策声明标注时间戳，标注"可能已过期——使用前验证" |
| "竞品"概念本身不清晰 | 无明确范围的分析会产生噪音 | 拒绝启动，直到用户澄清和谁比、为什么比 |
| 用户要求直接复制竞品功能 | 本 Workflow 评估机会，不是克隆产品 | 引导："让我们先评估这个功能对你的用户和策略是否有意义" |
| 证据不足却要求精确市场结论 | 用推测填补空白，违反核心原则 | 报告已知信息，明确标注未知，拒绝伪造精确度 |
| 没有真实决策需求——只是"好奇竞品在做什么" | 无决策锚点的分析产出散乱 | 启动前先问："这次分析要支撑什么决策？" |

---

## V4.0 核心升级

- **我方基线前置**：先理解我方用户、场景、能力、指标和约束；
- **动态候选池**：根据模式和信息增益决定数量，不机械凑满；
- **加权筛选**：权重随业务决策变化，不再固定等权 `/14`；
- **Claim 级证据账本**：每条重要主张可追踪到来源、时间和局限；
- **动作与优先级分离**：BUILD、VALIDATE、MONITOR、REJECT × P0/P1/P2/P3；
- **三种输出模板**：快速判断、标准分析、深度研究；
- **项目状态管理**：持续记录范围、基线、竞品、证据和下一步；
- **单文件便携版**：`PORTABLE.md` 可直接复制给任意 AI；
- **Agent 加载协议**：`AGENTS.md` 规定仓库读取和执行顺序；
- **跨工作流路由**：用户价值与行为假设转交用户研究操作系统。

## 更新日志

| 版本 | 日期 | 变更 |
|---|---|---|
| V3.0 | 2026-07 | 证据治理、机会评估和跨平台适配 |
| V4.0 | 2026-07 | 执行封装升级：我方基线、加权筛选、证据账本、动作类型、便携版与 Agent 协议 |

---

## 作者

**Diandian** — 用户研究员，心理学背景，关注 AI 工作流、用户研究与数据驱动决策。

---

## License

MIT
