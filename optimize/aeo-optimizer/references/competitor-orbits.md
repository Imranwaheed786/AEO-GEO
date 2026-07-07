# Competitor Orbits — AEO Competitive Intelligence

This reference document provides the framework for categorizing competitors, assessing query difficulty, and selecting the optimal attack path for Answer Engine Optimization.

## The 4R Strategic Framework

Before executing any competitive tactics, follow this progression:

| Phase | Action | Purpose |
|---|---|---|
| **Research** | Understand what is currently working in the market and who your real competitors are | Map the landscape before acting |
| **Replicate** | Find successful models and replicate their approach — do not invent from scratch | Build on proven patterns |
| **Reciprocate** | Provide immense value and education to the audience first, building trust before selling | Earn authority through generosity |
| **Replace** | Once you have matched the competitor and built trust, introduce your improved model to replace them | Innovate from a position of parity |

**Key principle**: You cannot skip phases. Attempting to Replace (Phase 4) before completing Research and Replication guarantees failure. The 4R sequence is mandatory.

## The Predator Stack: 3 Competitor Orbits

When assessing competitors for AEO, do not lump them into one group. Categorize them into three distinct "Orbits" and attack in **reverse order** (Outer → Mid → Core).

### Orbit 1: Core Orbit (The Cheetahs / Deep Water)

**Who they are**: Enterprise-level competitors — massive brands, Wikipedia, industry leaders with thousands of pages and years of authority.

**AEO signals**:
- Appear consistently across almost all Answer Engines (ChatGPT, Claude, Gemini)
- Strong brand signals recognized by AI without needing citations
- Thousands of Trustpilot/G2 reviews establishing overwhelming consensus
- Massive content libraries (1,000+ pages)
- AI mentions them by name even without being prompted

**Strategy**: Do NOT attack directly at the start. You need substantial budget and enterprise-level tactics to unseat Core Orbit competitors. Attempting this early wastes resources.

**When to target**: Only after establishing authority in Mid and Outer orbits, building citation momentum, and accumulating 10+ consistent AI citations.

### Orbit 2: Mid Orbit (Active Competitors / Shallow Water)

**Who they are**: Competitors actively trying to rank in AEO, just like you. They have a deliberate content strategy but a smaller footprint than Core Orbit.

**AEO signals**:
- Rank for specific layers of a query (e.g., location-based, budget-based, or niche-specific queries)
- Actively publish content with some AEO awareness
- Moderate content footprint (200–300 pages)
- Appear in AI answers for mid-specificity queries but not broad ones
- Have some third-party reviews and citations but not dominant consensus

**Strategy**: **Replicate then improve**. Find their content gaps — topics they cover poorly or incompletely — and write better, more comprehensive versions. Use the 4R framework: study what they're doing, match it, then exceed it.

