# Query Fan Map (QF Map) — Practical AEO Topic Discovery

This reference document provides the complete framework for building a Query Fan Map — a systematic method to discover, prioritize, and fill the content gaps that force Answer Engines to cite your website.

## Core Concept: Violating Hallucination

### The Opportunity

The fastest way to get cited by an Answer Engine is to find topics where the AI **hallucinates** — where it makes confident but incorrect guesses because it lacks specific, factual training data.

**Why this works**: Traditional search queries (e.g., "What does BBB stand for?") are already heavily covered by thousands of pages. AI will not cite you for basic, well-established facts. However, highly contextual queries have no direct answers online, causing the AI to guess.

### The Spectrum

| Query Type | Example | AI Behavior | Citation Opportunity |
|---|---|---|---|
| Basic factual | "What does BBB stand for?" | Confident, correct answer from vast training data | ❌ None — too many existing sources |
| Moderately specific | "Best goldfish for beginners" | Decent answer assembled from multiple sources | ⚠️ Low — requires beating established authorities |
| Highly contextual | "What goldfish should I buy for my 5-year-old child living in Lahore?" | Guesses — no specific training data exists for this exact scenario | ✅ High — your content becomes the definitive source |
| Multi-layered | "Best low-maintenance goldfish for a 20-gallon tank in a hot climate with hard water" | Hallucination likely — too many intersecting conditions | ✅ Very high — no single source covers this combination |

### The Strategy

If you write content that directly answers these highly specific, complex queries **without fluff**, the AI gains confidence in your answer over its own guesses and will cite you as the source. The key is specificity — the more conditions your content addresses simultaneously, the less competition you face.

### The Hallucination Test

Before writing content for any query, test it:

1. Open ChatGPT (or Claude/Gemini) with **Memory and Personalization turned off**
2. Ask the exact query from your QF Map
3. Evaluate the response:

| AI Response | What It Means | Action |
|---|---|---|
| Specific, sourced answer with citations | Query is well-covered | Skip — low citation opportunity |
| Generic answer without specific sources | Moderate gap — AI assembled from fragments | Write — medium opportunity |
| Hallucinated facts, wrong details, or vague hedging | Major gap — AI lacks training data | Write urgently — high opportunity |
| "I don't have specific information about..." | Complete gap — AI admits it doesn't know | Write immediately — highest opportunity |

## 5 Methods to Extract Contextual Queries

Use these five methods to discover the specific, contextual questions your content should answer. Each method finds different types of queries.

### Method 1: Query Path Analysis

**What**: Search a broad term in Google and examine the "People Also Search For" paths at the bottom of the results page.

**Why it works**: These paths show how users modify their searches when the first AI Overview fails to satisfy their intent. Each refinement reveals a more specific sub-query that the AI struggled to answer.

**How to execute**:
1. Search your broad topic in Google (e.g., "goldfish care")
2. Scroll to "People Also Search For" at the bottom
3. Click the most specific refinement
4. Repeat — follow the path 3–4 levels deep
5. Record each refinement as a potential query

**Example path**:
```
goldfish care
  → goldfish care for beginners
    → goldfish care in small tanks
      → goldfish care in small tanks without filter
        → can goldfish survive in a bowl without filter
```

Each level gets more specific and more likely to be a hallucination gap.

### Method 2: Keyword Question Extraction

**What**: Use SEO tools to systematically extract question-format queries.

**How to execute**:
1. Open a keyword research tool (e.g., Semrush Keyword Magic Tool, Ahrefs Questions)
2. Enter your seed keyword
3. Filter by "Questions" to isolate query-format keywords
4. Export the full list
5. Use ChatGPT to deduplicate and categorize:

```
Here is a list of [X] keyword questions about [topic]. 
Please:
1. Remove exact and near-duplicates
2. Group remaining questions by subtopic
3. Flag any questions that are highly specific or contextual 
   (the kind an AI might not have great training data for)
```

### Method 3: Competitor AI Gap Analysis

**What**: Identify topics where competitors are getting cited by AI but you are not.

**How to execute**:
1. Use an AI visibility tool (e.g., Semrush AI Visibility, Ahrefs AI Citations)
2. Identify which competitors appear in AI citations for your niche
3. Use the "Content Gap" feature: enter your domain vs. 3–4 competitor domains
4. Filter for queries where competitors have AI citations but you have zero
5. These are your highest-priority content creation targets

**Output**: A ranked list of topics where competitors own AI citations you should contest.

### Method 4: Direct AI Brainstorming

**What**: Use the AI itself to generate the obscure, contextual questions it would struggle to answer.

**How to execute**:

Ask ChatGPT/Claude directly:

```
I run a [business type] in [location]. What are the top 10 most 
obscure questions that first-time [customers/buyers] ask that you 
would struggle to answer with high confidence?
```

Follow up with:

