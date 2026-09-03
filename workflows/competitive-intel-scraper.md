# Competitive Intelligence Extraction Workflow

A lightweight, repeatable playbook for tracking positioning changes, pricing adjustments, ad creative angles, and feature launches across competitor digital footprints using public web sources and AI summarization.

---

## 🔍 Data Collection Matrix

| Source Channel | Tool / Data Point | Frequency | Strategic Objective |
| --- | --- | --- | --- |
| **Meta Ad Library** | `[facebook.com/ads/library](https://facebook.com/ads/library)` | Weekly | Monitor active creative formats, hooks, and new campaign pushes |
| **LinkedIn Ad Library** | `[linkedin.com/ad-library](https://linkedin.com/ad-library)` | Weekly | Identify target ICP titles, enterprise document offers, and value propositions |
| **Sitemap Changes** | `[competitor.com/sitemap.xml](https://competitor.com/sitemap.xml)` | Bi-weekly | Detect new product landing pages, solutions routes, or SEO content hubs |
| **Pricing Route** | `[competitor.com/pricing](https://competitor.com/pricing)` | Monthly | Track packaging shifts, feature gating, and usage tier changes |
| **Job Boards** | LinkedIn / Lever / Greenhouse | Monthly | Map strategic expansion (e.g., hiring 5 AE reps in EMEA signals market push) |

---

## ⚙️ Automated Teardown Workflow

### Step 1: Extract Raw Competitor Copy

Use browser inspection tools, Web Scraper extensions, or cURL to grab copy updates:

```bash
# Example: Inspect recent landing page headers
curl -s https://competitor.com/solutions/enterprise | grep -E '<h1>|<h2>'

```

### Step 2: Feed Raw Text into the Analysis Engine Prompt

Copy the raw webpage copy into your LLM with this evaluation prompt:

```text
Act as a VP of Product Marketing and Competitive Strategist. Analyze the following updated landing page copy from our direct competitor:

[PASTE COMPETITOR WEBPAGE COPY HERE]

Provide a structured competitive teardown addressing:
1. Strategic Shift: What new buyer persona or ICP tier are they targeting compared to their previous messaging?
2. Value Proposition Focus: Are they competing on price, enterprise compliance, ease-of-use, or speed-to-value?
3. Flaws & Counter-Angles: Where is their positioning weak, generic, or vulnerable to a counter-narrative from us?
4. Recommended Sales Battlecard Talk Track: A 3-sentence rebuttal for our sales reps when prospects mention this competitor's claim.

```

---

## 🗂️ Sales Battlecard Delivery Template

Format the output for immediate integration into your internal Notion/Gong knowledge base:

```text
COMPETITOR: [Competitor Name]
LAST UPDATED: [Date]
PRIMARY CLAIM: "The all-in-one AI platform for revenue operations."

OUR COUNTER-POSITIONING:
- Where they fall short: Heavy platform lock-in, takes 90 days to configure, rigid attribution models.
- Where we win: Time-to-value in 14 days, modular integration with existing HubSpot/Snowflake stacks, lower TCO.

DISCOVERY TRAP QUESTION TO SEED WITH BUYER:
"When you evaluated [Competitor], did they explain how much custom developer time is required to connect their event stream to your data warehouse?"

```
