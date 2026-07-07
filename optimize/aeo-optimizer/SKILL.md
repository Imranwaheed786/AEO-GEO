---
name: aeo-optimizer
description: 'Use when the user asks to "optimize for answer engines", "AEO strategy", "get recommended by AI", "AI visibility", "build consensus for AI". Transforms content strategy from traditional SEO to Answer Engine Optimization — targeting AI citations, brand visibility, and consensus across ChatGPT, Claude, Gemini, and AI Overviews. For tactical content rewriting, see geo-content-optimizer. For answer-first sentence structure, see first-sentence-engine.'
version: "1.0.0"
license: Apache-2.0
compatibility: "Claude Code ≥1.0, skills.sh marketplace, ClawHub marketplace, Vercel Labs skills ecosystem. No system packages required. Optional: MCP network access for SEO tool integrations."
homepage: "https://github.com/Imranwaheed786/seo-geo-claude-skills"
when_to_use: "Use when optimizing content strategy for Answer Engines like ChatGPT, Claude, Gemini, Perplexity, or Google AI Overviews. Also for measuring AI visibility, building brand consensus, tracking AI citations, or transitioning from SEO to AEO."
argument-hint: "<content URL, brand name, or strategy brief> [target answer engines]"
metadata:
  author: Imranwaheed786
  version: "1.0.0"
  geo-relevance: "high"
  tags:
    - aeo
    - answer-engine-optimization
    - ai-visibility
    - ai-citations
    - ai-share-of-voice
    - consensus-building
    - passage-indexing
    - brand-sentiment
    - chatgpt-optimization
    - claude-optimization
    - gemini-optimization
    - ai-overviews
    - query-fan-out
    - query-fan-map
    - chunking-optimization
    - retrieval-filters
    - ai-content-formatting
    - hallucination-gap-analysis
    - aida-funnel-mapping
    - competitor-orbits
    - ocs-grading
    - negative-content-strategy
    - hallucination-hunting
    - usp-extraction
    - query-path-tracing
    - master-prompt-formulation
    - prompt-engineering-aeo
    - aqce-writing-formula
    - AEO优化
    - AI答案引擎优化
    - AI最適化
    - AI최적화
  triggers:
    # EN-formal
    - "answer engine optimization"
    - "AEO strategy"
    - "optimize for answer engines"
    - "AI visibility strategy"
    - "AI share of voice"
    - "build consensus for AI"
    - "AI citation strategy"
    - "brand recommendation by AI"
    # EN-casual
    - "get recommended by AI"
    - "show up in ChatGPT answers"
    - "AI doesn't recommend my brand"
    - "how to get AI to mention me"
    - "ChatGPT never mentions us"
    - "build brand presence in AI"
    - "AI keeps recommending competitors"
    - "query fan out optimization"
    - "chunk optimization for AI"
    - "how to pass AI retrieval filters"
    - "build a query fan map"
    - "find AI hallucination gaps"
    - "what topics should I write for AI citation"
    - "AI content gap analysis"
    - "who are my AEO competitors"
    - "competitor analysis for AI ranking"
    - "which AI queries can I win"
    - "what does AI know about my brand"
    - "find what AI thinks about competitors"
    - "extract competitor USPs from AI"
    - "create AEO content writing prompt"
    # EN-question
    - "how to optimize for answer engines"
    - "what is AEO"
    - "how do I get cited by AI"
    - "how to measure AI visibility"
    - "what KPIs for AI optimization"
    - "how to build AI consensus"
    # EN-competitor
    - "AEO vs SEO"
    - "answer engine vs search engine"
    - "AI Overview optimization strategy"
    - "ChatGPT brand optimization"
    # ZH-pro
    - "答案引擎优化"
    - "AEO策略"
    - "AI可见度优化"
    - "AI引用策略"
    - "AI共识构建"
    # ZH-casual
    - "让AI推荐我的品牌"
    - "AI搜索不到我"
    - "怎么让ChatGPT提到我"
    - "AI总推荐竞品"
    # JA
    - "アンサーエンジン最適化"
    - "AEO戦略"
    - "AI可視性最適化"
    - "AI引用戦略"
    # KO
    - "답변 엔진 최적화"
    - "AEO 전략"
    - "AI 가시성 최적화"
    - "AI 인용 전략"
    # ES
    - "optimización para motores de respuesta"
    - "estrategia AEO"
    - "visibilidad en IA"
    # PT
    - "otimização para motores de resposta"
    - "estratégia AEO"
    - "visibilidade em IA"
    # Misspellings
    - "answer engine optimisation"
    - "anser engine optimization"
    - "AEO optimisation"
---

# AEO Optimizer

