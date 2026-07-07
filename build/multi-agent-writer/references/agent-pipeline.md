# Multi-Agent Semantic Writing System — Agent Pipeline

Full specification for all 15 agents. Each agent completes its task before the next starts. The pipeline converts a content brief into a complete, entity-rich, semantic SEO content draft.

Source framework: [Chapter 5: Semantic Content Writing Framework](https://www.mubashirhassan.com/seo/chapter5.html)

---

## Phase 1: Content Brief Interpreter

### Role

Reads the user's content brief and extracts the page's core direction. This agent does not write content — it only prepares the strategy.

### Task

Identify and extract:

- Central entity
- Primary keyword
- Secondary keywords
- Search intent
- Audience
- Page type
- Main user problem
- Calculator/tool/product/service purpose
- Required sections
- Required facts
- Required tables
- Internal links
- External source needs
- Word count
- Tone
- Restrictions

### Output Format

```text
Central Entity:
Primary Keyword:
Secondary Keywords:
Page Type:
Search Intent:
Target Audience:
Macro Context:
User Problem:
Main Outcome:
Required Sections:
Required Facts:
Required Entities:
Required Tables:
Required Examples:
Internal Links:
External Evidence Needed:
Tone:
Restrictions:
```

### Quality Rule

Do not write any article content. Output the strategy summary only.

---

## Phase 2: Macro Context Controller

### Role

Protects the page from topic drift. Chapter 5 says each page should have exactly one macro context because multi-topic pages confuse semantic understanding.

### Task

Define what belongs and what does not belong on the page:

- Does every section support the H1?
- Does every entity support the central entity?
- Does every heading deepen the same topic?
- Are there unrelated subtopics?
- Is the page informational, commercial, or mixed?
- Are product/service mentions allowed?
- Should some sections become separate pages?

### Output Format

```text
Approved Macro Context:
Allowed Subtopics:
Restricted Subtopics:
Entities to Include:
Entities to Avoid:
Content Boundary:
Reasoning:
```

### Example

For a page about **Wheelchair Ramp Slope Calculator**:

**Allowed**: wheelchair ramp slope, rise, run, ramp length, 1:12 slope, ADA-style guidance, landings, handrails, metric conversion, residential ramp slope.

**Avoid**: car ramps, driveway slope, roof pitch, pipe slope, ladder angle, medical advice, wheelchair product reviews.

---

## Phase 3: Entity & Attribute Research Agent

### Role

Builds the semantic entity map. Chapter 5 says content should include more relevant entities and attribute values as long as they support the macro context.

### Task

Build a full entity network:

- Central entity
- Parent entity
- Child entities
- Sibling entities
- Supporting entities
- Attributes
- Values
- Units
- Measurements
- Use cases
- Problems
- Comparisons
- Rules
- Examples

### EVA Triple Rule

Every factual sentence should express a clear Entity→Attribute→Value relationship.

**Example EVA Triples**:

| Entity | Attribute | Value |
|--------|-----------|-------|
| Wheelchair ramp slope | formula | rise ÷ run |
| 1:12 slope | percent grade | 8.33% |
| ADA ramp run | maximum rise | 30 inches |
| Ramp length | formula | √(rise² + run²) |

### Output Format

```text
Central Entity:
Parent Entity:
Child Entities:
Sibling Entities:
Supporting Entities:
Attributes:
Attribute Values:
Measurement Units:
Use Cases:
Problems:
Comparisons:
Required EVA Triples:
Missing Entity Gaps:
```

---

## Phase 4: SERP Intent Mapper

### Role

Converts keywords, autocomplete terms, competitor headings, and PAA questions into content sections.

### Task

For each query, decide:

- Should this query be answered in an H2?
- Should this query be answered in an H3?
- Should this query become an FAQ?
- Should this query become a table?
- Should this query become a formula?
- Should this query become an example?
- Should this query be ignored because it breaks macro context?

### Priority Scale

| Priority | Meaning |
|----------|---------|
| 10 | Must answer in main content |
| 8–9 | Important section or H3 |
| 6–7 | FAQ or supporting paragraph |
| 4–5 | Related but minor |
| 1–3 | Avoid or mention briefly |

### Output Format

| Query | Intent | Priority | Best Placement | Answer Format | Required Entities | Required Facts |
|-------|--------|----------|---------------|---------------|-------------------|----------------|

### Rules

- Main intent queries should become H2s or important H3s
- Repeated queries should be merged
- Weak or unrelated queries should be removed
- Every query must support the page macro context

---

## Phase 5: Evidence Research Agent

### Role

Finds and organizes facts, data, definitions, formulas, standards, studies, and authoritative sources. Chapter 5 recommends using research papers, university studies, government data, and authoritative sources to support claims.

### Source Priority

Use sources in this order:

1. Government sources
2. Official standards
3. University sources
4. Peer-reviewed research
5. Established industry organizations
6. Competitor pages only for gap analysis, not facts

### Output Format

```text
Fact:
Entity:
Attribute:
Value:
Source Needed:
Preferred Source Type:
Citation Placement:
Confidence Level:
```

### Rules

- Use government, official, university, or authoritative sources where possible
- Do not use competitor pages as primary factual sources
- Mark unsupported claims as "needs verification"
- Do not write the article yet

---

## Phase 6: Context Vector Architect

### Role

Creates the H1→H2→H3 structure. Chapter 5 says the content should create a proper context vector, where the H1 defines the macro context and every heading deepens the same context.

### Correct Heading Flow

1. Definition
2. Calculator/tool explanation
3. Formula
4. Core standard or rule
5. Charts/tables
6. Use cases
7. Examples
8. Mistakes
9. Related calculators/resources
10. FAQs

### Bad Heading Flow (avoid)

- Definition → Random product pitch
- Unrelated comparison
- Advanced formula before basic explanation
- FAQ before main content
- Competitor copy structure

### Output Format

```text
H1:
  Intro Purpose:
  H2:
    H3:
    H3:
  H2:
    H3:
    H3:
  ...
```

### Rules

- H1 must include the central entity and main attribute
- Each H2 must deepen the H1
- Each H3 must support its parent H2
- Start with definition and tool purpose
- Place formulas before examples
- Place FAQs after the main content
- Do not add unrelated sections
- Use question-style headings where useful

---

## Phase 7: Featured Snippet & Direct Answer Agent

### Role

Creates direct answer blocks for every important heading. Chapter 5 says the answer should appear immediately after the question, and key answer blocks should stay around 40 words for snippet extraction.

### Answer Block Formula

```text
[Entity] + [direct predicate] + [value/outcome].
[Qualifier or condition].
[Example, formula, or use case].
```

### Example

> A wheelchair ramp slope measures vertical rise against horizontal run. A 1:12 slope needs 12 inches of run for every 1 inch of rise. This ratio equals 8.33% grade.

### Output Format

```text
Heading:
Direct Answer:
Expansion:
Example/Qualifier:
```

### Rules

- Answer immediately after the heading
- Keep the first answer under 40 words where possible
- Use the central entity clearly
- Avoid vague openings
- Do not start with filler phrases
- Bold the answer or key fact, not the keyword
- Use factual sentence structure

---

## Phase 8: Semantic Content Writer

### Role

Writes the full article using all outputs from Phases 1–7.

### Writing Rules

From Chapter 5:

- Use factual sentence structures
- Use short sentences
- Remove fluff
- Use direct declarations
- Avoid contextless words
- Use lists and tables
- Use definitions, signifiers, and qualifiers
- Use exact numbers
- Give examples after plural nouns
- Use same part of speech in lists
- Put the condition after the main clause
- Bold the answer, not the keyword
- Avoid product promotion on informational pages

### Sentence Formula

Use: `Entity + predicate + object/value.`

**Good**: Wheelchair ramp slope measures vertical rise against horizontal run.

**Bad**: It is basically something that can be really helpful when trying to understand how steep a ramp might be.

### Banned Words

Remove: really, very, quite, just, basically, simply, actually, literally, honestly, obviously, clearly, definitely, certainly, probably, generally, usually, overall, importantly.

### Output

Full content in clean markdown with proper heading hierarchy.

---

## Phase 9: Structured Data Writer

### Role

Adds extraction-friendly tables, formulas, lists, and worked examples. Chapter 5 recommends ordered and unordered lists because they help Google extract structured information.

### Required Elements

- Definition tables
- Formula blocks with variable definitions
- Comparison tables
- Step-by-step examples
- Measurement tables
- Mistake tables
- Status tables
- Calculator input/output tables

### Rules

- Every table must have a short context sentence before it
- Every formula must define its variables
- Every example must show input, calculation, and result
- Do not add tables only for decoration
- Keep the structure aligned with the macro context

---

## Phase 10: EVA Triple Auditor

### Role

Checks whether factual sentences can be converted into semantic triples. Chapter 5 says EVA — Entity, Attribute, Value — is the foundational unit of semantic content.

### Audit Format

```text
Original Sentence:
Problem:
EVA Triple: Entity → Attribute → Value
Improved Sentence:
```

### Example

**Weak**: It is useful for planning.

**Improved**: A wheelchair ramp slope calculator estimates required ramp run from vertical rise and slope ratio.

**Triple**: Wheelchair ramp slope calculator → estimates → required ramp run

### Rules

- Replace "it," "this," and "they" when the entity is unclear
- Replace weak verbs with specific predicates
- Add numeric values where needed
- Keep sentences short

---

## Phase 11: Discourse Integration Editor

### Role

Checks paragraph flow and context continuity. Chapter 5 warns against breaking context across paragraphs and breaking the information graph.

### Checks

- Does each paragraph continue the previous idea?
- Does each H3 support the H2?
- Does each H2 support the H1?
- Are transitions logical?
- Are there abrupt topic jumps?
- Are examples placed after the concept they explain?

### Output Format

```text
Context Flow Issues:
Recommended Fixes:
Rewritten Sections:
```

---

## Phase 12: Internal Linking Strategist

### Role

Adds contextual internal links. Chapter 5 says internal links should use anchor text that describes the relationship between source and target pages.

### Output Format

| Source Section | Anchor Text | Target URL | Placement Sentence | Reason | Priority |
|---------------|-------------|------------|-------------------|--------|----------|

### Rules

- Use fewer but stronger links
- Anchor text must describe the target page
- The source section and target page must share entity context
- Do not add irrelevant links
- Avoid exact-match overuse
- Avoid generic anchors like "click here"
- Place links where they help the user
- Do not overlink the same page

---

## Phase 13: Technical Semantic SEO Agent

### Role

Creates title, meta description, URL, image SEO, schema, and semantic HTML suggestions. Chapter 5 says technical elements must align with the content's entity and contextual strategy.

### Output Format

```text
Title Tag:
Meta Description:
H1:
URL Slug:
Featured Image Filename:
Featured Image Alt Text:
Supporting Image Alt Texts:
Recommended Schema:
FAQ Schema Questions:
Breadcrumb:
Semantic HTML Structure:
```

### Rules

- Title tag must include entity + attribute + modifier
- Meta description must include main entity, supporting entity, benefit, and CTA
- H1 must define the macro context
- URL must be clean and entity-based
- Image alt text must describe entity + attribute
- Schema must connect the page's entities

---

## Phase 14: FAQ Extraction Agent

### Role

Writes concise FAQ answers from the content brief and draft.

### Rules

- Answer directly
- Do not repeat the question in full
- Use the entity clearly
- Use numeric values where available
- Keep answers under 40 words where possible
- Avoid long explanations
- Avoid sales language
- Create 6–10 FAQs

### Output Format

```text
FAQ 1:
Question:
Answer:

FAQ 2:
Question:
Answer:
```

---

## Phase 15: Final Semantic SEO Auditor

### Role

Gives the final quality score and fixes weak areas.

### Audit Criteria

| Criterion | Weight |
|-----------|--------|
| Macro Context Clarity | /10 |
| Entity Coverage | /10 |
| Attribute-Value Coverage | /10 |
| Factual Sentence Structure | /10 |
| Answer-First Structure | /10 |
| EVA Triple Clarity | /10 |
| Heading Hierarchy | /10 |
| Discourse Flow | /10 |
| Table and List Quality | /5 |
| Examples and Formulas | /5 |
| Internal Linking | /5 |
| Technical SEO Alignment | /5 |
| Schema Alignment | /5 |
| Fluff Removal | /5 |

**Total: /100**

### Output Format

```text
Macro Context: /10
Entity Coverage: /10
Attribute-Value Coverage: /10
Factual Sentence Structure: /10
Answer-First Structure: /10
EVA Triple Clarity: /10
Heading Hierarchy: /10
Discourse Flow: /10
Table and List Quality: /5
Examples and Formulas: /5
Internal Linking: /5
Technical SEO: /5
Schema Alignment: /5
Fluff Removal: /5

Passed Checks:
Failed Checks:
Exact Fixes Needed:
Final Rewritten Improvements:
Final Score: /100
```

### Scoring Guide

| Score Range | Verdict |
|-------------|---------|
| 90–100 | Publish-ready. Minimal edits. |
| 75–89 | Strong draft. Fix flagged items before publishing. |
| 60–74 | Needs revision. Multiple sections require rewriting. |
| Below 60 | Major rewrite. Re-run agents 8–11. |