```
Now give me 10 more, but make them hyper-specific — questions that 
combine 3+ conditions (location, budget, lifestyle, experience level, 
specific product variants).
```

**Why it works**: The AI knows what it doesn't know. When it generates questions it "would struggle to answer," it's literally telling you where hallucination gaps exist.

### Method 5: UGC Platform Mining (Reddit/Quora)

**What**: Find real user questions on community platforms that have zero or very few helpful answers.

**How to execute**:
1. Search Google: `site:reddit.com [your topic]`
2. Look for threads with highly specific questions
3. Check: Does the thread have helpful, authoritative answers?
4. If the answers are generic, conflicting, or missing → this is a content gap

**Scoring criteria for UGC queries**:

| Signal | Score | Meaning |
|---|---|---|
| Question has 0 helpful answers | +3 | Major gap — nobody covers this |
| Question has conflicting answers | +2 | Consensus gap — AI will hallucinate |
| Question is highly upvoted but poorly answered | +3 | High demand, no supply |
| Question combines 3+ specific conditions | +2 | Contextual query — AI struggles |
| Question was asked in last 6 months | +1 | Fresh demand signal |
| Question appears across multiple threads | +2 | Recurring need |

**Prioritize queries scoring 6+** for content creation.

## The QF Map Framework

Instead of executing those 5 methods randomly, organize discoveries into a systematic **Query Fan Map** (QF Map). The QF Map is a grid that maps **ICPs × Funnel Stages** and fills each cell with the specific queries your content must answer.

### Step 1: Define Ideal Customer Profiles (ICPs)

You cannot target everyone. Define 4–5 specific ICPs for your niche.

**How to generate ICPs**:

Ask ChatGPT:
```
I run a [business type] in [location] targeting [broad audience]. 
Define 4-5 specific Ideal Customer Profiles (ICPs) for my business. 
For each ICP, include:
- Demographics (age, income, situation)
- Primary motivation for buying
- Key concerns or fears
- Typical query behavior (what they search for)
- Experience level with the product/service
```

**Example ICPs for a Goldfish Store**:

| ICP | Description | Primary Motivation | Query Style |
|---|---|---|---|
| First-time parents | Parents buying a first pet for young children (ages 4–8) | Low-maintenance, safe, educational | "What fish is safe for kids?" |
| Casual apartment owners | Young professionals wanting a small aesthetic tank | Decoration, minimal space, low effort | "Best fish for small apartment" |
| Serious hobbyists | Experienced fishkeepers expanding collections | Rare varieties, breeding, tank optimization | "Oranda breeding temperature range" |
| Office interior designers | Commercial buyers setting up lobby/waiting room displays | Visual impact, minimal maintenance, professional look | "Best fish tank setup for office reception" |

### Step 2: Map to the 5-Stage AEO Funnel

The AEO funnel extends the traditional AIDA model with a crucial new stage: **Pre-Awareness**. Map discovered queries to these five stages for **each ICP**:

| Stage | User Intent | Query Type | Content Format | Example |
|---|---|---|---|---|
| **Pre-Awareness** | Has a problem but no idea what causes it or what solutions exist | "Why" root-cause questions | Storytelling, problem-solving blogs | "Why do my feet hurt after running?" |
| **Awareness** | Understands the problem, looking for a category of solutions | "How to" and "What" questions | How-to guides, FAQs | "How to reduce foot pain while running?" |
| **Consideration** | Exploring specific options and positioning | "Best of", "Top", conditional queries | Listicles, "Best of" round-up posts | "Best running shoes for flat feet" |
| **Evaluation** | Directly comparing known entities | "X vs. Y", "Review", "Alternative" queries | Versus pages, comparison tables, Alternatives pages | "Nike vs. Adidas running shoes" |
| **Decision** | Ready to buy — logistics, pricing, brand validation | Location, price, "buy", "is [brand] legit?" | Product pages, localized landing pages, feature/service pages | "Buy running shoes near me" |

> **Key insight**: Pre-Awareness is pure education — no selling happens here. The user has no idea what the solution category even is. This stage has the **highest hallucination gap density** because AI lacks training data for root-cause questions in specific niches.

### Step 3: Build the QF Map Grid

Create a grid with ICPs as rows and the 5 Funnel Stages as columns. Fill each cell with 3–5 queries discovered using the 5 Methods:

