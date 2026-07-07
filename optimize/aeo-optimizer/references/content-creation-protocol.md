# Content Creation Protocol — From Research to AEO-Optimized Writing

This reference document provides the complete protocol for transforming competitive research and query analysis into hallucination-proof, AEO-optimized content. It bridges the gap between research (competitor orbits, hallucination hunting) and execution (actual writing).

## Strategic Principle: Competing Smart, Not Hard

Finding weak competitors (Outer Orbit) is not enough. You must understand **why** they rank and **how** to write better than them. Entering content creation without researching the terrain — the AI's perception, customer language, real intent, and constraints — guarantees failure.

The protocol has three parts:
1. **Competitor Analysis** (one-time per competitor)
2. **Query Analysis** (per article)
3. **Master Prompt Formulation** (combines everything into a writing brief)

---

## Part 1: Competitor Analysis (One-Time Setup)

This analysis is performed **once per main competitor**. The goal is to understand what the AI "thinks" about them and extract the signals that drive the AI's recommendations.

### Step 1A: Extract AI-Perceived USPs

Instead of asking a client what makes them unique, ask the AI what makes the **competitor** unique.

**Prompt:**
```
Analyze [Competitor URL]. What is their primary USP in [Industry]?
```

**What to capture**: The AI will reveal specific qualities it values — these might be completely different from what a human would identify:

| Human-Perceived USP | AI-Perceived USP | Gap |
|---|---|---|
| "Great customer service" | "Fair and transparent pricing" | AI values pricing data, not subjective claims |
| "We've been around a long time" | "Established 1996, 25+ years of documented expertise" | AI values specific dates and verifiable history |
| "Quality products" | "Discretion and privacy in high-value transactions" | AI found a niche the client didn't even market |

**Why it matters**: You must inject similar or superior USPs into your own content so the AI views you as an equal or better alternative. If the AI values "Fair pricing" in your competitor, your content must explicitly address pricing transparency.

**Critical rule**: For local or highly specific queries, always use **exact URLs** in your prompts. Otherwise, the AI will heavily hallucinate and give you answers about unrelated businesses with similar names.

### Step 1B: Extract Dominant Subject Areas (Angles)

You need to know what **topics** the AI associates with the competitor.

**Prompt:**
```
What subject areas does [Competitor URL] consistently dominate?
```

**What to capture**: The AI will list the specific topic clusters it associates with that competitor:

| Competitor | AI-Identified Dominant Angles |
|---|---|
| Jewelry Store A | Investment perspectives, precious metals market, heritage pieces |
| Car Wash B | Eco-friendly cleaning, luxury vehicle care, fleet services |
| SaaS Tool C | Startup onboarding automation, customer churn reduction, live chat |

**Why it matters**: If you want to beat a competitor, you must prove your authority in their **specific, overlapping angles**. You cannot generically compete — you must match them topic-for-topic in the areas where you want to displace them.

### Competitor Analysis Output Template

```markdown
## Competitor Analysis: [Competitor Name]

**URL**: [exact URL]
**Date analyzed**: YYYY-MM-DD
**AI tool used**: ChatGPT / Claude / Gemini

### AI-Perceived USPs
1. [USP 1] — AI's exact wording: "[quote]"
2. [USP 2] — AI's exact wording: "[quote]"
3. [USP 3] — AI's exact wording: "[quote]"

### Dominant Subject Areas / Angles
1. [Angle 1]
2. [Angle 2]
3. [Angle 3]

### Your Client's Position
- Can match USP 1? ✅/❌ — Action: [match/exceed/introduce alternative]
- Can match USP 2? ✅/❌ — Action: [match/exceed/introduce alternative]
- Can match Angle 1? ✅/❌ — Action: [create content/expand coverage]
```

---

## Part 2: Query Analysis (Per Article)

Before writing **any** article, perform a Query Analysis. This ensures your content perfectly matches the AI's mathematical embeddings — how it matches user queries to content answers.

### Step 2A: Extract Customer Language & Tone

Do NOT write like a textbook. Write exactly how the customer speaks.

**How to execute:**

1. Search your topic on Reddit: `site:reddit.com [your topic] [audience]`
   - Example: `site:reddit.com goldfish beginner`
2. Gather 3–4 URLs of real user questions/threads
3. Feed them to the AI with this prompt:

**Prompt:**
```
Here are 3-4 Reddit threads where real users discuss [topic]:
- [URL 1]
- [URL 2]
- [URL 3]

Identify the tone, vocabulary, and emotional register of these users. 
I will be writing content to address these concerns at the exact same 
level as the questioner. Give me:
1. Common words/phrases they use
2. Their emotional state (anxious, excited, confused, etc.)
3. Their knowledge level (beginner, intermediate, expert)
4. Questions they ask that aren't in the post title
```

**What you get**: A tone profile that ensures your content resonates with real users and matches the language patterns the AI has indexed from these discussions.

### Step 2B: Identify the Real Intent

When someone searches "Best goldfish for beginners," they don't just want a list of fish. They are searching because they are **scared of killing the fish**.

**Prompt:**
```
Why would someone search "[exact target query]"? 
Give me the real reasons for their consideration and evaluation — 
not the surface-level intent, but the underlying fears, desires, 
and decision-making factors.
```

**Example output for "Best goldfish for beginners":**

