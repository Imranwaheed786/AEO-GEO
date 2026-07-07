# LLM Ranking Mechanics — Tactical AEO Execution

This reference document covers the three tactical techniques for manipulating how Large Language Models select, evaluate, and cite your content. These are the execution-level hacks that sit on top of the strategic AEO framework.

## Overview: How LLMs Actually Select Content

When a user asks an LLM a question, the model does not simply search for the best article. It runs a multi-step pipeline:

1. **Fan Out** — The model internally expands the user's query into 6–8 sub-queries
2. **Chunk Retrieval** — The model searches for individual paragraphs (not pages) that answer each sub-query
3. **Filter & Rank** — The model applies three strict filters (Consistency, Consensus, Contextual Relevance) to decide which chunks to actually cite

Your content must be optimized for all three steps. Failing at any single step means the AI will skip your content entirely — even if it's the best answer available.

## Technique 1: Query Fan Out Mapping

### What It Is

When a user types a simple query like "Which goldfish should I buy?", the AI does not search for that exact phrase. It internally expands this into a "Fan Out" of 6–8 sub-queries:

- What are the common types of goldfish?
- What tank size does each type need?
- Common vs. fancy goldfish — differences?
- Goldfish maintenance tips for beginners
- What do goldfish cost?
- Best goldfish for beginners vs. experienced keepers
- Goldfish feeding requirements
- Local availability and pricing

### Why Traditional SEO Fails Here

Traditional SEO: Find a high-volume keyword → build headings around it → optimize for that single phrase.

AEO reality: If your article only answers the main query ("best goldfish to buy"), the AI will **ignore it** because it doesn't satisfy the sub-queries the model internally generated. The AI needs content that covers multiple angles of the same topic.

### How to Execute

**Step 1: Generate the Fan Out Map**

Before writing any content, map out the AI's likely sub-queries using:

- **ChatGPT/Claude**: Ask "What sub-questions would someone need answered before they can answer: [main query]?"
- **Google's "People Also Ask"**: Captures real user question patterns
- **Google's "People Also Search For"**: Shows related search clusters
- **Your own expertise**: Add domain-specific angles the tools might miss

**Step 2: Build the Fan Out Coverage Matrix**

| Sub-Query | Covered in Article? | Section/Paragraph | Autonomy Check |
|---|---|---|---|
| [Sub-query 1] | ✅ Yes / ❌ No | § [section name] | ✅ Standalone / ❌ Needs context |
| [Sub-query 2] | ✅ Yes / ❌ No | § [section name] | ✅ Standalone / ❌ Needs context |
| ... | ... | ... | ... |

**Step 3: Ensure Multi-Angle Coverage**

A single piece of content should address the topic from multiple user perspectives:

| User Level | Content Angle | Example |
|---|---|---|
| Beginner | Getting started, basics, "which one is easiest" | "If you've never owned a goldfish, start with the Common Goldfish..." |
| Intermediate | Comparison, upgrade path, common mistakes | "Once you're comfortable with water changes, Fantails offer more variety..." |
| Expert | Advanced care, breeding, rare varieties | "Butterfly Koi require precise pH between 7.0–8.0 and 30+ gallon tanks..." |

**The math**: The more sub-queries your article covers, the higher the mathematical probability it gets cited. An article covering 7/8 sub-queries will almost always beat an article covering 3/8, regardless of other quality signals.

### Fan Out Map Template

```markdown
## Fan Out Map: [Main Query]

**Target query**: [The user's primary question]
**Generated sub-queries** (aim for 6–8):

1. [Sub-query] → covered in § [section]
2. [Sub-query] → covered in § [section]
3. [Sub-query] → covered in § [section]
4. [Sub-query] → covered in § [section]
5. [Sub-query] → covered in § [section]
6. [Sub-query] → covered in § [section]
7. [Sub-query] → NOT YET COVERED — add section
8. [Sub-query] → NOT YET COVERED — add section

**Coverage score**: X/Y sub-queries covered
**Target**: ≥80% coverage before publishing
```

## Technique 2: Chunk Optimization

### How AI Ingestion Actually Works

AI models do not read or index your website page by page. They ingest and evaluate data **chunk by chunk** — paragraph by paragraph. Each chunk is independently stored, indexed, and retrieved.

### The Librarian Analogy

Think of the AI as a smart librarian. It does not want to read a 200-page book to find an answer. It wants to remember the **exact page and paragraph** where the concise answer lives. If the answer is scattered across five different paragraphs, the librarian skips your book entirely and picks the one where the answer is on a single page.