**Tactical actions**:
1. List all queries where Mid Orbit competitors are cited by AI
2. Identify which queries they cover superficially or generically
3. Create deeper, more contextual content for those same queries
4. Ensure your content passes all 3 Retrieval Filters (see [llm-ranking-mechanics.md](https://github.com/Imranwaheed786/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/llm-ranking-mechanics.md))
5. Build consensus across platforms to match their third-party presence

### Orbit 3: Outer Orbit (Lucky Competitors / Empty Water)

**Who they are**: Random blogs, unrelated sites, low-authority forums, or niche pages that the AI cites only because nothing better exists.

**AEO signals**:
- Appear on only 1 or 2 highly specific queries
- Have no consistent AEO strategy
- Very few pages (often a single blog post or forum thread)
- The AI cites them because it is hallucinating due to lack of relevant data
- Low-quality or outdated content that happens to be the only source available

**Strategy**: **Attack here first**. These competitors only appear because the AI is guessing. You can easily replace them with minimal effort by providing a direct, accurate, well-structured answer.

**Why this works**: When you replace an Outer Orbit competitor, the AI immediately gains confidence in your content because it's dramatically better than what it was previously relying on. This is how you earn your first 2–3 citations — the foundation for moving up to Mid and Core Orbit competition.

## The Orbit Attack Sequence

```
Phase 1: Outer Orbit (Weeks 1–4)
  → Find queries where AI cites random/low-quality sources
  → Write authoritative, chunk-optimized content
  → Earn first 2–3 AI citations
  → AI begins recognizing your domain

Phase 2: Mid Orbit (Months 2–4)
  → Target queries where active competitors are cited
  → Replicate their strategy with superior content
  → Build cross-platform consensus
  → Expand citation count to 10+

Phase 3: Core Orbit (Month 6+)
  → Contest broad, high-volume queries
  → Leverage accumulated authority and citations
  → Requires enterprise-level effort and budget
  → AI recommends you alongside established leaders
```

## OCS Environment Grading

Before writing content for any query, grade the competitive environment. Do not waste time on saturated queries.

### The 3 Grades

| Grade | Name | What the AI Does | Competitor Type | Action |
|---|---|---|---|---|
| **O** | Open (Hallucination Zone) | Gives weak answers, changes context, cites Outer Orbit competitors, or admits uncertainty | Outer Orbit / no competitors | ✅ Primary target — write immediately |
| **C** | Contested (Competing) | Provides somewhat inconsistent answers across platforms; Mid Orbit competitors appear | Mid Orbit | ⚠️ Good target for moderate budgets — replicate and improve |
| **S** | Saturated | Provides strong, exact, confident answers citing Core Orbit competitors consistently | Core Orbit | ❌ Avoid initially — requires enterprise-level effort |

### How to Grade a Query

1. **Turn off Memory and Personalization** in your AI tools
2. Search the exact query in ChatGPT, Claude, AND Gemini
3. For each AI, note:
   - Is the answer confident and specific? (→ Saturated signal)
   - Does the answer vary between models? (→ Contested signal)
   - Does the AI guess, hedge, or cite low-quality sources? (→ Open signal)
4. Assign the grade based on the dominant signal

### OCS Grading Template

| Query | ChatGPT Grade | Claude Grade | Gemini Grade | Overall | Cited Competitor Orbit | Action |
|---|---|---|---|---|---|---|
| [query 1] | O/C/S | O/C/S | O/C/S | O/C/S | Outer/Mid/Core | Write/Replicate/Skip |
| [query 2] | | | | | | |

### Combining OCS with QF Map

Apply OCS grading to every query in your QF Map grid to create a prioritized content calendar:

| Priority | QF Map Stage | OCS Grade | Orbit Target | Action |
|---|---|---|---|---|
| P0 (Immediate) | Pre-Awareness / Awareness | O (Open) | Outer Orbit | Write authoritative content now |
| P1 (Soon) | Consideration | O or C | Outer / Mid | Write or improve content |
| P2 (Plan) | Evaluation | C (Contested) | Mid Orbit | Replicate competitor + improve |
| P3 (Later) | Decision | C or S | Mid / Core | Build after earning citations |
| P4 (Enterprise) | Any | S (Saturated) | Core Orbit | Enterprise budget required |

## The Budget Hack: Negative & Anti-Audience Content

If you have a low budget and need quick AEO wins, bypass broad keywords entirely and focus on **negative layers**, **anti-audience queries**, and **problem-specific exclusions**.

### What Are Negative Queries?

These are queries framed around what NOT to do, what to avoid, or which options are bad for specific audiences:

| Query Type | Example | Why It Works |
|---|---|---|
| Negative recommendation | "Which fancy goldfish are bad for beginners?" | Almost no brands write negative content |
| Anti-audience | "Running shoes not suitable for marathons" | Brands avoid discouraging potential buyers |
| Problem identification | "Worst mistakes when setting up a fish tank" | Brands focus on positive messaging |
| Exclusion queries | "CRM tools that don't work for solo entrepreneurs" | SaaS companies avoid negative positioning |
| Risk queries | "Hidden costs of cheap goldfish tanks" | Sellers avoid transparency about downsides |

### Why This Works

1. **Zero competition**: Established brands almost never write negative or exclusion-based content because marketing teams avoid anything that could discourage a purchase
2. **High hallucination rate**: AI struggles with negative queries because its training data lacks this perspective — it's trained mostly on positive, promotional content
3. **Outer Orbit by default**: Any AI citation for these queries will be from random forums or low-quality sources — easy to replace
4. **Quick citation wins**: Writing one authoritative negative content piece can earn citations faster than competing for positive queries

### Budget Hack Content Templates

```markdown
## "Which [Products] Are Bad For [Audience]?"
- List 3–5 specific products with factual reasons why they're unsuitable
- Include the specific conditions that make them bad (not generic)
- Recommend alternatives (this is where you mention your product)

## "[Category] Not Suitable for [Use Case]"
- Identify the specific technical limitations
- Explain why the popular choices fail for this use case
- Position your product as the exception (if applicable)

## "Worst Mistakes When [Activity]"
- List 5–7 specific, non-obvious mistakes
- Include data or expert sources for each
- Provide the correct approach for each mistake
```

## Competitor Audit Template

Use this template to map your competitive landscape:

### Orbit Classification

| Competitor | Orbit | AEO Signal Evidence | Pages | Review Volume | AI Mention Rate |
|---|---|---|---|---|---|
| [Competitor A] | Core | Appears in all 3 major LLMs consistently | 1,000+ | 5,000+ reviews | >80% |
| [Competitor B] | Mid | Appears for niche/location queries | 200–300 | 100–500 reviews | 30–60% |
| [Competitor C] | Outer | 1–2 specific queries only | <50 | <50 reviews | <10% |
| [Your Brand] | ? | [Assess honestly] | [Count] | [Count] | [Measure] |

### Query Environment Assessment

| Target Query | OCS Grade | Current Cited Source | Orbit | Content Exists? | Priority |
|---|---|---|---|---|---|
| [query] | O/C/S | [source name] | Outer/Mid/Core | Yes/No | P0–P4 |

## Integration with AEO Workflow

| AEO Step | Competitor Orbits Connection |
|---|---|
| Step 1: Engine Landscape | Orbit mapping shows which engines each competitor dominates |
| Step 2: AEO Readiness Audit | OCS grading reveals which queries are winnable now |
| Step 3: QF Map | Apply OCS grades to every QF Map cell for prioritization |
| Step 4: Consensus Strategy | Mid Orbit requires consensus building; Outer Orbit does not |
| Step 5: KPI Framework | Track orbit progression (Outer → Mid → Core) as a KPI |
| Step 7: Transformation Plan | Attack sequence determines content calendar priority |

## Source

Knowledge derived from:
- Video 7: [Competitor Orbits — AEO Competitive Intelligence](http://www.youtube.com/watch?v=yUb70yR3STo)
