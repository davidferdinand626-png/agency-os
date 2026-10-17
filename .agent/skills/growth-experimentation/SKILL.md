---
name: growth-experimentation
description: Design, prioritize, and analyze growth experiments and viral loops using empirical ICE/RICE scoring and scientific test rigor.
allowed-tools: Read, Glob, Grep
---

# Growth Experimentation & Scientific Testing Framework

> Eliminate opinion-based marketing by running rapid, disciplined growth experiments backed by statistical rigor and verifiable metrics.

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Generate and prioritize a marketing experiment backlog for a client or campaign.
- Formulate testable, falsifiable growth hypotheses.
- Calculate sample size, statistical significance, and minimum detectable effect (MDE).
- Design self-reinforcing viral, organic, and paid growth loops.

---

## 1. The Scientific Growth Hypothesis Standard

Never execute a test without an unambiguous hypothesis structured in this exact format:

$$\text{If we } [\text{implement specific change } X] \text{ for } [\text{target segment } Y], \text{ then } [\text{metric } Z] \text{ will increase by } [N\%] \text{ because } [\text{behavioral insight } W].$$

### Falsifiability Rule
If a hypothesis cannot be proven completely wrong within a predefined testing window (typically 14 to 30 days), it is invalid and must be rejected before launch.

---

## 2. Experiment Prioritization: The ICE Framework

Score every test idea across 3 dimensions from 1 to 10:

$$\text{ICE Score} = \frac{\text{Impact} + \text{Confidence} + \text{Ease}}{3}$$

- **Impact (1-10):** If this experiment succeeds wildly, how significantly will it move our primary North Star Metric (e.g. Qualified Pipeline, CAC reduction, Monthly Active Accounts)?
- **Confidence (1-10):** How certain are we that this will succeed based on historical data, competitor teardowns, or user interviews? (Scores of 9-10 require empirical validation from prior tests).
- **Ease (1-10):** How simple and fast is it to build and launch with current tools? (10 = <2 hours of copy/styling tweaks; 1 = requires custom engineering and backend changes).

---

## 3. The 4 Fundamental Growth Loops

When architecting long-term scalable growth, design self-reinforcing loops rather than linear funnels:

1. **Viral / Referral Loop:**
   $$\text{User joins} \longrightarrow \text{Uses product} \longrightarrow \text{Naturally exposes or invites colleague} \longrightarrow \text{Colleague joins}.$$
2. **Organic Content Loop:**
   $$\text{System publishes programmatic guide/asset} \longrightarrow \text{Search engines index} \longrightarrow \text{High-intent traffic arrives} \longrightarrow \text{New signups} \longrightarrow \text{Generates new data/content}.$$
3. **Paid Re-investment Loop:**
   $$\text{Spend } \$1 \text{ on targeted ad} \longrightarrow \text{Generate } \$3 \text{ in gross profit within 30 days} \longrightarrow \text{Reinvest profit into increased ad spend}.$$
4. **Sales-Assisted Product Loop:**
   $$\text{End-user adopts free/entry tier} \longrightarrow \text{Hits collaboration threshold} \longrightarrow \text{Automated trigger alerts sales/AE} \longrightarrow \text{Enterprise contract closed}.$$

---

## 4. Experiment Log Schema

Maintain an experiment ledger in `project-logs/experiments.md` using this layout:

```markdown
# Growth Experiment Log

| ID | Date Launched | Hypothesis | ICE Score | Status | Pre-Test Metric | Post-Test Metric | Verdict | Next Iteration |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| EXP-01 | 2026-10-20 | If we add automated corporate invoice download to the hero CTA, B2B signups will increase by 25% | 8.3 | RUNNING | 2.4% conv | TBD | IN PROGRESS | If positive, roll out to all regional landing pages |
```
