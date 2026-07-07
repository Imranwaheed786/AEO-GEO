---
name: first-sentence-engine
description: 'Use when the user asks to "write section openings", "first sentence optimization", "snippet-ready introductions", "answer-first writing", "optimize section starts". Generates entity-first section openings optimized for featured snippets, AI answer extraction, and passage-level retrieval. For full articles, see seo-content-writer. For AI citation optimization, see geo-content-optimizer.'
version: "9.0.0"
license: Apache-2.0
compatibility: "Claude Code ≥1.0, skills.sh marketplace, ClawHub marketplace, Vercel Labs skills ecosystem. No system packages required."
homepage: "https://github.com/aaron-he-zhu/seo-geo-claude-skills"
when_to_use: "Use when writing or rewriting section openings for tool pages, calculator pages, SaaS pages, product pages, blog articles, or comparison pages. Also when the user wants answer-first content, snippet-optimized introductions, or entity-forward section starts."
argument-hint: "<page type> <entity/tool name>"
metadata:
  author: aaron-he-zhu
  version: "9.0.0"
  geo-relevance: "high"
  tags:
    - seo
    - geo
    - first-sentence
    - section-opening
    - featured-snippet
    - answer-first
    - passage-retrieval
    - ai-citation
    - content-writing
    - tool-page-content
    - calculator-content
    - snippet-optimization
    - セクション最適化
    - 段落开头优化
    - redaccion-seo
  triggers:
    # EN-formal
    - "first sentence optimization"
    - "write section openings"
    - "optimize section introductions"
    - "answer-first writing"
    - "snippet-ready introductions"
    - "entity-first content"
    - "passage-level optimization"
    - "section opening formula"
    # EN-casual
    - "write me better section starts"
    - "how should I start each section"
    - "my section openings are weak"
    - "make my intros snippet-ready"
    - "fix my section beginnings"
    - "help me start sections better"
    # EN-question
    - "how do I write section openings for SEO"
    - "what makes a good first sentence"
    - "how to get featured snippets"
    - "how to write for AI extraction"
    # ZH-pro
    - "段落开头优化"
    - "首句优化"
    - "精选摘要写作"
    - "回答优先写作"
    # ZH-casual
    - "怎么写段落开头"
    - "帮我优化开头句"
    - "第一句话怎么写"
    # JA
    - "セクション最適化"
    - "冒頭文の書き方"
    - "スニペット最適化"
    - "回答ファースト"
    # KO
    - "섹션 시작 최적화"
    - "첫 문장 최적화"
    - "스니펫 최적화"
    - "답변 우선 작성"
    # ES
    - "optimización de primera oración"
    - "redacción de aperturas"
    - "escritura orientada a snippets"
    # PT
    - "otimização de primeira frase"
    - "abertura de seção SEO"
    # Misspellings
    - "first sentance optimization"
    - "snippit ready introductions"
    - "passage retreival optimization"
---

# First Sentence Engine