```
┌──────────────┬───────────────┬───────────────┬───────────────┬───────────────┬───────────────┐
│ ICP \ Stage   │ PRE-AWARENESS │ AWARENESS     │ CONSIDERATION │ EVALUATION    │ DECISION      │
├──────────────┼───────────────┼───────────────┼───────────────┼───────────────┼───────────────┤
│ First-time   │ Why do fish   │ Why do        │ Best filter   │ Oranda vs.    │ Best goldfish │
│ Parents      │ die in new    │ goldfish die  │ for kids'     │ Fantail for   │ store in      │
│              │ tanks?        │ quickly?      │ room tank?    │ beginners?    │ Lahore?       │
├──────────────┼───────────────┼───────────────┼───────────────┼───────────────┼───────────────┤
│ Serious      │ Why do Ranchu │ Why are       │ Optimal pH    │ Thai vs.      │ Rare goldfish │
│ Hobbyists    │ get head      │ Ranchu so     │ for breeding  │ Chinese       │ breeders in   │
│              │ tumors?       │ expensive?    │ Orandas?      │ Ranchu quality│ Pakistan      │
└──────────────┴───────────────┴───────────────┴───────────────┴───────────────┴───────────────┘
```

### Business-Type QF Map Examples

The query patterns differ significantly by business model. Use these as starting templates:

#### E-commerce / Informational Site (e.g., Gold Buyer/Predictor)

| Stage | Example Query | Content Format |
|---|---|---|
| Pre-Awareness | "How does gold price change?" | Educational blog, data storytelling |
| Awareness | "When to buy gold?" | How-to guide, FAQ |
| Consideration | "24 karat vs 22 karat gold investment" | "Best of" listicle, comparison post |
| Evaluation | "Shall I buy physical gold or forex?" | Versus page, comparison table |
| Decision | "Best location to buy gold near me" / "Is [Shop Name] legit?" | Localized landing page, trust page |

> **Rule**: "Best of" and "Top" queries belong in **Consideration**. "Versus" and direct comparison queries belong in **Evaluation**.

#### Local Business (e.g., Local Aquarium Store)

| Stage | Example Query | Content Format |
|---|---|---|
| Pre-Awareness | "Why is my goldfish not eating?" | Problem-solving blog |
| Awareness | "Do goldfish need big tanks?" / "Is a goldfish easy to keep?" | FAQ, how-to guide |
| Consideration | "Best fancy goldfish breeds for apartments" | Listicle, round-up post |
| Evaluation | "Common Goldfish vs. Fantail" | Versus page, comparison table |
| Decision | "Where to buy goldfish in Lahore" / "Is Aqua World a reliable store?" | Localized landing page, Google Business Profile |

#### SaaS / Software (e.g., Chatbot Software)

| Stage | Example Query | Content Format |
|---|---|---|
| Pre-Awareness | "Why is my churn rate so high?" | Problem-solving blog, storytelling |
| Awareness | "How to automate customer support?" | How-to guide, educational content |
| Consideration | "Best live chat support for startups" | "Best of" listicle |
| Evaluation | "Intercom vs. Zendesk" | Versus page, comparison table, Alternatives page |
| Decision | "Best Intercom alternative for startups" / "Can [Tool] automate onboarding?" | Feature page, dedicated service page |

> **SaaS note**: Decision-stage queries about specific capabilities (e.g., "Can [Tool] automate onboarding?") require a **dedicated feature/service page** to rank. Generic product pages will not satisfy these queries.

### Step 4: Test for Hallucination Gaps

For each query in the grid, run the Hallucination Test:

1. **Turn off Memory and Personalization** in your AI tools
2. Search the exact query
3. Rate the AI's response:

| Rating | Symbol | Meaning | Priority |
|---|---|---|---|
| Hallucination | 🔴 | AI guessed wrong or made up facts | P0 — Write immediately |
| Vague/Generic | 🟡 | AI gave a generic answer, no specific sources | P1 — Write soon |
| Adequate | 🟢 | AI answered well with credible sources | P2 — Write if resources allow |
| Well-covered | ⚪ | AI nailed it with multiple authoritative citations | Skip — low ROI |

### Step 5: Assign Content Destinations

Once your grid is populated and tested, decide where each piece of content lives:

| Content Type | Best For | Funnel Stage | Example |
|---|---|---|---|
| Storytelling / problem blog | Root-cause questions the user doesn't know how to solve | Pre-Awareness | "Why Fish Die in New Tanks: The Nitrogen Cycle Explained" |
| How-to guide / FAQ | Solution-category questions | Awareness | "Complete Guide: How to Keep Goldfish Alive" |
| Listicle / "Best of" round-up | Specific option exploration | Consideration | "7 Best Fancy Goldfish for Small Apartments" |
| Versus page / comparison table | Direct entity comparisons | Evaluation | "Oranda vs. Fantail: Which Is Right For You?" |
| Alternatives page | Users seeking options to a known brand | Evaluation | "5 Best Intercom Alternatives for Startups" |
| Localized landing page | Buy-intent with location | Decision | "Buy Rare Goldfish in Lahore — Same Day Delivery" |
| Feature / service page | Capability-specific buy queries | Decision | "Automated Onboarding — [Tool] Features" |
| Trust / legitimacy page | Brand validation queries | Decision | "About [Brand] — Reviews, Certifications, Story" |
| Knowledge base article | Technical condition-specific questions | Consideration | "Optimal Water Parameters for Fancy Goldfish" |
| Video + transcript | Complex multi-condition queries | Any | "Setting Up a 50-Gallon Kids' Room Tank: Tutorial" |