| Surface Intent | Real Intent |
|---|---|
| "Find a list of beginner goldfish" | "I'm scared of killing a fish and wasting money" |
| "Compare goldfish types" | "I want the safest, lowest-risk option" |
| "Learn about goldfish care" | "I want to know the minimum effort required" |

**Why it matters**: Your article must directly answer these **underlying fears and desires**, not just the surface query. The AI recognizes content that addresses real intent and prioritizes it over generic listicles.

### Step 2C: Find the Constraints (Context Builders)

Answer Engines need context. You must define the **limits** of the user's situation so the AI can match your content to specific user scenarios.

**Prompt:**
```
What are all possible constraints for a person asking "[exact target query]"? 
Include situational, financial, environmental, and experience-based constraints.
```

**Example output for "Best goldfish for beginners":**

| Constraint Category | Specific Constraints |
|---|---|
| Budget | Under $50 setup, under $100 setup, premium budget |
| Space | Studio apartment, house with dedicated room, office desk |
| Climate | Hot climate (>85°F), cold climate (<60°F), air-conditioned indoor |
| Experience | Never owned a pet, had other pets but not fish, returning to fishkeeping |
| Household | Has young children, has cats/dogs, lives alone |
| Time | Busy professional (minimal maintenance), stay-at-home (more time available) |

**Why it matters**: Each constraint combination creates a unique user scenario. When you address specific constraints in your content, the AI can confidently match it to highly specific queries that competitors' generic content cannot serve.

---

## Part 3: The Master Prompt Formulation

Combine all extracted data from Parts 1 and 2 into a single **Master Prompt** that you use to generate AEO-optimized content.

### The Master Prompt Template

```markdown
# Content Creation Brief: [Article Title / Target Query]

## Target Query
[The exact query this content must answer]

## My Core USPs
Below are my core USPs. Embed them naturally throughout the content 
to leverage consistency across my web presence:
1. [USP 1 — exact phrasing to use]
2. [USP 2 — exact phrasing to use]
3. [USP 3 — exact phrasing to use]

## My Dominant Angles
Below are my established angles for contextual relevance. 
Reference these where applicable:
1. [Angle 1]
2. [Angle 2]
3. [Angle 3]

## Customer Language Profile
- **Tone**: [anxious/excited/skeptical/etc.]
- **Vocabulary level**: [beginner/intermediate/expert]
- **Common phrases they use**: [list from Reddit extraction]
- **Emotional register**: [what they're really feeling]

## Real Intent
The reader is NOT just looking for [surface intent]. They are actually:
- [Real reason 1 — underlying fear/desire]
- [Real reason 2 — underlying fear/desire]
- [Real reason 3 — underlying fear/desire]

## Constraints to Address
Cover these specific user scenarios in the content:
- Budget: [constraint options]
- Space: [constraint options]
- Climate/Location: [constraint options]
- Experience: [constraint options]
- [Other relevant constraints]

## Competitor Context
The current AI-cited competitor for this query is [Competitor Name].
Their AI-perceived USPs are: [list]
Their dominant angles are: [list]
Our content must match or exceed these signals while introducing 
our unique differentiators.

## Writing Rules
1. Every paragraph must be autonomous (see Chunk Autonomy Checklist)
2. Lead with the answer, not the backstory
3. Include specific data points in every claim
4. Address constraints explicitly ("If you live in a hot climate...")
5. Use the customer's language, not industry jargon
6. Match the emotional register identified above
```

### Master Prompt Quality Checklist

Before using the Master Prompt to generate content, verify:

- [ ] USPs are in the **exact phrasing** used across all managed platforms
- [ ] Angles match the dominant areas where you want to compete
- [ ] Customer language is sourced from **real user threads** (not assumed)
- [ ] Real intent goes beyond surface-level query interpretation
- [ ] At least 4 constraint categories are identified
- [ ] Competitor USPs are documented for comparison
- [ ] Writing rules include chunk autonomy requirement

### Using the Master Prompt

Feed the complete Master Prompt to your AI writing tool (or use it as your own writing guide). The resulting content will:

1. **Match AI embeddings**: Because it uses the same language patterns the AI has indexed
2. **Address real intent**: Because it answers underlying fears, not just surface queries
3. **Fill hallucination gaps**: Because it covers specific constraint combinations no competitor addresses
4. **Build consistency**: Because USPs are embedded using exact managed-asset phrasing
5. **Satisfy contextual relevance**: Because constraints provide the deep context the AI needs (Filter C)

---

## Integration with AEO Workflow

| AEO Step | Content Creation Protocol Connection |
|---|---|
| Step 2: AEO Readiness Audit | Existing content scored against Master Prompt standards |
| Step 3: QF Map | Each QF Map cell generates one Master Prompt |
| Step 4: Competitor Orbits & Hallucination Hunting | Competitor Analysis (Part 1) feeds USPs and Angles |
| Step 5: Consensus Strategy | Master Prompt USP phrasing must match consensus messaging |
| Step 7: LLM Ranking Mechanics | Writing rules enforce Chunk Autonomy and Filter compliance |
| Step 8: Transformation Plan | Master Prompts become the content production queue |

## Source

Knowledge derived from:
- Video 9: [Content Creation Protocol — Query Analysis & Master Prompt](http://www.youtube.com/watch?v=VIDEO_9_ID)
