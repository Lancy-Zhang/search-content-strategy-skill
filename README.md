# Search Content Toolkit

**Content research, planning, production and performance diagnosis — one reusable AI skill.**

Portfolio project by **Lancy Zhang · 张欣澜**

[中文使用指南](README.zh-CN.md) · [Skill entry point](plan-search-content/SKILL.md)

## Contents
- What this skill does
- Choose a task
- What to provide
- Quick start
- Six ready-to-use prompts
- Combine tasks
- What happens next

## What this skill does
Help a brand decide **what content to create, which pages to improve, how to brief and write it, and how to investigate results**.
This is one reusable skill with six capabilities. You can describe your goal in everyday language; you do not need to know a module number or complete every step.
English is the default documentation language. Requests and deliverables can be English, Chinese or bilingual.

## Choose a task
| Capability | Question it answers | Minimum useful input | What you receive |
|---|---|---|---|
| **Find Content Opportunities** | What should this brand talk about, and why? | Website or offer description, target market; goal if known | User needs, topic ideas, specific gaps, brand value and sources |
| **Plan Keywords & Pages** | Which searches belong together, and which page should answer them? | Keyword list or permission to research candidate terms; offer, market and existing pages if available | Keyword groups, likely intent, create/update/merge/defer recommendations |
| **Build a Content Brief** | What should a writer or campaign team produce? | Topic, audience, goal, verified facts; existing research if available | Structured Content Brief or broader Campaign Brief |
| **Write & Review Content** | How do we turn the brief into useful, accurate content? | Brief or sufficient audience/goal/facts; style or draft if available | Draft or revision, title, description, link suggestions and quality notes |
| **Diagnose Search Performance** | What changed, what might explain it, and what should we check? | GSC and/or GA4 data, relevant periods, filters and definitions | Verified changes, possible causes, next checks and improvement actions |
| **Prioritise Content Work** | What should we do first with limited time or budget? | Candidate tasks, goal, evidence and constraints | Do first / do later / defer plan with reasons and measurement |

GSC means Google Search Console (search visibility and clicks). GA4 means Google Analytics 4 (website visits and behaviour). A Content Brief specifies one article/page; a Campaign Brief coordinates a larger marketing project.

## What to provide
**For a first website review:** start with a website and target market. Add one sentence about your goal, such as more product enquiries. If the site cannot be read, provide relevant page text or product information.
**For a more tailored plan:** add audience, existing content, known keywords, competitors and available production resources. You do not need every field to start.
**For performance diagnosis:** provide actual exports or authorised access. GSC alone can support search-performance analysis; GA4 alone can support website-behaviour analysis. Both are helpful but neither is automatically mandatory for the other. Comparing changes requires comparable periods; one period supports a current-state review.
**For writing:** provide verified facts and a brief, or ask the toolkit to prepare the brief first. Include brand tone, language and desired action.

| Available information | Can do now | Needs additional evidence |
|---|---|---|
| Website only | Review visible content, suggest candidate topics/pages, draft an initial plan | Actual search demand, rankings, traffic, conversion or ROI conclusions |
| Website + keyword list | Clean/group terms, infer intent, map pages | Verified volume/difficulty if not supplied or researched |
| GSC exports | Analyse visibility, clicks, queries and page changes supported by the export | On-site actions or actual sales without corresponding records |
| GA4 exports | Analyse supported channels, landing pages and events | Complete organic search queries; untracked actions |
| PMax / Search ad exports | Use relevant search-term evidence to inform content research | Full advertising efficiency, budget and bidding analysis requires a separate paid-media workflow |

No automatic access to company accounts is created by installing the skill. Do not supply passwords. Share only authorised data and remove personal details when unnecessary.

## Quick start
Replace the bracketed fields and send this in an assistant where the skill is installed or available:

```text
Use $plan-search-content to review [website].
Target market: [country/region].
Business goal: [goal].
Start with content opportunities, keyword/page planning and priorities.
Use public evidence, distinguish facts from assumptions, and tell me only what additional inputs would materially improve the result.
Output language: [English / Chinese / bilingual].
```

