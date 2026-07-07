---
name: multi-agent-writer
description: 'Use when the user asks to "write semantic content", "run writing system", "multi-agent writing", "write from brief", "semantic SEO draft", "rank within days", "@writing". Runs a 15-agent pipeline that converts a content brief into a complete semantic SEO draft with EVA triples, answer-first blocks, entity maps, and technical SEO. For single-section openings, see first-sentence-engine. For GEO-only passes, see geo-content-optimizer.'
version: "9.1.0"
license: Apache-2.0
compatibility: "Claude Code ≥1.0, skills.sh marketplace, ClawHub marketplace, Vercel Labs skills ecosystem. No system packages required."
homepage: "https://github.com/aaron-he-zhu/seo-geo-claude-skills"
when_to_use: "Use when the user provides a content brief and wants a complete semantic SEO article that ranks fast. Also when the user says @writing, asks for multi-agent content, entity-rich articles, EVA-triple-based writing, or wants content optimized for both Google NLP and AI answer engines."
argument-hint: "<content brief or topic>"
metadata:
  author: aaron-he-zhu
  version: "9.1.0"
  geo-relevance: "high"
  tags:
    - seo
    - geo
    - semantic-writing
    - multi-agent
    - content-brief
    - eva-triples
    - entity-seo
    - answer-first
    - featured-snippet
    - ai-citation
    - content-creation
    - semantic-seo
    - macro-context
    - 语义写作
    - マルチエージェント
    - redaccion-semantica
  triggers:
    # EN-formal
    - "multi-agent writing"
    - "semantic SEO writing"
    - "write from content brief"
    - "run writing system"
    - "semantic content draft"
    - "entity-rich article"
    - "EVA triple writing"
    - "write semantic content"
    - "content brief to article"
    - "15-agent writing pipeline"
    # EN-casual
    - "@writing"
    - "write me a ranking article"
    - "write content that ranks fast"
    - "create an article from my brief"
    - "help me write world-class content"
    - "write an article that ranks within days"
    - "turn this brief into content"
    - "use the writing system"
    # EN-question
    - "how to write content that ranks fast"
    - "how to create semantic SEO content"
    - "how to write entity-rich articles"
    - "what is EVA triple writing"
    # ZH-pro
    - "语义SEO写作"
    - "多代理写作系统"
    - "实体写作"
    - "内容简报转文章"
    # ZH-casual
    - "帮我写排名文章"
    - "用写作系统写文章"
    - "写一篇能快速排名的文章"
    # JA
    - "セマンティックSEOライティング"
    - "マルチエージェント記事作成"
    - "コンテンツブリーフから記事"
    - "エンティティSEO"
    # KO
    - "시맨틱 SEO 글쓰기"
    - "멀티에이전트 글쓰기"
    - "콘텐츠 브리프에서 기사"
    - "빠르게 순위 올리는 글"
    # ES
    - "escritura semántica SEO"
    - "sistema de escritura multi-agente"
    - "redacción desde brief"
    # PT
    - "redação semântica SEO"
    - "sistema multi-agente de escrita"
    # Misspellings
    - "multi agent writting"
    - "semantic SEO writting"
    - "EVA tripple writing"
---

# Multi-Agent Semantic Writing System

