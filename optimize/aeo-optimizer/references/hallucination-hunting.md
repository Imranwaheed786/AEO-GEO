# Hallucination Hunting & USP Extraction — Tactical AEO Intelligence

This reference document provides the step-by-step framework for auditing what AI knows about your brand vs. competitors, hunting hallucination gaps through query layering, tracing AI's background query paths, and extracting the specific USPs that AI values.

## The Core Problem: Human USPs ≠ AI USPs

When a client lists their Unique Selling Points, those are **human-valued USPs** — features they believe make them special (e.g., "we accept crypto," "our staff offers complimentary drinks," "female-owned business").

AEO isn't about what the client thinks is unique. It's about **what the AI thinks is unique**. If the AI doesn't know those USPs exist — because they're not published, cited, or corroborated across the web — they are useless for AEO.

**The gap**: There are two separate realities:
- **Client reality**: "We're unique because of X, Y, Z"
- **AI reality**: "I know this business does A and B, but nothing about X, Y, or Z"

Your job is to close this gap by discovering what the AI values and ensuring your client's content matches those signals.

## Step 1: AI Competitor Auditing

Before writing content or defining USPs, audit what the AI currently knows about your client vs. the leading competitors.

### The Two-Question Audit

**Question 1 — About your client:**
```
What do you know about [Client Business Name]?
```

Record everything the AI returns: services, pricing, history, reviews, location details, specializations. This is your **AI knowledge baseline**.

**Question 2 — About the competitor:**
```
What do you know about [Competitor Business Name]?
```

Record the same categories. This reveals what the AI considers important about the competitor.

### The Knowledge Gap Matrix

| Factor | Your Client (AI Knows) | Competitor (AI Knows) | Gap? |
|---|---|---|---|
| Founding year / history | ? | e.g., "Established 1996" | ✅ AI values longevity |
| Number of locations | ? | e.g., "9+ locations" | ✅ AI values scale |
| Specific services | e.g., "Basic car wash, detailing" | e.g., "Full detail, EV charging, ceramic coating" | ✅ Competitor has richer service profile |
| Reviews / reputation | ? | ? | Compare depth |
| Specializations | ? | ? | Compare specificity |
| Unique features | ? | e.g., "EV charging stations" | ✅ AI associates competitor with innovation |

**Key insight**: The AI's response reveals what data it has been trained on. If it knows the competitor was established in 1996 and has EV charging, those are the signals the AI uses for recommendations. Your client must publish equivalent or superior signals.

### What the Gap Tells You

| AI Response About Your Client | Meaning | Action |
|---|---|---|
| Detailed, accurate, rich information | AI has strong training data | Optimize existing signals |
| Basic, generic, or partially accurate | AI has weak training data | Major content gap — publish more |
| "I don't have specific information" | AI has almost no training data | Complete content build needed |
| Incorrect information (hallucination) | AI is guessing from fragments | Urgent — publish correct information everywhere |

## Step 2: Layering for Hallucination Hunting

Do NOT ask the client who their competitors are. Instead, ask for their **Top 5 Services**. Then apply **Layers** to force the AI to search for highly specific niches where it will hallucinate.

### What Are Layers?

Layers are modifiers that add specificity to a core service query. Each layer narrows the search space and increases the probability of finding a hallucination gap.

### The 6 Layer Types

| Layer | What It Adds | Example (Car Wash) |
|---|---|---|
| **Location** | Geographic specificity | "Car wash in Amsterdam" |
| **Demographic/Persona** | Identity-based targeting | "Car wash owned by a Black entrepreneur" |
| **Problem** | Specific issue to solve | "Car wash that cleans deep stains" |
| **Budget** | Price sensitivity | "Affordable premium car wash under €50" |
| **Experience Level** | User expertise | "Car wash for luxury car first-time owners" |
| **Negative/Exclusion** | What to avoid | "Car wash that doesn't use harsh chemicals" |

### How to Apply Layers

Take each of the client's top 5 services and combine with 2–3 layers:

```
[Core Service] + [Layer 1] + [Layer 2]
```

