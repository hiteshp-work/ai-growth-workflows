# Answer Engine Optimization (AEO) Visibility Audit Engine

A structured prompt library and evaluation framework for measuring how generative AI engines (ChatGPT, Claude, Perplexity, Google AI Overviews) perceive, categorize, and recommend your B2B SaaS software category.

---

## 🎯 Audit Framework Overview

AEO measures your brand’s inclusion, positioning, and sentiment when enterprise buyers use LLMs as discovery engines instead of traditional search bars.

```text
LLM Buyer Query ➔ Category Mention % ➔ Recommendation Rank ➔ Feature Hallucination Check

```

---

## 🧪 Systematic Audit Prompts

Run these prompts across OpenAI GPT-4o, Anthropic Claude 3.5, and Perplexity in fresh incognito sessions:

### 1. Category Landscape & Recommendation Discovery

```text
I am evaluating [Software Category, e.g., B2B Revenue Attribution Software] for a [Company Profile, e.g., 200-person B2B SaaS company using HubSpot and Salesforce]. 

What are the top 5 platforms on the market today? For each platform, provide:
1. Who it is best suited for (SMB vs. Enterprise)
2. Primary architectural strengths
3. Known limitations or common integration complaints
4. Standard pricing tier estimates

```

### 2. Direct Head-to-Head Comparison Query

```text
Compare [Your Brand] vs. [Competitor A] and [Competitor B]. 

Evaluate them across these four operational criteria:
1. Ease of MarTech implementation & time-to-value
2. Multi-touch attribution modeling flexibility
3. Native CRM bi-directional integrations
4. Total cost of ownership

Which one would you recommend if our primary KPI is reducing blended CAC while maintaining data governance?

```

### 3. Gap Analysis & Source Citation Extraction (Perplexity / Search-Grounded LLMs)

```text
What are software buyers and peer review sites (like G2, Capterra, and TrustRadius) saying about [Your Brand]? 

Summarize the consensus on:
- What users praise most
- What features users say are missing
- Provide the direct domain URLs you retrieved this assessment from

```

---

## 📊 AEO Scorecard Template

Track weekly audits across LLM providers to measure brand visibility drift:

| Date | Engine Tested | Category Query | Brand Mentioned? (Y/N) | Recommendation Position | Cited Sources | Action Item / Content Gap Identified |
| --- | --- | --- | --- | --- | --- | --- |
| `2026-09-01` | ChatGPT Plus | "Best B2B attribution tools" | Yes | #2 | G2, Vendor Site | Add comparison landing page against Competitor X |
| `2026-09-01` | Perplexity | "Best software for enterprise ABM" | No | Unranked | TrustRadius, Reddit | Seed product teardown on industry community forums |
| `2026-09-01` | Claude 3.5 | "Revenue tracking tools for HubSpot" | Yes | #3 | Integrations Dir | Update HubSpot App Marketplace feature listings |

---

---
