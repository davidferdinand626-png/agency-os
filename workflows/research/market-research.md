# Workflow: Market Research & Intelligence Architecture
**Track:** Research & Competitive Strategy  
**Primary Agent:** The Strategy Director & Market Researcher  
**Supporting Skills:** `competitor-teardown`, `market-sizing-analysis`, `customer-journey-mapping`, `technical-seo-audit`, `geo-aeo-optimization`

---

## 1. Objective & Scope

Produce a rigorous, data-backed market analysis, competitive teardown, and search intelligence report for a target client, product category, or regional market. All findings must adhere to `standards/research-integrity.md` with explicit factual labeling.

---

## 2. Required Input Context

Before initiating research, gather:
- Client brand profile from `brands/<brand>.md`.
- Target geographical boundary (e.g. Dar es Salaam, Tanzania; Nairobi, Kenya; Global B2B).
- Identified top 3 incumbent competitors.
- Zero-cost data sources (Census, TCRA, GSMA, public-apis directory).

---

## 3. Step-by-Step Execution Protocol

### Step 1: Quantitative TAM / SAM / SOM Financial Modeling
1. Load the `market-sizing-analysis` skill.
2. Establish demographic baseline metrics (population, urban concentration, internet/smartphone penetration, target income cohort).
3. Build a bottom-up formula:
   $$\text{TAM} = \text{Total Potential Users in Geography} \times \text{Annual Usage Frequency} \times \text{Average Order Value (AOV)}$$
   $$\text{SAM} = \text{TAM} \times \text{Smartphone Penetration \%} \times \text{Digital Payment Readiness \%}$$
   $$\text{SOM} = \text{SAM} \times \text{Realistic Target Market Share (Year 1-3: 5\% to 15\%)}$$
4. Present findings in a sensitivity table (Conservative, Expected, Aggressive).

### Step 2: Competitive Teardown & Positioning Matrix
1. Load the `competitor-teardown` skill.
2. Audit the top 3 competitors across 6 vectors:
   - Pricing architecture & commission models.
   - Core value proposition & marketing hooks.
   - App UX / friction points (from customer reviews and social complaints).
   - Trust signals & safety features.
   - Corporate / B2B capabilities (invoicing, fleet management).
   - Paid ad creative angles (Meta Ad Library / Google Search).
3. Identify the "White Space Opportunity": where competitors are vulnerable or indifferent.

### Step 3: Customer Journey & Friction Mapping
1. Load the `customer-journey-mapping` skill.
2. Map the 5 lifecycle stages (Awareness, Consideration, Decision, Retention, Advocacy).
3. Detail the specific psychological friction points preventing conversion at each stage.

### Step 4: Search Engine & Generative Engine Intelligence (SEO / GEO / AEO)
1. Load `technical-seo-audit` and `geo-aeo-optimization` skills.
2. Identify high-intent organic search queries and questions asked in AI engines (Perplexity, ChatGPT, Claude).
3. Define the atomic answer blocks and schema markup needed to capture Google Rich Snippets and AI Overview citations.

---

## 4. Deliverable Artifact Schema

Save research deliverables to `research/<project-name>-market-research.md` using this layout:

```markdown
# Market Research & Intelligence Report: [Client / Target Market]
**Factual Confidence:** Production-Grade / Audited  
**Date:** [YYYY-MM-DD]  
**Lead Strategist:** Strategy Director (Agency OS)  

## 1. Executive Summary & Strategic Theses
- Thesis 1: [Core market opportunity]
- Thesis 2: [Competitor vulnerability]
- Thesis 3: [Target conversion angle]

## 2. Quantitative Market Sizing (TAM / SAM / SOM)
[Parameters table + Formula derivation + Sensitivity Matrix]

## 3. In-Depth Competitive Teardown (Top 3 Incumbents)
[Feature comparison matrix + Ad strategy analysis + White space roadmap]

## 4. Customer Journey & Friction Architecture
[5-stage journey matrix with emotional triggers and agency interventions]

## 5. SEO & Generative Engine (AEO) Opportunities
[Keyword target list + llms.txt configuration + Structured FAQ schema]
```
