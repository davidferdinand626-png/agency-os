# Workflow: Multi-Channel Campaign Launch Architecture
**Track:** Marketing Strategy & Growth  
**Primary Agent:** The Strategy Director & Creative Director  
**Supporting Skills:** `launch-strategy`, `copywriting-frameworks`, `conversion-rate-optimization`, `growth-experimentation`, `social-distribution-engine`, `email-marketing-sequences`, `influencer-marketing`

---

## 1. Objective & Scope

Design, budget, schedule, and execute a complete go-to-market campaign across paid acquisition, organic social, email lifecycle marketing, and creator partnerships. Governed by zero-spend internal production and empirical CRO heuristics.

---

## 2. Step-by-Step Procedure

### Step 1: Strategic Angle & Value Proposition Formulation
1. Load `copywriting-frameworks`.
2. Extract the primary customer pain point from `workflows/research/`.
3. Draft 3 distinct campaign angles:
   - **Angle 1 (Direct PAS):** Urgent operational friction -> agitated financial/time cost -> product as definitive relief.
   - **Angle 2 (AIDA Narrative):** High-curiosity counter-intuitive hook -> customer aspiration -> proof -> frictionless call to action.
   - **Angle 3 (Social Proof & Risk Reversal):** Enterprise peer adoption -> zero-risk pilot guarantee.

### Step 2: Funnel Architecture & CRO Friction Audit
1. Load `conversion-rate-optimization` and `customer-journey-mapping`.
2. Map the conversion path: Ad Impression -> Landing Page -> Registration -> First Core Action -> Payment.
3. Apply LIFT heuristics: ensure hero value proposition is clear within 5 seconds, eliminate extraneous navigation links, and reduce form fields to the bare minimum.

### Step 3: Omnichannel Content & Distribution Plan
1. Load `social-distribution-engine`:
   - Draft LinkedIn authority posts and carousel specs for B2B executives.
   - Draft high-velocity X/Twitter threads for early adopters and tech operators.
   - Draft short-form vertical video hooks (9:16) for TikTok / Instagram Reels.
2. Load `email-marketing-sequences`:
   - Construct a 4-touch cold B2B outbound sequence.
   - Build a 5-day inbound lead nurture and welcome drip.

### Step 4: Creator & Influencer Roster Construction
1. Load `influencer-marketing`:
   - Segment creators into Tier 1 (Macro culture reach), Tier 2 (Hyper-local community trust), and Tier 3 (Niche business specialists).
   - Write creative briefs with strict visual continuity and brand token compliance.

### Step 5: Growth Experimentation & ICE Backlog
1. Load `growth-experimentation`:
   - Populate a prioritized backlog of 5-10 falsifiable marketing experiments.
   - Score each test by Impact, Confidence, and Ease (ICE framework).
   - Define minimum detectable effect (MDE) and 14-day evaluation windows.

---

## 3. Campaign Deliverable Schema

Save campaign deliverables to `workflows/marketing-strategy/<campaign-name>-plan.md`:

```markdown
# Comprehensive Campaign Launch Plan: [Campaign Title]
**Client:** [Client Name] | **Target Launch:** [Date] | **Governing Framework:** fCMO Sprint

## 1. Executive Strategy & Core Value Propositions
- Hero Tagline: "..."
- Secondary Subhead: "..."
- Primary Conversion CTA: "..."

## 2. Channel Allocation & Budget Blueprint
| Channel | Target Audience | Primary Asset | Metric Target | Budget Allocation |
| :--- | :--- | :--- | :--- | :--- |
| LinkedIn Sponsored | Corporate CFOs/Ops | Case Study Video + PDF | Qualified MQLs | 35% |
| Meta / TikTok Paid | Commuters / Riders | 35s Kinetic Video Ad | App Installs / CPAs | 35% |
| Creator / Influencer| Regional Influencers| In-app Ride Experience | Social Reach & Codes| 20% |
| Email Outbound | Targeted Account List| 4-Touch Sequence | Demo Meetings Booked| 10% |

## 3. High-Converting Copywriting Suite (Ads, Landing Page, Social)
[Full copy for PAS and AIDA variants]

## 4. Email Lifecycle Sequences
[Full text of 4-touch outbound and 5-day inbound welcome series]

## 5. Prioritized ICE Growth Experimentation Backlog
[Prioritized test table with hypotheses and success thresholds]
```
