---
name: conversion-rate-optimization
description: Systematically audit and optimize landing pages, conversion funnels, checkout flows, and forms using empirical CRO heuristics.
allowed-tools: Read, Glob, Grep
---

# Conversion Rate Optimization (CRO) & Funnel Heuristics

> Maximize visitor-to-customer conversion rates by eliminating friction, amplifying perceived value, and establishing trust.

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Conduct an exhaustive heuristic teardown of an existing landing page or funnel.
- Design high-converting sales funnels from scratch.
- Formulate A/B test hypotheses with quantifiable success metrics.
- Optimize signup forms, checkout flows, or lead capture widgets.

---

## 1. The LIFT Heuristic Evaluation Model

Every page or funnel step must be audited across the 6 LIFT dimensions:

1. **Value Proposition (The Engine):** Is the unique reason to buy obvious within the first 5 seconds? Does the perceived benefit drastically outweigh the perceived cost?
2. **Relevance:** Does the page match the exact scent, intent, and promise of the referring ad or search query?
3. **Clarity:** Is the layout intuitive? Can a user understand what the product is, how it works, and who it is for without scrolling?
4. **Urgency:** Is there an authentic reason to take action right now (limited inventory, onboarding cohort cut-off, bonus expiration)?
5. **Anxiety (Conversion Killer):** What doubts or hesitations does the user have? Are there trust badges, security icons, guarantees, transparent terms, and verifiable social proof?
6. **Distraction (Conversion Leaker):** Are there extraneous navigation links, competing CTAs, redundant social icons, or irrelevant animations pulling the user off the conversion path?

---

## 2. The Above-the-Fold Audit Checklist

A user should never have to scroll to answer these 4 questions:
- [ ] **What is this?** (Clear product category and descriptive headline)
- [ ] **Who is it for?** (Target persona explicitly named or signaled)
- [ ] **What do I get?** (Top 3 tangible benefits, not just technical features)
- [ ] **What do I do next?** (Single primary CTA with high color contrast)

---

## 3. Form & Checkout Friction Reduction Rules

1. **Rule of Field Minimization:** Every additional form field reduces conversion by an average of 4-7%. Strip all non-essential fields (e.g., remove "Company Phone" and "Fax" from initial B2B signup).
2. **Inline Validation:** Provide instant visual confirmation (green checkmark) upon field completion. Never wait until form submission to display errors.
3. **Progressive Disclosure:** For multi-step forms (e.g. quote calculators), place low-friction questions first (e.g. "What type of ride do you need?") before requesting personal contact information on the final step.
4. **Social Proof Proximity:** Position an authoritative quote or security seal directly adjacent to the payment or submit button.

---

## 4. CRO Audit Output Schema

When conducting a CRO audit, deliver the report using this structured format:

```markdown
# Conversion Rate Optimization Audit: [Target URL/Page]

## 1. Executive Summary
- Current Primary Funnel Goal: [e.g. B2B Demo Request]
- Overall Heuristic Health Score: [1-100]
- Top 3 Conversion Blockers Identified:
  1. [Blocker 1]
  2. [Blocker 2]
  3. [Blocker 3]

## 2. LIFT Model Analysis
| Dimension | Rating (1-5) | Critical Findings & Deficiencies |
| :--- | :---: | :--- |
| Value Proposition | ⭐️⭐️⭐️ | ... |
| Clarity | ⭐️⭐️ | ... |
| Relevance | ⭐️⭐️⭐️⭐️ | ... |
| Urgency | ⭐️ | ... |
| Anxiety | ⭐️⭐️ | ... |
| Distraction | ⭐️⭐️⭐️ | ... |

## 3. Prioritized Optimization Backlog (ICE Framework)
| Priority | Experiment / Modification | Impact (1-10) | Confidence (1-10) | Ease (1-10) | ICE Score |
| :---: | :--- | :---: | :---: | :---: | :---: |
| 1 | Revamp hero headline using PAS formula | 9 | 8 | 9 | 24.0 |
| 2 | Remove top navigation on landing page | 7 | 8 | 10 | 23.3 |
| 3 | Add client logo ticker below CTA | 8 | 7 | 8 | 21.0 |
```
