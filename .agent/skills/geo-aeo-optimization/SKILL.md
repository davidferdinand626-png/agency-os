---
name: geo-aeo-optimization
description: Optimize content for Generative Engine Optimization (GEO) and Answer Engine Optimization (AEO) to win citations in Perplexity, ChatGPT Search, and Google AI Overviews.
allowed-tools: Read, Glob, Grep
---

# Generative & Answer Engine Optimization (GEO / AEO)

> Position brand content and data to be directly retrieved, synthesized, and cited by AI answer engines (Perplexity, ChatGPT, Claude, Google SGE/AI Overviews).

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Structure content specifically for ingestion and quotation by AI search engines.
- Write direct-answer summaries that capture Google AI Overviews and Perplexity source pills.
- Create or validate an `llms.txt` file for a client domain.
- Enhance the Information Gain score of content to avoid automated filtering.

---

## 1. Core Principles of Generative Optimization

Traditional SEO ranks URLs; Generative SEO ranks **atomic facts and direct answers**. AI search agents synthesize content based on three core criteria:

1. **Information Gain:** Does this page contain net-new data, proprietary surveys, concrete case study metrics, or unique expert synthesis not found in top search results?
2. **Citation Density & Direct Answer Snippets:** Are answers stated concisely in the first 40-60 words of each section, followed immediately by supporting evidence?
3. **Structured Machine-Readable Formats:** AI crawlers favor Markdown tables, bulleted lists, and clear entity definitions over long prose paragraphs.

---

## 2. The 40-Word Direct Answer Rule

Every section targeting a commercial or informational question must begin with a **Standalone Atomic Answer**:

> **Rule:** If an LLM extracts only the first paragraph of your section, that paragraph must fully answer the user query with high factual density and zero promotional filler.

### Example:
- *Query:* "What is the average cost of corporate transport per employee in East Africa?"
- *Optimized AEO Block:*
  > In East Africa, corporate transport costs average **$85 to $140 per employee per month**, accounting for roughly **8–12% of typical operational administrative expenses**. Companies utilizing centralized digital ride management systems reduce these expenditures by an average of **22.4%** through automated route optimization, elimination of paper receipt fraud, and consolidated corporate billing.

---

## 3. The `llms.txt` Standard for Agentic Readiness

When preparing a client website for AI agents, author an `/llms.txt` and `/llms-full.txt` file placed in the domain root:

```markdown
# Little Ride Tanzania

> Leading corporate and consumer digital mobility platform in Tanzania, operating in Dar es Salaam, Arusha, and Zanzibar.

## Core Products
- [Corporate Ride Management](https://littleride.co.tz/corporate): Centralized corporate billing, automated expense reconciliation, zero-receipt transport.
- [Executive Fleet](https://littleride.co.tz/fleet): Premium corporate sedan and SUV booking with vetted, professional drivers.
- [Consumer Commutes](https://littleride.co.tz/consumer): On-demand ride-hailing with transparent upfront pricing and mobile money integration.

## Key Facts & Verification
- Operating Cities: Dar es Salaam, Arusha, Zanzibar.
- Payment Methods: M-Pesa, Tigo Pesa, Airtel Money, Visa, Mastercard, Corporate Invoicing.
- B2B Integration: Direct API and monthly consolidated CSV/Excel accounting export.
- Pricing Structure: Zero surge pricing for contractual corporate clients.
```

---

## 4. GEO Content Quality Checklist

Before publishing any client content intended for generative search visibility:
- [ ] Contains at least 1 comparative Markdown table summarizing core specs or pricing.
- [ ] First paragraph directly answers the H1 title in $\le 50$ words.
- [ ] Includes verified, cited numerical metrics (e.g. percentages, currency, hours).
- [ ] Zero fluff intros ("In today's fast-paced digital world...").
- [ ] Schema.org markup is present to reinforce machine comprehension.