> **[SEO & GEO Skills Library](https://github.com/aaron-he-zhu/seo-geo-claude-skills)** · 22 skills for SEO + GEO · [ClawHub](https://clawhub.ai/u/aaron-he-zhu) · [skills.sh](https://skills.sh/aaron-he-zhu/seo-geo-claude-skills)
> **System Mode**: This build skill follows the shared [Skill Contract](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/skill-contract.md) and [State Model](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/state-model.md).

This skill runs a **15-agent pipeline** that converts a content brief into a complete, entity-rich, semantic SEO content draft. Every agent completes its task before the next agent starts. The output is optimized for Google NLP extraction, AI Overview citation, featured snippets, and human readability.

**System role**: Build layer skill. It orchestrates 15 internal agents that transform a content brief into a publication-ready semantic article.

## When This Must Trigger

Use this when the conversation involves producing a complete article from a content brief — even if the user doesn't use semantic SEO terminology:

- User provides a content brief and wants a full article
- User says `@writing` or asks to "run the writing system"
- User wants entity-rich content that ranks fast
- User asks for EVA-triple-based or answer-first content
- User wants a multi-agent content pipeline
- User needs content optimized for both search and AI citation

## What This Skill Does

1. **Brief Interpretation**: Extracts central entity, keywords, intent, audience, and constraints
2. **Macro Context Protection**: Defines one context boundary to prevent topic drift
3. **Entity & Attribute Mapping**: Builds semantic entity network with EVA triples
4. **Query-to-Section Mapping**: Maps keywords and PAA questions to headings
5. **Evidence Planning**: Identifies claims needing authoritative sources
6. **Heading Architecture**: Creates H1→H2→H3 context vector
7. **Direct Answer Blocks**: Writes 40-word featured snippet answers
8. **Semantic Draft Writing**: Writes the full article with factual sentence structures
9. **Structured Data**: Adds tables, formulas, examples, comparison charts
10. **EVA Triple Audit**: Verifies Entity→Attribute→Value clarity
11. **Discourse Flow**: Checks paragraph and section continuity
12. **Internal Linking**: Suggests contextual links with exact placements
13. **Technical SEO**: Generates title, meta, slug, schema, image SEO
14. **FAQ Extraction**: Creates 6–10 concise FAQ answers
15. **Final Audit**: Scores the draft out of 100 and fixes weak areas

## Quick Start

Start with one of these prompts. Finish with a short handoff summary using the repository format in [Skill Contract](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/skill-contract.md).

### From a Content Brief

```
@writing Here is my content brief: [paste brief]
```

### Quick Topic

```
Run the multi-agent writing system for "wheelchair ramp slope calculator" targeting informational intent
```

### With Specific Requirements

```
@writing Write a 3,000-word semantic SEO article about [topic] targeting [keyword], include calculator tables and ADA standards
```

## Skill Contract

**Expected output**: a complete semantic SEO content draft with metadata, entity map, EVA audit, internal links, schema, FAQs, and quality score, plus a short handoff summary ready for `memory/content/`.

- **Reads**: the content brief, target keywords, entity inputs, quality constraints, and prior decisions from [CLAUDE.md](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/CLAUDE.md) and the shared [State Model](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/state-model.md) when available.
- **Writes**: a complete article draft with all 15-agent outputs plus a reusable summary that can be stored under `memory/content/`.
- **Promotes**: content strategy decisions, entity maps, EVA findings, and audit scores to `memory/hot-cache.md`, `memory/decisions.md`, and `memory/open-loops.md`.
- **Next handoff**: use the `Next Best Skill` below when the draft is ready for quality gate review.

### Handoff Summary

Emit this shape when finishing the skill (see [skill-contract.md §Handoff Summary Format](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/skill-contract.md) for the authoritative format):

- **Status**: DONE / DONE_WITH_CONCERNS / BLOCKED / NEEDS_INPUT
- **Objective**: what was analyzed, created, or fixed
- **Key Findings / Output**: the highest-signal result
- **Evidence**: URLs, data points, or sections reviewed
- **Open Loops**: blockers, missing inputs, or unresolved risks
- **Recommended Next Skill**: one primary next move

## Core Principles

The system follows the Chapter 5 semantic writing framework:

- **One macro context per page** — multi-topic pages confuse semantic understanding
- **Entity-Attribute-Value (EVA) triples** — every factual sentence expresses Entity→Attribute→Value
- **Factual sentence structures** — use "X does Y" not vague filler
- **Direct answers immediately after headings** — answer first, explain second
- **Short sentences** — remove words that add no meaning
- **40-word answer blocks** — optimized for featured snippet extraction
- **Consistent technical alignment** — title, H1, URL, schema, internal links, images all support the same entity
- **No product promotion on informational pages** — keep content unbiased

Source: [Chapter 5: Semantic Content Writing Framework](https://www.mubashirhassan.com/seo/chapter5.html)

## Instructions

When a user provides a content brief, run all 15 agents in sequence. Each agent must complete before the next starts.

> **Reference**: See [references/agent-pipeline.md](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/build/multi-agent-writer/references/agent-pipeline.md) for the full agent prompts, output formats, quality rules, and worked examples.

### Phase Summary

| Phase | Agent | Task |
|-------|-------|------|
| 1 | Content Brief Interpreter | Extract strategy from brief |
| 2 | Macro Context Controller | Define single context boundary |
| 3 | Entity & Attribute Researcher | Build entity map and EVA triples |
| 4 | SERP Intent Mapper | Map queries to sections |
| 5 | Evidence Research Agent | Identify source requirements |
| 6 | Context Vector Architect | Create heading hierarchy |
| 7 | Featured Snippet Agent | Write direct answer blocks |
| 8 | Semantic Content Writer | Write the full draft |
| 9 | Structured Data Writer | Add tables, formulas, examples |
| 10 | EVA Triple Auditor | Audit entity-attribute-value clarity |
| 11 | Discourse Integration Editor | Check context flow |
| 12 | Internal Linking Strategist | Add contextual internal links |
| 13 | Technical Semantic SEO Agent | Generate metadata and schema |
| 14 | FAQ Extraction Agent | Create concise FAQs |
| 15 | Final Semantic SEO Auditor | Score and fix the draft |

### Writing Rules

These rules apply throughout all 15 phases:

- Use one macro context per page
- Focus on entities, not just keywords
- Use factual sentence structures: "X does Y"
- Answer first, explain second
- Do not distance the question from the answer
- Use short sentences
- Remove words that add no meaning
- Use exact numbers, values, percentages, formulas, and units
- Use definitions, signifiers, and qualifiers
- Give examples after plural nouns
- Use the same part of speech in lists
- Put "if" conditions after the main clause
- Bold answers, not keywords
- Avoid unnecessary links
- Do not promote products on informational pages
- Every factual sentence should be convertible into an EVA triple

### Sentence Formula

Use: `Entity + predicate + object/value.`

**Good**: Wheelchair ramp slope measures vertical rise against horizontal run.

**Bad**: It is basically something that can be really helpful when trying to understand how steep a ramp might be.

## Validation Checkpoints

### Input Validation
- [ ] Content brief provided with identifiable topic and keyword
- [ ] Search intent determinable (informational, commercial, transactional)
- [ ] Audience and page type identifiable
- [ ] At least one central entity extractable

### Output Validation
- [ ] **Banned-vocab self-check** — scan for: `crucial, robust, leverage, delve, nuanced, multifaceted, furthermore, moreover, pivotal, tapestry, foster, showcase, intricate, vibrant, cutting-edge, harness, elevate, empower, streamline, synergy, holistic, seamless, seamlessly, realm, paramount, myriad`. Also banned phrases: `In today's digital landscape`, `It is important to note`, `It's worth noting that`, `Let's dive in`, `Without further ado`, `At the end of the day`. Replace any hit with a concrete alternative.
- [ ] Single macro context maintained throughout
- [ ] EVA triples audited on all factual sentences
- [ ] Direct answer within 40 words under every H2
- [ ] Entity coverage matches entity map from Phase 3
- [ ] Heading hierarchy follows context vector (Phase 6)
- [ ] Internal links use descriptive anchors matching target entity
- [ ] FAQ answers under 40 words each
- [ ] Technical SEO elements align with content entity strategy
- [ ] Final audit score ≥ 75/100

## Final Output Structure

The complete deliverable contains:

```text
A. Content Strategy Summary
B. Macro Context Definition
C. Entity & Attribute Map
D. Query-to-Section Map
E. Evidence Requirements
F. Heading Structure
G. Full SEO Content Draft
H. Tables / Formulas / Examples
I. FAQs (6–10)
J. Internal Linking Suggestions with Exact Locations
K. Meta Title
L. Meta Description
M. URL Slug
N. Image SEO
O. Schema Suggestions
P. Final Semantic SEO Audit (score /100)
```

### Final Instruction

Every section must reduce the cost of retrieval for Google, AI Overviews, featured snippets, and LLM answer engines. If a sentence does not add extractable information, remove it. Write like a semantic information architect, not a blog writer.

### Save Results

After delivering the content draft to the user, ask:

> "Save these results for future sessions?"

If yes, write a dated summary to `memory/content/YYYY-MM-DD-<topic>.md` containing:
- One-line description of what was created
- Target keyword and content type
- Entity map summary
- EVA coverage score
- Final audit score
- Open loops or items needing review

**Gate check recommended**: Run content-quality-auditor before publishing (PostToolUse hook will remind automatically).

If any findings should influence ongoing strategy, recommend promoting key conclusions to `memory/hot-cache.md`.

## Reference Materials

- [Agent Pipeline](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/build/multi-agent-writer/references/agent-pipeline.md) — Full 15-agent prompts, output formats, quality rules, and worked examples
- [Master Prompt](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/build/multi-agent-writer/references/master-prompt.md) — Copy-paste prompt for any LLM
- [Chapter 5 Source](https://www.mubashirhassan.com/seo/chapter5.html) — Original semantic content writing framework

## Next Best Skill

- **Primary**: [content-quality-auditor](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/cross-cutting/content-quality-auditor/SKILL.md) — gate the draft before publishing with full 80-item CORE-EEAT audit.
- **Alternative**: [geo-content-optimizer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/build/geo-content-optimizer/SKILL.md) — additional GEO optimization pass for AI citation readiness.
