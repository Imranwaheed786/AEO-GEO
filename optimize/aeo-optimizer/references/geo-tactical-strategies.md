# GEO Tactical Strategies — Technical Implementation for AI Citation

This reference document provides the 5 tactical strategies for ensuring AI engines can find, understand, trust, and cite your content. These strategies complement the content-level frameworks (A.Q.C.E., FAQ) with technical and platform-level optimizations.

## Strategy 1: Create Direct and Snippable Content

AI engines do not want fluff — they want clean, crisp, and fast answers.

### E.E.A.T. in the First Sentences

In the very first few sentences of any article, prove why you are qualified to answer. AI will not pull snippets from random, unverified sites.

**Formula**: `As a [credential] who has [specific experience], here is [answer]...`

**Examples:**

| ❌ No E.E.A.T. | ✅ E.E.A.T. Upfront |
|---|---|
| "There are many great laptops for video editing." | "As a video editor who has tested 20+ laptops in the last 6 months, here is my verdict..." |
| "Goldfish care can be tricky." | "After maintaining 15 aquariums for 8 years, including tropical and coldwater setups, here's what works..." |
| "SEO is changing rapidly." | "Having managed AEO campaigns for 40+ clients since 2023, the shift to AI-first content requires..." |

### Answer Immediately

Do not waste time with long introductions. If the query is "Best video editing laptop," the first sentence under the heading must be:

> "The best video editing laptop is [X] because of [Y]."

This aligns with the A.Q.C.E. Answer layer (see [aeo-writing-framework.md](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/aeo-writing-framework.md)).

### Format for Scanning

If content is easy for human eyes to scan, it is easy for AI to extract:

| Format | When to Use | AI Extraction Benefit |
|---|---|---|
| Bullet points | Features, steps, requirements | AI pulls as structured lists |
| Comparison tables | Product vs. product, method vs. method | AI extracts directly as tabular data |
| H2/H3 subheadings | Topic boundaries | AI uses headings as chunk delimiters |
| Bold key claims | Statistics, recommendations | AI treats bold as emphasis signals |
| Numbered lists | Sequential processes | AI presents as step-by-step answers |

### Mini-Blogs Inside the Blog

Treat every H2 section as a **mini-blog post** that answers one specific, core question entirely. Each H2 section must:

- Have a clear question it answers (stated or implied in the heading)
- Contain a complete answer within that section
- Not rely on other sections for context
- Be extractable as a standalone snippet

This is the structural implementation of the **Stand-Alone Rule** and **Chunk Autonomy** principles.

---

## Strategy 2: Intent & Conversational Search

People do not talk to AI the way they type into traditional Google Search.

### The Query Shift

| Traditional SEO Query | Conversational AI Query |
|---|---|
| "Best student phones 2025" | "What is the best phone for college students who take Zoom classes and photos?" |
| "cheap goldfish food" | "What should I feed my goldfish if I'm on a tight budget and live in a hot climate?" |
| "SEO tools comparison" | "Which SEO tool is best for a small business with no technical team?" |

### Direct Answer + Expansion

When answering conversational questions:

1. **Give the direct answer first**: "The Samsung Galaxy A54 is the best phone for college students who take Zoom classes."
2. **Then expand on constraints**: "It supports stylus input for notes, has a 48MP camera for photos, and is water-resistant — important if you're carrying it across campus in the rain."

### Natural Language Rules

| ❌ Keyword-Stuffed | ✅ Natural Language |
|---|---|
| "Best student phone 2025 cheap student phone for college student best phone" | "If you're heading to college and need a phone that handles Zoom calls without stuttering, here's what to look for." |

**Key principle**: AI detects and ignores robotic, overly-optimized content. Write exactly how humans speak to each other. The content-creation-protocol's Customer Language extraction (from Reddit) ensures your writing matches real conversational patterns.

---

## Strategy 3: Schema Markup & Technical Optimization

You must help AI bots understand your site's structure using code. Schema markup tells the AI exactly what each element on your page is.

### LD-JSON Schema Implementation

Add schema markup to every page using `<script type="application/ld+json">` tags.

### Common Schemas by Content Type

| Content Type | Required Schemas | Key Properties |
|---|---|---|
| **Blog Posts** | `Article`, `FAQ`, `HowTo` | `headline`, `author`, `datePublished`, `dateModified` |
| **E-commerce** | `Product`, `Review`, `Offer` | `name`, `price`, `availability`, `aggregateRating` |
| **Local Business** | `LocalBusiness`, `Organization` | `name`, `address`, `telephone`, `geo`, `openingHours` |
| **Person/Author** | `Person` | `name`, `url`, `sameAs` (social links), `jobTitle` |
| **FAQ Pages** | `FAQPage`, `Question`, `Answer` | `name` (question text), `acceptedAnswer` |

### Article Schema Template

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[Article Title]",
  "author": {
    "@type": "Person",
    "name": "[Author Name]",
    "url": "[Author Profile URL]",
    "sameAs": [
      "https://linkedin.com/in/[profile]",
      "https://youtube.com/@[channel]",
      "https://twitter.com/[handle]"
    ]
  },
  "datePublished": "2025-05-15",
  "dateModified": "2025-06-20",
  "publisher": {
    "@type": "Organization",
    "name": "[Site Name]",
    "logo": {
      "@type": "ImageObject",
      "url": "[Logo URL]"
    }
  }
}
```

### FAQ Schema Template

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[FAQ Question]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[4-sentence FAQ answer following the template]"
      }
    }
  ]
}
```

### Schema Audit Checklist