**Examples:**
- "Premium car detailing" + Location + Problem → "Premium car detailing for deep stains in Amsterdam"
- "Mobile car wash" + Demographic + Budget → "Affordable mobile car wash for busy professionals"
- "Interior car cleaning" + Negative + Experience → "Chemical-free interior cleaning for new car owners"

### Layering Matrix Template

| Core Service | Location Layer | Demographic Layer | Problem Layer | Budget Layer | Negative Layer |
|---|---|---|---|---|---|
| [Service 1] | [city/region] | [persona] | [specific issue] | [price range] | [exclusion] |
| [Service 2] | | | | | |
| [Service 3] | | | | | |
| [Service 4] | | | | | |
| [Service 5] | | | | | |

**Target**: Generate 15–25 layered queries from 5 core services.

### How to Spot Hallucination

When you ask the AI a layered query, watch for these two telltale behaviors:

#### Signal A: Justifications

The AI starts explaining why it can't find what you're looking for:
- "I couldn't find a widely listed business matching that description..."
- "Finding this specific combination is difficult because..."
- "There isn't a well-known service that specifically..."
- "While I don't have exact data on..."

**What this means**: The AI has no training data for this query. This is a hallucination gap.

#### Signal B: Alternative Suggestions

The AI deflects to unrelated or general resources:
- "You might try checking general business directories..."
- "Here are some car washes in the area (not matching your criteria)..."
- "Consider searching on [generic platform] for more options..."

**What this means**: The AI is trying to be helpful but has no real answer. Another hallucination gap.

### Hallucination Response Scoring

| AI Response Pattern | Score | Opportunity Level |
|---|---|---|
| Both Justifications + Alternatives | 🔴 10/10 | Maximum gap — write content immediately |
| Justifications only | 🟠 8/10 | Strong gap — high priority content |
| Partial answer + alternatives | 🟡 6/10 | Moderate gap — good opportunity |
| Answer with wrong details | 🟡 5/10 | Hallucination — correct with your content |
| Decent answer, few sources | 🟢 3/10 | Small gap — write if resources allow |
| Strong, sourced answer | ⚪ 1/10 | No gap — skip |

## Step 3: Query Path Tracing

When an AI struggles with your query, it doesn't just give up. It **modifies your query in the background** to try and find an answer. You need to know what those background searches are.

### The Comet Browser Hack

Use **Comet Browser** or **Perplexity Pro** (any AI tool that shows its search process) to trace the exact query paths the AI takes.

**How it works**:
1. Enter your layered query (e.g., "Black-owned car wash in Netherlands")
2. Watch the AI's search process — it will show the modified queries it tries
3. Record each query modification

### Example Query Path

```
Original query: "Black-owned car wash in Netherlands"
    ↓
AI Background Search 1: "car wash Netherlands Black owned"
    ↓
AI Background Search 2: "car wash Netherlands Afro-Caribbean"
    ↓
AI Background Search 3: "minority-owned car wash Amsterdam"
    ↓
AI Background Search 4: "car wash Netherlands diverse ownership"
```

### Why This Matters

Each background query the AI generates is a **keyword opportunity**. The AI is literally telling you what terms it searches for when trying to answer your target query.

### The Execution

Take these exact background queries and:

1. **Use them as SEO keywords**: Include these terms in your page titles, headers, and content
2. **Create dedicated pages**: Build content around "Afro-Caribbean Car Wash Amsterdam" or "Minority-Owned Auto Detailing Netherlands"
3. **Match the AI's vocabulary**: The AI searched for "Afro-Caribbean" — use that term, not just "Black-owned"
4. **Cross-reference with QF Map**: Add these traced queries to your Query Fan Map grid

### Query Path Tracing Template

| Original Layered Query | AI Background Query 1 | AI Background Query 2 | AI Background Query 3 | Content Created? |
|---|---|---|---|---|
| [layered query] | [traced term 1] | [traced term 2] | [traced term 3] | ☐/☑ |

## Step 4: USP Extraction & Dissection

Once you identify competitors ranking for your targeted layers, dissect **why the AI chose them**.

### The 3-Question USP Extraction

Ask the AI these three questions about each cited competitor:

**Question 1: Legitimacy check**
```
Is [Competitor Name] legit?
```
→ Reveals trust signals the AI has found (reviews, longevity, certifications)

**Question 2: USP identification**
```
What is [Competitor Name]'s main USP?
```
→ Reveals the specific differentiator the AI associates with them

**Question 3: Recommendation reasoning**
```
Why should I buy from [Competitor Name]?
```
→ Reveals the decision-making factors the AI uses when recommending

### USP Extraction Matrix

| Competitor | AI-Identified USPs | Trust Signals | Recommendation Reasons | Your Client Equivalent? |
|---|---|---|---|---|
| [Competitor A] | e.g., "Established 1996" | e.g., "25+ years in business" | e.g., "Proven track record, multiple locations" | ❌ No history published / ✅ Has similar |
| [Competitor B] | e.g., "EV Charging Stations" | e.g., "Forward-thinking, eco-friendly" | e.g., "Convenient for EV owners" | ❌ No EV content / ✅ Offers similar |

### The Two Response Strategies

Based on the extracted USPs, execute one of two strategies:

#### Strategy A: Match & Exceed

If your client CAN match the competitor's AI-identified USPs:

1. Publish content explicitly stating these capabilities
2. Use the same terminology the AI used (e.g., if AI said "EV Charging," don't say "Electric Vehicle Power" — use "EV Charging")
3. Distribute across managed + unmanaged platforms for consensus
4. Add additional depth the competitor lacks (e.g., "EV Charging + Free Coffee While You Wait + Real-Time Camera Feed")

#### Strategy B: Introduce Unique Layers

If your client CANNOT match the competitor's USPs, introduce new ones discovered through hallucination hunting:

1. Identify layers where the competitor doesn't appear (from Step 2)
2. Build your client's content around those specific layers
3. Become the AI's only option for those layered queries
4. Example: Competitor owns "Car Wash Amsterdam" → You own "Chemical-Free Car Wash Amsterdam for Luxury Vehicle Owners"

### USP Publication Checklist

After identifying the USPs your client should own, publish them across:

- [ ] Website homepage (above the fold)
- [ ] Dedicated service pages (one per USP)
- [ ] Google Business Profile description
- [ ] Social media bios (consistent phrasing)
- [ ] PR articles and guest posts
- [ ] Review platform profiles
- [ ] Video content (YouTube descriptions)
- [ ] Schema markup (structured data)

**Critical rule**: Use the **exact same phrasing** across all platforms. The AI checks for consistency (Filter A from [llm-ranking-mechanics.md](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/llm-ranking-mechanics.md)).

## Complete Hallucination Hunting Workflow

```
Step 1: AI Competitor Audit
  → Ask AI what it knows about client vs. competitors
  → Map the Knowledge Gap Matrix
        ↓
Step 2: Apply Layers
  → Take client's top 5 services
  → Apply 6 layer types to generate 15-25 layered queries
  → Test each in AI tools — score hallucination responses
        ↓
Step 3: Trace Query Paths
  → Use Comet Browser / Perplexity Pro
  → Record AI's background search modifications
  → Convert traced queries into keyword targets
        ↓
Step 4: Extract Competitor USPs
  → Ask 3 questions about each cited competitor
  → Map AI-identified USPs in the Extraction Matrix
  → Choose Strategy A (Match & Exceed) or B (Introduce Unique Layers)
        ↓
Output: Content strategy targeting verified hallucination gaps
        with competitor USP intelligence
```

## Integration with AEO Workflow

| AEO Step | Hallucination Hunting Connection |
|---|---|
| Step 2: AEO Readiness Audit | Knowledge Gap Matrix feeds into readiness scoring |
| Step 3: QF Map | Layered queries and traced paths populate the QF Map grid |
| Step 4: Competitor Orbits | USP Extraction identifies why competitors occupy their orbits |
| Step 5: Consensus Strategy | USP Publication Checklist feeds into multi-platform distribution |
| Step 7: LLM Ranking Mechanics | Traced query paths become Fan Out targets; USP consistency validates Filter A |

## Source

Knowledge derived from:
- Video 8: [Hallucination Hunting & USP Extraction](http://www.youtube.com/watch?v=VIDEO_8_ID)