> **[SEO & GEO Skills Library](https://github.com/aaron-he-zhu/seo-geo-claude-skills)** · 21 skills for SEO + GEO · [ClawHub](https://clawhub.ai/u/aaron-he-zhu) · [skills.sh](https://skills.sh/aaron-he-zhu/seo-geo-claude-skills)
> **System Mode**: This build skill follows the shared [Skill Contract](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/skill-contract.md) and [State Model](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/state-model.md).

This skill generates section openings using first-sentence logic optimized for semantic SEO, passage-level retrieval, featured snippets, AI answer extraction, and query intent alignment. It applies to tool pages, calculator pages, SaaS pages, product pages, blog articles, and comparison pages.

**System role**: Build layer skill. It crafts entity-first, answer-first section openings that feed directly into quality review, deployment, or monitoring.

## When This Must Trigger

Use this when the conversation involves writing or rewriting section openings — even if the user doesn't mention snippets or SEO:

- Writing H2/H3 section openings for tool or calculator pages
- Rewriting weak or generic section introductions
- Optimizing content for featured snippet extraction
- Making section starts quotable by AI systems
- Writing entity-forward content for product or SaaS pages
- Creating answer-first section patterns for any content type

## What This Skill Does

1. **Entity-First Openings**: Places the central entity in the first 5 words
2. **Direct Answer Delivery**: Satisfies search intent in the opening sentence
3. **Mechanism Integration**: Explains how/why immediately after the answer
4. **Intent Mapping**: Matches sentence patterns to query intent type
5. **Snippet Targeting**: Formats for featured snippet and AI extraction
6. **Banned Pattern Enforcement**: Rejects filler, vague pronouns, and generic intros

## Quick Start

Start with one of these prompts. Finish with a short handoff summary using the repository format in [Skill Contract](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/skill-contract.md).

### Basic Section Opening

```
Write section openings for a [tool name] page with H2s: What is, How it works, Why use it
```

### Rewrite Existing Openings

```
Rewrite these section openings using answer-first logic: [paste sections]
```

### With Specific Intent

```
Write informational section openings for a BMI calculator page targeting "BMI calculator"
```

## Skill Contract

**Expected output**: entity-first section openings ready for integration plus a short handoff summary ready for `memory/content/`.

- **Reads**: the page type, entity/tool name, target keyword, section headings (H2/H3), query intent, and prior decisions from [CLAUDE.md](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/CLAUDE.md) and the shared [State Model](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/state-model.md) when available.
- **Writes**: entity-first section openings (1–3 sentences per section) plus a reusable summary that can be stored under `memory/content/`.
- **Promotes**: approved sentence patterns, intent mapping decisions, and rewrite blockers to `memory/hot-cache.md`, `memory/decisions.md`, and `memory/open-loops.md`.
- **Next handoff**: use the `Next Best Skill` below when the openings are ready for full content writing or quality review.

### Handoff Summary

Emit this shape when finishing the skill (see [skill-contract.md §Handoff Summary Format](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/references/skill-contract.md) for the authoritative format):

- **Status**: DONE / DONE_WITH_CONCERNS / BLOCKED / NEEDS_INPUT
- **Objective**: what was analyzed, created, or fixed
- **Key Findings / Output**: the highest-signal result
- **Evidence**: URLs, data points, or sections reviewed
- **Open Loops**: blockers, missing inputs, or unresolved risks
- **Recommended Next Skill**: one primary next move

## Core Rule

The first sentence of every section must contain:

1. **Central Entity** — the tool, product, or concept name
2. **Direct Answer** — what it does or why it matters
3. **Mechanism / Differentiator** — how it works or what sets it apart

**Formula**: `[Entity] + [Direct Answer] + [Mechanism / Qualification]`

**Advanced Formula**: `[Entity] + [Outcome] + [Mechanism] + [Context]`

## Instructions

When a user requests section openings, run these steps in order:

1. **Identify Page Type** — tool, calculator, SaaS, product, blog, or comparison
2. **Map Query Intent** — classify each section heading as informational, procedural, comparison, or decision
3. **Apply Intent Pattern** — use the matching sentence formula (see Query Intent Mapping below)
4. **Write 1–3 Sentences Per Section** — sentence 1 = direct answer, sentence 2 = mechanism, sentence 3 = practical benefit
5. **Validate Each Opening** — run the Output Validation Checklist
6. **Enforce Writing Constraints** — reject banned patterns, fix vague pronouns, remove filler
7. **Final Review** — confirm entity placement, intent satisfaction, and mechanism presence

## Query Intent Mapping

### Informational Query

**Pattern**: Entity + Definition + Mechanism

**Example**: A shoe size calculator estimates foot measurements by analyzing length and width to improve fitting accuracy.

### Procedural Query

**Pattern**: Entity + Action + Outcome

**Example**: A BMI calculator calculates body mass index by comparing weight and height to assess body composition.

### Comparison Query

**Pattern**: Entity + Contrast + Use Case

**Example**: A pace calculator differs from a speed calculator by focusing on time per distance rather than distance over time.

### Decision Query

**Pattern**: Entity + Judgment + Condition

**Example**: A calorie calculator is useful for weight management when daily energy intake needs accurate planning.

## Tool Page Patterns

### What is [Tool]

**Pattern**: `[Tool Name] helps users [solve outcome] by [mechanism].`

**Example**: A loan calculator estimates monthly repayments by applying interest rates, loan terms, and principal balance.

### How does [Tool] work

**Pattern**: `[Tool Name] works by [mechanism] to [outcome].`

**Example**: A time duration calculator works by subtracting timestamps to measure exact elapsed time.

### Why use [Tool]

**Pattern**: `[Tool Name] improves [benefit] by [mechanism].`

**Example**: A fuel cost calculator improves trip budgeting by combining mileage, fuel price, and travel distance.

### Accuracy Section

**Pattern**: `[Tool Name] provides accurate estimates when [condition].`

**Example**: A pregnancy calculator provides accurate due dates when the last menstrual cycle date is entered correctly.

## Tool Content Rules

For tool-based content, every H2 must begin with:

- **1st sentence** → direct answer
- **2nd sentence** → mechanism
- **3rd sentence** → practical benefit

Structure: Sentence 1 = answer first. Sentence 2 = explain why. Sentence 3 = explain value.

## Writing Constraints

**Do not**:
- Start with generic introductions
- Use filler
- Delay answers
- Use vague pronouns
- Hide entity names

**Banned openers**:
- "Nowadays..."
- "In today's world..."
- "It is important to..."
- "There are many ways..."

## Validation Checkpoints

### Output Validation Checklist

Before finalizing each section opening:

- [ ] Is the entity in the first 5 words?
- [ ] Is the answer immediate?
- [ ] Is there a mechanism or differentiator?
- [ ] Is the sentence specific (no vague language)?
- [ ] Does it satisfy the mapped search intent?
- [ ] Is it free of banned openers and filler?

### Best Practice Targets

Each section opening must:

✓ Mention the exact entity
✓ Satisfy search intent fast
✓ Explain mechanism
✓ Provide context

Target: snippet extraction, AI visibility, semantic relevance, answer-first writing.

### Save Results

After delivering section openings to the user, ask:

> "Save these results for future sessions?"

If yes, write a dated summary to `memory/content/YYYY-MM-DD-<topic>.md` containing:
- One-line description of what was created
- Page type and entity name
- Intent patterns applied
- Open loops or items needing review

**Gate check recommended**: Run content-quality-auditor before publishing (PostToolUse hook will remind automatically).

If any findings should influence ongoing strategy, recommend promoting key conclusions to `memory/hot-cache.md`.

## Next Best Skill

- **Primary**: [seo-content-writer](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/build/seo-content-writer/SKILL.md) — expand the section openings into full content.
- **Alternative**: [content-quality-auditor](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/cross-cutting/content-quality-auditor/SKILL.md) — gate the draft before publishing or handing it off.