### The Problem: Scattered Information

**Bad (information scattered across 5 paragraphs)**:

> Paragraph 1: "Goldfish come in many varieties..."
> Paragraph 3: "One thing to consider is what you feed them..."
> Paragraph 7: "The feeding schedule should be..."
> Paragraph 12: "Going back to nutrition, protein content..."
> Paragraph 15: "In summary, feeding is important..."

The AI cannot efficiently stitch together scattered information. It will skip this content entirely.

### The Fix: Autonomous Chunks

**Good (complete thought in one paragraph)**:

> "Feed goldfish two to three pellets twice daily — once in the morning and once in the evening. Overfeeding is the leading cause of goldfish death (Veterinary Aquatics Association, 2024). For Fancy Goldfish varieties, reduce to two pellets per feeding due to their compressed digestive tract. Use sinking pellets for Fancy varieties and floating pellets for Common Goldfish to match their natural feeding position."

### The Chunk Autonomy Checklist

Every paragraph you write must pass all 5 checks:

- [ ] **Self-contained**: Contains a complete thought with question and answer within itself
- [ ] **No backward references**: Does not rely on "as mentioned above" or "building on the previous section"
- [ ] **No forward references**: Does not say "as we'll discuss later" or "more on this below"
- [ ] **Includes a data point**: Contains at least one specific fact, stat, date, or named source
- [ ] **Extractable**: Can be pulled out of the article and presented to a user as-is, and it would still make complete sense

### Chunk Scoring

Rate each paragraph against the 5-point checklist:

| Score | Rating | Action |
|---|---|---|
| 5/5 | Fully autonomous | Ready for AI citation |
| 4/5 | Near-autonomous | Fix the missing element |
| 3/5 | Partially dependent | Rewrite to consolidate scattered info |
| 2/5 or below | Dependent | Full rewrite needed — merge with related paragraphs |

### Before/After Example

**Before (score 2/5 — depends on prior context, no data)**:
> "As we discussed, these types are better for beginners. They're easier to care for and don't need as much attention."

**After (score 5/5 — fully autonomous)**:
> "Common Goldfish are the best choice for first-time fish owners. They tolerate temperature fluctuations between 65–75°F, survive occasional overfeeding, and require only a basic 20-gallon tank setup. Unlike Fancy Goldfish varieties (which need precise 72–74°F water and weekly 25% water changes), Common Goldfish can go 10–14 days between tank cleanings — per the American Goldfish Association's 2024 care guidelines."

## Technique 3: The Three Retrieval Filters

When the AI finds 10 paragraphs that all answer the user's question, it applies **three strict filters** to decide which one to actually show. You must pass all three.

### Filter A: Consistency (Managed Assets)

**What the AI checks**: All the platforms you control — your website, Google Business Profile, social media bios, LinkedIn company page, directory listings.

**What it looks for**: Is this entity saying the **exact same thing** about itself everywhere?

**How it fails**:

| Platform | Description | Problem |
|---|---|---|
| Website | "Premium Freshwater Fish Store" | ✅ Specific |
| Instagram Bio | "All Kinds of Pets" | ❌ Contradicts website |
| Google Business | "Pet Shop" | ❌ Too generic, doesn't match |
| Yelp Listing | "Aquarium & Fish Supplies" | ⚠️ Related but inconsistent |

The AI sees these contradictions and **drops your ranking**. It cannot confidently associate your entity with a specific topic.

**Consistency Audit Checklist (Managed Assets)**:

- [ ] Website homepage tagline
- [ ] Website About page description
- [ ] Google Business Profile description
- [ ] Instagram bio
- [ ] LinkedIn company description
- [ ] Facebook page description
- [ ] X/Twitter bio
- [ ] Directory listings (Yelp, Yellow Pages, industry-specific)
- [ ] Email signature line
- [ ] YouTube channel description

**Rule**: Use **identical core phrasing** across all managed assets. Minor variations are acceptable (e.g., character limits on Twitter), but the core positioning statement must be recognizably the same.

### Filter B: Consensus (Unmanaged Assets)

**What the AI checks**: What third parties are saying about you on platforms you do NOT control — Reddit, Trustpilot, forums, review sites, news articles, blog mentions.

**What it looks for**: Does the third-party narrative match what you claim about yourself?

**How it fails**:

| Your Claim | Third-Party Reality | AI Conclusion |
|---|---|---|
| "We specialize in goldfish" | Reviews mention buying aquarium plants | Mismatch — entity expertise unclear |
| "Premium quality products" | Reddit threads call you "budget option" | Contradiction — trust reduced |
| "Best for beginners" | Forum posts say "not beginner-friendly" | Consensus disagrees — won't recommend |

**The Hack: Active Review Management**

You must actively manage unmanaged assets — not by faking reviews, but by reshaping the context:

1. **Reply to misleading reviews**: If a review says "Great aquarium plants!", reply with: "We're glad you loved the plants for your freshwater fish tank! Our goldfish customers often add live plants to their tank setups." This re-establishes the goldfish context for the AI.

2. **Encourage on-topic reviews**: Ask satisfied goldfish customers specifically to mention goldfish in their reviews.

3. **Participate in forums**: Contribute genuine expertise in forums under your brand name, consistently reinforcing your positioning.

4. **Monitor brand mentions**: Track what's being said and correct factual errors promptly.

**Consensus Gap Analysis Template**:

| Source | What They Say | Aligned with Your Claim? | Action |
|---|---|---|---|
| Trustpilot Review #1 | "Great goldfish selection" | ✅ Yes | None |
| Reddit r/Aquariums | "Good plant selection" | ⚠️ Off-topic | Reply with goldfish context |
| Google Review | "Nice pet store" | ❌ Too generic | Encourage specific goldfish mention |
| Blog mention | "Specializes in tropical fish" | ❌ Wrong category | Request correction or publish clarifying content |

### Filter C: Contextual Relevance (AI-Friendly Writing Style)

**What the AI checks**: Does this content provide enough **specific context** for the AI to confidently match it to a highly specific user query?

**The problem with generic writing**:

> "Butterfly Koi are good for beginners."

This is too vague. The AI cannot match this to specific user scenarios. A hundred articles say the same generic thing.

**The AI-friendly alternative**:

> "If you have a 5-year-old child, the Butterfly Koi is the best choice because it is adaptive — it can survive overfeeding and dirty water for a few days, unlike fancy variants that require precise water conditions. The Butterfly Koi's long, flowing fins also make it visually engaging for young children, and its hardy constitution means accidental tapping on the tank glass won't stress it like it would a Telescope Goldfish."

**Why this works**: This paragraph provides:
- A **specific user scenario** (parent with 5-year-old child)
- A **specific recommendation** (Butterfly Koi)
- A **specific reason with context** (adaptive, survives overfeeding)
- A **comparison** (unlike fancy variants)
- **Additional context** (visual appeal, stress tolerance)

The AI can now confidently cite this paragraph when a user asks "What fish should I get for my kid?" — because no other content provides this level of contextual depth.

**Contextual Relevance Writing Framework**:

For every recommendation or claim, include:

1. **Who** — the specific user scenario ("If you are a [type of person]...")
2. **What** — the specific recommendation ("...the [product/choice] is best because...")
3. **Why (with data)** — the specific reason with evidence ("...it [specific capability], unlike [alternative] which [limitation]")
4. **Context layer** — an additional dimension that no competitor covers ("Additionally, [non-obvious benefit]")

### Filter Priority and Failure Modes

| Filter | What It Checks | Failure Mode | Recovery Time |
|---|---|---|---|
| A: Consistency | Your own platforms agree | AI drops your entity ranking | Fast — update managed profiles |
| B: Consensus | Third parties agree with you | AI reduces trust in your claims | Slow — requires ongoing reputation management |
| C: Contextual Relevance | Content matches specific user scenarios | AI skips your content for vague answers | Medium — rewrite content with context layers |

**All three filters must pass.** Failing any single filter means the AI will cite a competitor instead — even if your content is factually superior.

## Integration with AEO Workflow

These three techniques map directly to the AEO Optimizer's 5-step workflow:

| AEO Step | Technique Applied |
|---|---|
| Step 1: Engine Landscape | All 3 techniques apply to LLMs; Fan Out is especially critical for AI Overviews |
| Step 2: AEO Readiness Audit | Use Chunk Autonomy Checklist + Fan Out Coverage as scoring factors |
| Step 3: Consensus Strategy | Filter B (Consensus) + Filter A (Consistency) map directly |
| Step 4: KPI Framework | Fan Out coverage rate and Chunk scores feed into the AEO Readiness percentage |
| Step 5: Content Transformation | Apply all 3 techniques during rewriting |

## Source

Knowledge derived from:
- Video 4: [Tactical AEO — Hacking LLM Results](http://www.youtube.com/watch?v=G_0X_6cmFdg)