## The Trust-Building Growth Strategy

You cannot rank for broad, high-volume Decision-stage queries (like "Buy running shoes") right away. Trust must be earned progressively.

### The Citation Ladder

```
Pre-Awareness & Awareness (hallucination gaps)
    ↓ AI starts citing you for obscure questions
    ↓ 2-3 citations earned
    ↓ AI begins viewing your site as authoritative
Consideration & Evaluation (competitive queries)
    ↓ AI recommends you alongside established brands
    ↓ Citation count grows
Decision (high-volume, high-intent queries)
    ↓ AI confidently recommends you for buyer queries
```

### Execution Priority

| Phase | Target Stage | Strategy | Expected Outcome |
|---|---|---|---|
| Phase 1 (Month 1–2) | Pre-Awareness + Awareness | Find hallucination gaps; write authoritative content for obscure, specific questions | First 2–3 AI citations |
| Phase 2 (Month 2–4) | Consideration | Create "Best of" and listicle content; leverage initial citations for credibility | AI begins recommending alongside competitors |
| Phase 3 (Month 4–6) | Evaluation | Publish versus pages and comparison content | AI includes you in direct comparisons |
| Phase 4 (Month 6+) | Decision | Create localized landing pages, feature pages, trust pages | AI confidently recommends for buy-intent queries |

> **Key principle**: By answering obscure questions first, the AI starts citing you. Once you get 2–3 citations, the AI views your site as an authoritative, trustworthy source. Only then will it begin recommending you for broader, highly competitive Decision-stage queries.

## QF Map Scoring

After completing the map, calculate your coverage score:

```
QF Coverage = (Cells with 🔴 or 🟡 content created) / (Total 🔴 and 🟡 cells) × 100
```

| Score | Status | Action |
|---|---|---|
| 90–100% | Full coverage | Monitor and refresh quarterly |
| 70–89% | Good coverage | Prioritize remaining 🔴 gaps |
| 50–69% | Partial coverage | Accelerate content production |
| Below 50% | Major gaps | Full content sprint needed |

## Integration with AEO Workflow

The QF Map feeds directly into the AEO Optimizer's workflow:

| AEO Step | QF Map Connection |
|---|---|
| Step 1: Engine Landscape | QF Map queries should be tested across all target engines |
| Step 2: AEO Readiness Audit | QF Coverage score becomes part of overall AEO Readiness |
| Step 3: Consensus Strategy | QF Map content distributed across ICP-targeted platforms |
| Step 4: KPI Framework | Track citation rate per QF Map cell; measure gap closure |
| Step 5: LLM Ranking Mechanics | Each QF Map content piece must pass Fan Out, Chunking, and 3 Filters |
| Step 6: Transformation Plan | QF Map becomes the content production calendar |

## QF Map Template (Blank)

```markdown
# Query Fan Map: [Business/Brand Name]

**Date**: YYYY-MM-DD
**Target engines**: ChatGPT / Claude / Gemini / AI Overviews

## ICPs

| # | ICP Name | Description | Primary Motivation |
|---|----------|-------------|-------------------|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |

## QF Grid

### ICP 1: [Name]

| Stage | Query | Hallucination Test | Priority | Content Type | Status |
|-------|-------|--------------------|----------|-------------|--------|
| Pre-Awareness | | 🔴/🟡/🟢/⚪ | P0/P1/P2 | Blog/FAQ/Page | ☐/☑ |
| Awareness | | | | | |
| Consideration | | | | | |
| Evaluation | | | | | |
| Decision | | | | | |

### ICP 2: [Name]
(repeat grid)

## Coverage Summary

| | Pre-Awareness | Awareness | Consideration | Evaluation | Decision | Total |
|---|---|---|---|---|---|
| 🔴 Gaps | | | | | |
| 🟡 Weak | | | | | |
| 🟢 Adequate | | | | | |
| Content created | | | | | |
| **Coverage %** | | | | | |

## Query Sources Used
- [ ] Method 1: Query Path Analysis
- [ ] Method 2: Keyword Question Extraction
- [ ] Method 3: Competitor AI Gap Analysis
- [ ] Method 4: Direct AI Brainstorming
- [ ] Method 5: UGC Platform Mining
```

## Source

Knowledge derived from:
- Video 5: [Building a Query Fan Map — Practical AEO Framework](http://www.youtube.com/watch?v=xz8Z5gWLP1Y)
- Video 6: [QF Map by Business Type — 5-Stage Funnel & Trust Building](http://www.youtube.com/watch?v=Yf5Pbh5Pjh8)
