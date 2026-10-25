# Search Content Strategy Skill
### 搜索内容策略工作台

A reusable AI skill that turns brand context and search evidence into content decisions, briefs, drafts and measurable optimisation actions.

**Portfolio project by Lancy Zhang · 张欣澜**

## What it does | 六个模块

| Module | Purpose | Deliverable |
|---|---|---|
| M1 Content Opportunity Research | Identify relevant user needs and content gaps | Evidence-backed topic opportunities |
| M2 Keyword & Page Planning | Cluster queries, infer intent and map existing pages | Keyword clusters and page actions |
| M3 Brief Builder | Translate research into production requirements | Content Brief / Campaign Brief |
| M4 Content Production & QA | Draft content and check facts, intent and brand voice | Draft, metadata and QA record |
| M5 GSC / GA4 Diagnostics | Investigate search and website performance changes | Findings, hypotheses and verification actions |
| M6 Content Prioritisation | Balance business relevance, evidence, effort and dependencies | Prioritised content backlog |

## How it works | 工作流

Start with brand, market, audience and business objective. The entry point selects the required modules and passes evidence and decisions between them.

**Full planning flow:** opportunities → keyword/page planning → prioritisation → brief → production and QA.

**Performance investigation:** diagnostics → targeted research or page improvements → prioritisation → measurement.

Modules also work independently. Shared evidence IDs connect a recommendation to its source, topic, keyword cluster and page.

## Use the skill | 使用方法

1. Open [the entry point](plan-search-content/SKILL.md) and review the [brand intake template](plan-search-content/assets/brand-intake.md).
2. In a compatible skill-enabled assistant, install the complete `plan-search-content` folder using that host's skill installation method. Reading this repository alone does not install or run the skill.
3. Invoke `$plan-search-content` with your brand information and task. Supply authorised GSC/GA4 exports when diagnosing performance.

Example prompts:

> 使用 $plan-search-content，为这个品牌进行内容机会研究、关键词分组和优先级排序。目标市场：[国家]；官网：[URL]；业务目标：[目标]。

> Use $plan-search-content to create a content brief from these keyword clusters and verified product facts.

> 使用 $plan-search-content，比较这两期 GSC/GA4 导出，区分已确认事实、可能原因与下一步验证行动。

## Project structure

- `plan-search-content/SKILL.md` — routing, shared context and final checks.
- `plan-search-content/references/` — six workflows and evidence rules.
- `plan-search-content/assets/` — brand intake, delivery templates and icon.
- `plan-search-content/agents/openai.yaml` — assistant display metadata.

## Design principles | 设计重点

- Reuse the method across brands while keeping each brand's facts separate.
- Distinguish observed data, estimates, hypotheses and unknowns.
- Map similar queries to user needs instead of creating one article per keyword.
- Check metric scope, denominators and aggregation before interpreting changes.
- Keep recommendations connected to evidence, resources and measurement.
- Use authorised data connections or exports; the skill does not grant access to private analytics accounts.

## Skills demonstrated | 项目能力

Content strategy · SEO research workflow design · Keyword clustering · Search intent analysis · Content briefing · Editorial QA · Marketing analytics · AI workflow design.

本项目将内容研究、生产与效果分析整理为可复用的技能流程，支持中文、英文及双语交付。