- [ ] Every blog post has `Article` schema with `author` and `dateModified`
- [ ] Every FAQ section has `FAQPage` schema
- [ ] Author profile has `Person` schema with `sameAs` links
- [ ] E-commerce pages have `Product` and `Review` schemas
- [ ] Local business pages have `LocalBusiness` schema with `geo` coordinates
- [ ] All schemas validate at [schema.org validator](https://validator.schema.org/)

---

## Strategy 4: Multi-Platform Authority

AI models do not just read your blog — they scan the entire internet to verify your authority. If you only exist on your website, AI won't trust you.

### The Authority Ecosystem

| Platform | Content Type | AEO Benefit |
|---|---|---|
| **YouTube** | Video tutorials, reviews, comparisons | AI cross-references video transcripts with written content |
| **LinkedIn** | Professional articles, carousels, thought leadership | AI validates author expertise and professional credentials |
| **Reddit** | Community answers, discussions | AI heavily indexes Reddit for conversational patterns |
| **GitHub** | Code, documentation, open source | AI validates technical expertise for tech topics |
| **Quora** | Expert answers | AI pulls Quora answers for "What/Why/How" queries |
| **Podcasts** | Audio content (transcribed) | AI indexes podcast transcripts for authority signals |
| **X (Twitter)** | Threads, commentary | AI indexes for real-time expert opinions |

### Actionable Steps

1. **Link author bio to social profiles using `sameAs` schema**: This tells AI that the author on your blog is the same person on LinkedIn and YouTube

2. **Repurpose content across platforms**:
   - Blog post → LinkedIn carousel
   - Blog post → YouTube Short (key points in 60 seconds)
   - Blog post → X thread (one key insight per tweet)
   - FAQ section → Quora answers (using the same 4-sentence template)

3. **Use your real identity**:
   - Real name (not "Admin" or "Staff Writer")
   - Real photo (not AI-generated profile pictures)
   - Consistent bio across all platforms
   - Same headshot everywhere

### Cross-Platform Consistency Rule

Your messaging must be **identical** across all platforms. This feeds directly into the Consensus Strategy (see [consensus-building.md](https://github.com/aaron-he-zhu/seo-geo-claude-skills/blob/main/optimize/aeo-optimizer/references/consensus-building.md)):

- Same USP phrasing on website, LinkedIn, and YouTube
- Same statistics cited across all platforms
- Same brand positioning everywhere
- AI checks for consistency across 10+ sources (Filter A: Consistency)

---

## Strategy 5: AI Engine Indexing & Signals

You must explicitly allow AI bots to read and learn from your content.

### Robots.txt Configuration

Check your `robots.txt` file. If you have:

```
User-agent: *
Disallow: /
```

You are **actively blocking AI bots** from reading your site. You must modify this to allow AI crawlers.

**Recommended robots.txt for AEO:**

```
User-agent: *
Allow: /

User-agent: GPTBot
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

Sitemap: https://yourdomain.com/sitemap.xml
```

**Key AI bot user agents to allow:**

| Bot | Company | Purpose |
|---|---|---|
| `GPTBot` | OpenAI | ChatGPT training and retrieval |
| `Google-Extended` | Google | Gemini / AI Overviews |
| `ClaudeBot` | Anthropic | Claude training and retrieval |
| `PerplexityBot` | Perplexity | Perplexity AI search |
| `Applebot-Extended` | Apple | Siri / Apple Intelligence |

### Publisher Programs

Some AI engines have voluntary publisher programs. Submitting your site directly increases the chances of being cited:

| Program | Benefit |
|---|---|
| Google Search Console | Indexing for AI Overviews |
| Bing Webmaster Tools | Indexing for Copilot |
| Perplexity Publisher Hub | Direct citation in Perplexity results |

### Content Freshness Signals

AI heavily favors recent content. A newly updated blog post will be picked over an older article because AI wants to provide the most current answer.

**Content freshness strategy:**

| Action | Frequency | Impact |
|---|---|---|
| Update `dateModified` in schema | Every content refresh | AI sees the page as recently updated |
| Add new data/stats to existing posts | Monthly | AI prefers current data points |
| Refresh FAQ sections with new questions | Bi-monthly | Captures emerging AI queries |
| Add new constraint angles | Quarterly | Addresses evolving user scenarios |
| Full article rewrite if > 12 months old | Annually | Prevents content decay |

**Critical rule**: Do not just change the date — add **genuine new information**. AI can detect superficial updates.

---

## Technical AEO Audit Checklist

### Content Structure
- [ ] E.E.A.T. credentials in first 2 sentences
- [ ] Direct answer in first paragraph (A.Q.C.E. Answer layer)
- [ ] Comparison tables instead of prose comparisons
- [ ] H2 sections function as stand-alone mini-blogs
- [ ] Conversational language matching real user patterns

### Schema Markup
- [ ] `Article` schema with author and dates on every post
- [ ] `FAQPage` schema on pages with FAQ sections
- [ ] `Person` schema with `sameAs` for author profiles
- [ ] All schemas validate without errors

### Multi-Platform
- [ ] Author profile linked to 3+ platforms via `sameAs`
- [ ] Content repurposed to at least 2 additional platforms
- [ ] Real name and photo used consistently
- [ ] Same USP phrasing across all platforms

### AI Indexing
- [ ] `robots.txt` allows GPTBot, ClaudeBot, Google-Extended, PerplexityBot
- [ ] Site submitted to major publisher programs
- [ ] `dateModified` updated on all refreshed content
- [ ] Sitemap.xml current and submitted

## Source

Knowledge derived from:
- Video 14: [GEO Tactical Strategies — Technical Implementation](http://www.youtube.com/watch?v=VIDEO_14_ID)