If you are unsure what to choose:

```text
Use $plan-search-content. Here is my website: [URL].
I want to achieve [goal] in [market]. Choose the most useful tasks for me and start with the information available.
```

## Six ready-to-use prompts
### Find Content Opportunities
```text
Use $plan-search-content to find content opportunities for [website/brand].
Market: [market]. Audience: [audience]. Goal: [goal].
Review current content and relevant search evidence. Recommend topics, explain the user need, show the specific gap and describe the value our brand can add. Cite sources and mark unverified ideas.
```

### Plan Keywords & Pages
```text
Use $plan-search-content to group the attached keywords for [brand] in [market].
Existing pages: [URLs or attachment].
Identify user needs and search intent. Recommend which groups belong on one page and which pages to create or update. Do not invent search volumes.
```

### Build a Content Brief
```text
Use $plan-search-content to build a Content Brief for [topic/page].
Audience: [audience]. Goal: [goal]. Primary keyword: [keyword, if known].
Verified product facts and sources: [materials].
Include the angle, outline, supporting evidence, internal links, CTA and measurement. List missing facts separately.
```
For a multi-channel project, replace “Content Brief” with “Campaign Brief” and add channels, budget and timing if known.

### Write & Review Content
```text
Use $plan-search-content to write or improve [article/page] using the attached brief and verified materials.
Language/tone: [requirements]. Desired length: [range, optional].
Deliver the draft, title, description, relevant internal-link suggestions and factual quality checks. Keep editorial questions outside the final prose.
```

### Diagnose Search Performance
```text
Use $plan-search-content to investigate [problem].
Attached data: [GSC and/or GA4 exports].
Current period: [dates]. Comparison period: [dates]. Market/filters: [scope].
Important events and known website/tracking changes: [definitions/changes].
Validate data first, find the main contributors, separate facts from hypotheses, and recommend checks/actions with metrics and a review window.
```
Do not guess unavailable fields; the toolkit should request the specific missing columns needed for a conclusion.

### Prioritise Content Work
```text
Use $plan-search-content to prioritise these content tasks: [list or attachment].
Goal: [goal]. Evidence: [sources/data]. Available time/budget: [constraints].
Recommend do first, do later and defer. Explain expected value, effort, dependencies, minimum deliverables and how to evaluate each action.
```

## Combine tasks
**Plan and produce:** find opportunities → plan keywords/pages → prioritise → build a brief → write and review.
**Improve existing results:** diagnose available data → choose relevant page/content actions → prioritise → create a brief or revision → review results.
A request to “run the whole toolkit” includes diagnosis only when real performance data is available. Without it, receive a measurement plan rather than invented results.

```text
Use $plan-search-content to create a content plan for [brand/website] in [market].
Goal: [goal]. Audience: [audience]. Materials: [links/files]. Constraints: [resources].
Find opportunities, group keywords, map pages and prioritise work. Then create one brief and draft for the top-priority topic. If analytics data is available, diagnose it first; otherwise list the data needed to measure the plan.
```

## What happens next
The assistant selects relevant tasks, uses supplied or authorised sources, flags critical gaps, and produces the requested deliverables. Ask for changes in natural language, such as “focus on existing pages”, “make the brief shorter”, or “explain this in Chinese”. No special command syntax is required beyond making the skill available or invoking it.
Recommendations do not automatically publish content or change advertising, tracking or website settings.

## Files and installation
- `plan-search-content/SKILL.md`: skill entry point and routing.
- `plan-search-content/references/`: task workflows and Getting Started reference.
- `plan-search-content/assets/`: brand input and delivery templates.
- `plan-search-content/agents/openai.yaml`: display metadata.

Install the complete `plan-search-content` folder using your assistant's supported skill installation method. This GitHub page is source documentation; visiting it alone does not install or run the skill. The skill requires no embedded passwords or API keys.

## Portfolio focus
Content strategy · search intent analysis · keyword grouping · briefing · editorial quality · marketing analytics · reusable AI workflow design.