> **[SEO & GEO Skills Library](https://github.com/Imranwaheed786/seo-geo-claude-skills)** · 23 skills for SEO + GEO · [ClawHub](https://clawhub.ai/u/Imranwaheed786) · [skills.sh](https://skills.sh/Imranwaheed786/seo-geo-claude-skills)
> **System Mode**: This optimize skill follows the shared [Skill Contract](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/references/skill-contract.md) and [State Model](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/references/state-model.md).

This skill transforms content strategy from traditional SEO to Answer Engine Optimization (AEO). As AI systems increasingly answer user queries directly — via ChatGPT, Claude, Gemini, and Google AI Overviews — brands must optimize for AI citations, visibility, and consensus rather than rankings alone.

**System role**: Optimize layer skill. It audits existing content and strategy against AEO readiness, then produces a transformation plan that feeds into build-layer skills for execution.

## When This Must Trigger

Use this when the conversation involves transitioning from traditional search optimization to AI-first visibility — even if the user doesn't use AEO terminology:

- Measuring or improving brand visibility in AI-generated answers
- Building a strategy to get cited or recommended by ChatGPT, Claude, or Gemini
- Understanding why competitors appear in AI responses and you don't (Competitor Orbit mapping)
- Grading query difficulty for AEO (OCS: Open, Contested, Saturated)
- Transitioning content strategy from keyword-based SEO to question-based AEO
- Setting up AEO KPIs (AI Visibility, Citations, AI Share of Voice)
- Building consensus across third-party platforms to influence AI recommendations
- Recovering traffic lost to Google AI Overviews
- Formatting content for AI chunk retrieval and Query Fan Out coverage
- Passing the AI's three retrieval filters (Consistency, Consensus, Contextual Relevance)
- Finding hallucination gaps where AI lacks training data and needs your content
- Building a Query Fan Map (ICP × 5-stage AEO funnel) to systematically discover citation-worthy topics

## What This Skill Does

1. **Answer Engine Landscape Assessment**: Identifies which of the 4 engine types (LLMs, AI Overviews, Voice Assistants, Agentic Browsers) to target based on the user's niche
2. **AEO Readiness Audit**: Scores content against 8 AEO factors including passage autonomy, citation-worthiness, and cross-platform consistency
3. **Consensus Strategy**: Builds a multi-platform content distribution plan to create brand narrative dominance across AI training sources
4. **AI Model Targeting**: Tailors strategy to the distinct personalities of ChatGPT (agreeable), Claude (evidence-demanding), and Gemini (Google-integrated)
5. **AEO KPI Framework**: Establishes measurement for AI Visibility, Citations, AI Share of Voice, Consensus Score, and Navigational Search Lift
6. **Citation & Visibility Optimization**: Implements the Two Pillars — controlling source citations and earning direct brand recommendations
7. **LLM Ranking Mechanics**: Applies Query Fan Out mapping, Chunk autonomy scoring, and the 3 Retrieval Filters (Consistency, Consensus, Contextual Relevance)
8. **Query Fan Map (QF Map)**: Builds an ICP × 5-stage AEO funnel grid (Pre-Awareness through Decision) with hallucination testing, business-type templates (E-commerce, Local, SaaS), and a trust-building growth strategy
9. **Competitor Orbit Analysis**: Maps competitors into 3 orbits (Core/Mid/Outer), grades queries using OCS (Open/Contested/Saturated), hunts hallucination gaps via query layering and path tracing, and extracts AI-valued USPs from competitors
10. **Content Creation Protocol**: Produces Master Prompts and writes content using the A.Q.C.E. formula (Answer → Qualify → Cover → Extend), with semantic HTML formatting and Information Gain validation
11. **SEO-to-AEO Transformation**: Maps the 5 core differences and produces a migration plan preserving SEO foundations

## Quick Start

### Audit AEO Readiness

```
Audit my brand's AEO readiness for [brand name] targeting [industry/niche]
```

### Build Consensus Strategy

```
Build an AEO consensus strategy for [brand] across ChatGPT, Claude, and Gemini
```

### Set Up AEO KPIs

```
Set up AEO KPIs for [brand] — I want to track AI visibility, citations, and share of voice
```

### Build a Query Fan Map

```
Build a QF Map for [brand] — find hallucination gaps where AI can't answer accurately about [niche]
```

### Map Competitor Orbits

```
Map my AEO competitors for [brand/niche] — who can I beat and which queries are winnable?
```

## Skill Contract

**Expected output**: An AEO audit report with readiness scores, a consensus building plan, AEO KPI framework, and prioritized action items — plus a short handoff summary ready for `memory/audits/aeo-optimizer/`.

- **Reads**: brand name, target queries, current content inventory, competitor landscape, and prior SEO audits from [CLAUDE.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/CLAUDE.md) and the shared [State Model](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/references/state-model.md) when available.
- **Writes**: AEO readiness audit, consensus strategy, KPI framework, and transformation plan that can be stored under `memory/audits/aeo-optimizer/`.
- **Promotes**: AEO readiness scores, consensus gaps, priority platform targets, and AI model-specific findings to `memory/hot-cache.md`, `memory/decisions.md`, and `memory/open-loops.md`.
- **Next handoff**: use the `Next Best Skill` below when the audit is complete and content needs tactical optimization.

### Handoff Summary

Emit this shape when finishing the skill (see [skill-contract.md §Handoff Summary Format](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/references/skill-contract.md)):

- **Status**: DONE / DONE_WITH_CONCERNS / BLOCKED / NEEDS_INPUT
- **Objective**: what was analyzed, created, or fixed
- **Key Findings / Output**: the highest-signal result
- **Evidence**: URLs, data points, or sections reviewed
- **Open Loops**: blockers, missing inputs, or unresolved risks
- **Recommended Next Skill**: one primary next move

## Data Sources

> See [CONNECTORS.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/CONNECTORS.md) for tool category placeholders.

> **Note:** All integrations are optional. This skill works without any API keys — users provide data manually when no tools are connected.

**With ~~AI monitor + ~~SEO tool + ~~brand monitor connected:**
Automatically pull AI citation patterns, current AI visibility scores, brand sentiment across review platforms, and competitor AI recommendation frequency.

**With manual data only:**
Ask the user to provide:
1. Brand name and target industry/niche
2. Top 10–20 target queries where they want AI recommendations
3. Current content URLs or inventory
4. Any known instances of competitor AI recommendations

Proceed with the full workflow using provided data. Note in the output which metrics are from automated collection vs. user-provided data.

## Instructions

When a user requests AEO optimization, run these steps:

1. **Assess Answer Engine Landscape** — Determine which of the 4 engine types matter for the user's niche; profile AI model personalities (ChatGPT/Claude/Gemini) and their decision-making styles
2. **Audit AEO Readiness** — Score content against the Two Pillars (Citations and Visibility) and 8 AEO readiness factors; produce baseline scores
3. **Build Query Fan Map** — Define 4–5 ICPs; extract contextual queries using the 5 Methods; map to 5-stage AEO funnel (Pre-Awareness → Decision); test for hallucination gaps; assign content destinations
4. **Map Competitor Orbits & Hunt Hallucinations** — Classify competitors into 3 orbits; grade queries using OCS; apply 6 layer types to client's top services to find hallucination gaps; trace AI's background query paths; extract competitor USPs via 3-question audit; set attack sequence
5. **Build Consensus Strategy** — Create ICP-segmented content plan; map multi-platform distribution across 4 tiers; enforce message consistency
6. **Implement AEO KPI Framework** — Define measurement for AI Visibility, Citations, AI SOV, Consensus Score, and Navigational Search Lift; set targets and cadence
7. **Apply LLM Ranking Mechanics** — Score content chunks for autonomy; validate the 3 Retrieval Filters (Consistency, Consensus, Contextual Relevance)
8. **Produce Transformation Plan** — Map the 5 SEO→AEO shifts; prioritize actions by OCS grade and orbit; structure content calendar

> **References**: [instructions-detail.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/instructions-detail.md) (strategic workflow) · [query-fan-map.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/query-fan-map.md) (QF Map, hallucination testing) · [competitor-orbits.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/competitor-orbits.md) (orbits, OCS grading) · [hallucination-hunting.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/hallucination-hunting.md) (layering, path tracing, USP extraction) · [content-creation-protocol.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/content-creation-protocol.md) (Master Prompt, query analysis) · [llm-ranking-mechanics.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/llm-ranking-mechanics.md) (Chunking, 3 Filters)

## Validation Checkpoints

### Input Validation
- [ ] Brand name and target niche identified
- [ ] Top target queries defined (minimum 10)
- [ ] Current content inventory or URLs provided
- [ ] Target answer engines specified (default: all 3 major LLMs + AI Overviews)

### Output Validation
- [ ] **Banned-vocab self-check** — scan output for banned words/phrases per [skill-contract.md §Output Voice](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/references/skill-contract.md). Replace any hit with a concrete alternative.
- [ ] AEO readiness score produced for all 8 factors
- [ ] Consensus strategy includes ICP segmentation (minimum 3 segments)
- [ ] Multi-platform distribution covers all 4 tiers
- [ ] AEO KPI targets defined with measurement cadence
- [ ] Transformation plan maps all 5 SEO→AEO shifts
- [ ] Query Fan Out maps generated for top 5 target queries (≥80% sub-query coverage each)
- [ ] Content chunks scored for autonomy (target: ≥4/5 on Chunk Autonomy Checklist)
- [ ] All 3 Retrieval Filters validated (Consistency, Consensus, Contextual Relevance)
- [ ] QF Map grid populated (ICPs × 5 funnel stages) with hallucination-tested queries
- [ ] Competitors classified into 3 orbits (Core/Mid/Outer) with OCS grades assigned per query
- [ ] Attack sequence defined (Outer → Mid → Core) with timeline
- [ ] Source of each data point clearly stated (~~AI monitor data, user-provided, or estimated)

## Example

**User**: "Audit my brand's AEO readiness — we're an SEO SaaS tool called RankFlow and we're losing clicks to AI Overviews."

**Output** assesses the 4 answer engine types (prioritizes AI Overviews + ChatGPT for B2B SaaS), audits current citations and visibility across 3 models, identifies a consensus gap (brand appears on G2 but not in Reddit/Quora discussions), and produces a 90-day consensus building plan with ICP-segmented content for beginners, agencies, and enterprise. AEO Readiness Score: 38/100 → target 72/100. See full worked example in [references/instructions-detail.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/instructions-detail.md).

### Save Results

After delivering the AEO audit to the user, ask:

> "Save these results for future sessions?"

If yes, write a dated summary to `memory/audits/aeo-optimizer/YYYY-MM-DD-<brand>.md` containing:
- One-line AEO readiness verdict
- Top 3-5 actionable items
- Open loops or blockers
- Source data references

If any findings should influence ongoing strategy, recommend promoting key conclusions to `memory/hot-cache.md`.

## Reference Materials

- [Instructions Detail](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/instructions-detail.md) — Full 5-step workflow, AEO readiness scoring, audit checklists, worked example
- [AEO vs SEO Framework](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/aeo-vs-seo-framework.md) — The 5 core differences, KPI mapping, content strategy transformation checklist
- [Answer Engine Types](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/answer-engine-types.md) — Detailed profiles of 4 engine types, AI model personalities, targeting decision matrix
- [Consensus Building](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/consensus-building.md) — ICP segmentation, multi-platform distribution, message consistency, citation strategy
- [LLM Ranking Mechanics](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/llm-ranking-mechanics.md) — Query Fan Out mapping, Chunk autonomy scoring, 3 Retrieval Filters (Consistency, Consensus, Contextual Relevance)
- [Query Fan Map](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/query-fan-map.md) — Hallucination gap discovery, 5 query extraction methods, ICP × 5-stage AEO funnel, business-type templates, trust-building growth strategy
- [Competitor Orbits](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/competitor-orbits.md) — 4R framework, 3 competitor orbits (Core/Mid/Outer), OCS environment grading, Predator Stack attack sequence, negative content budget hack
- [Hallucination Hunting](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/hallucination-hunting.md) — AI competitor auditing, 6 query layer types, query path tracing, 3-question USP extraction, Match & Exceed vs. Introduce Unique Layers strategies
- [Content Creation Protocol](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/content-creation-protocol.md) — Competitor Analysis (USPs + angles), Query Analysis (customer language, real intent, constraints), Master Prompt template
- [Prompt Engineering](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/prompt-engineering.md) — 3 prompt elements (Context/Constraints/Format), 5 pro-tips (Role, Filter Bypass, Memory Clear, Anti-Agree, Source Unlock), AEO prompt templates
- [AEO Writing Framework](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/aeo-writing-framework.md) — A.Q.C.E. formula (Answer/Qualify/Cover/Extend), semantic HTML requirements, Information Gain check, quality checklist
- [AEO FAQ Framework](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/aeo-faq-framework.md) — 5 FAQ rules, 4-sentence template (Declarative/Clarification/Guardrail/Brand), hallucination-proof topic discovery
- [GEO Tactical Strategies](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/geo-tactical-strategies.md) — Snippable content, E.E.A.T. upfront, schema markup templates, multi-platform authority, AI bot indexing, content freshness

## Next Best Skill

- **Primary**: [geo-content-optimizer](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/build/geo-content-optimizer/SKILL.md) — execute tactical GEO optimization on content identified by the AEO audit.
- **Secondary**: [first-sentence-engine](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/build/first-sentence-engine/SKILL.md) — restructure content openings for answer-first, passage-level extraction.
- **For brand entity issues**: [entity-optimizer](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/cross-cutting/entity-optimizer/SKILL.md) — resolve AI entity recognition and disambiguation.
