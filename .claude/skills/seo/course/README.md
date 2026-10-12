# Claude SEO: how it works (course guide)

These notes come from the user's Claude SEO Mastery course (AI Marketing Hub Pro). Use them to explain what each command does, which order to run things in, and how to read the results. The course was recorded on an older release (13 sub-skills, 7 agents). This bundle is v2.4.2 (25+ sub-skills, 19 agents), so every command in the course still works, and there are more.

## The core loop (Lesson 1.4)
1. **Audit the site**: `/seo audit <url>` → `FULL-AUDIT-REPORT.md` + `ACTION-PLAN.md`, with a 0–100 SEO Health Score.
2. **Find weak pages**: which URLs drag the score down.
3. **Deep-dive each page**: `/seo page <url>` (five score cards; fix the lowest card first).
4. **Fix by priority**: Critical → High → Medium → Low. Fix template-level issues (on every page) before page-specific ones.
5. **Re-run and verify** that the score went up.

## Lesson → command map

| Lesson | Command | File |
|---|---|---|
| What is Claude SEO | overview of the commands | `what-is-claude-seo.md` |
| 1.1 Installing | install, then `/seo` lists commands | `lesson-1.1-installing-claude-seo.md` |
| 1.2 First audit | `/seo audit <url>` | `lesson-1.2-your-first-audit.md` |
| 1.3 Reading reports | read ACTION-PLAN first; PDF report prompt | `lesson-1.3-reading-audit-reports.md` |
| 1.4 Single page | `/seo page <url>` | `lesson-1.4-single-page-deep-dive.md` |
| 2.1 Technical | `/seo technical <url>` (9 categories) | `lesson-2.1-technical-audit.md` |
| 2.2 AI crawlers | robots.txt strategy for GPTBot, OAI-SearchBot, ClaudeBot… (part of `/seo technical` and `/seo geo`) | `lesson-2.2-ai-crawler-management.md` |
| 2.3 Core Web Vitals | LCP / INP / CLS (`/seo technical`, live data via `/seo google`) | `lesson-2.3-core-web-vitals.md` |
| 2.4 JavaScript SEO | CSR vs SSR detection | `lesson-2.4-javascript-seo.md` |
| 2.5 E-E-A-T | `/seo content <url>` | `lesson-2.5-eeat-content-analysis.md` |
| 2.6 Images | `/seo images <url>` | `lesson-2.6-image-optimization.md` |
| 2.7 Schema | `/seo schema <url>` | `lesson-2.7-schema-markup.md` |
| 2.8 Sitemap | `/seo sitemap <url>` | `lesson-2.8-sitemap-analysis.md` |
| Extension: DataForSEO | `/seo dataforseo …` (needs a DataForSEO account) | `extension-dataforseo.md` |
| Extension: Drift Monitor | `/seo drift baseline | compare | history <url>` | `extension-seo-drift.md`, `examples/seo-drift-demo-report.pdf` |
| Outrank Everyone L2 | installing Claude SEO + Claude Blog | `outrank-lesson-2-install-skills.md` |

Module 3 (AI Search Strategy) and Module 4 (Client Delivery) weren't in the saved pages. For AI search, use `/seo geo` and `/seo agentic`. For client delivery, chain `/seo audit` → `/seo plan <business-type>` → a PDF report.

## AEO / GEO / LLM optimization in this bundle
- `/seo geo <url>`: AI Overviews, ChatGPT, Perplexity and Copilot visibility. Covers AI-crawler access, llms.txt, passage-level citability, and brand-mention signals.
- `/seo agentic <url>`: whether AI agents can use the site (Lighthouse Agentic Browsing, accessibility tree, WebMCP, Markdown access).
- `/seo schema <url>`: entities and structured data that AI systems rely on.
- `/seo content <url>`: E-E-A-T and answer-ready, citable writing.
- Lesson 2.2's robots.txt strategies: block training but allow search (the course's recommendation), block all, or allow all.

## Reading a report (Lesson 1.3)
Start with the executive summary: health score, top issues, quick wins. Then read `ACTION-PLAN.md`. Check whether each finding is template-level or page-specific. Critical items often block other improvements. A finished example is in `examples/reading-audit-reports.pdf`.

## PDF report prompt (from Lesson 1.3)
After an audit, ask for a professional PDF that includes:
- all findings and recommendations, with screenshots inline next to their sections
- bar, pie or line charts where comparisons help
- a title page, table of contents, section dividers and page numbers
- consistent styling, with no overlap or clipping

Check the finished PDF for layout problems before delivering it.
