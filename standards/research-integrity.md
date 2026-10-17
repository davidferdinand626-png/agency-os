# Standard: Research Integrity & Factual Verification
**Category:** Operational Standard  
**Governing Role:** The Strategy Director & The Quality Assurance Inspector  
**Enforcement:** Mandatory for all research deliverables, strategy reports, and financial models.

---

## 1. Core Principles of Research Integrity

Agency OS strictly forbids unsubstantiated claims, fabricated statistics, and generic AI filler. Every statement must either be verified against primary sources, calculated from explicit baseline assumptions, or marked with its exact epistemic confidence level.

---

## 2. Mandatory Verification Taxonomy

Every key finding, quantitative metric, and market claim must include an inline factual label:

- `[VERIFIED]`: Confirmed via direct primary documents, verified regulatory filings, official census data, or live programmatic API queries.
- `[INFERRED]`: Mathematically or logically derived from two or more verified facts using documented calculation formulas.
- `[ASSUMED]`: Stated as a baseline operational assumption where empirical data is unavailable. The assumption parameters must be made completely transparent.
- `[NOT TESTED]`: Stated capability or hypothesis that has not yet been executed in our local environment.
- `[BLOCKED]`: Identified capability or dependency that cannot be executed due to verified host hardware or environment constraints.

---

## 3. Data Source Hierarchy

When conducting research, prioritize data sources according to this hierarchy:

1. **Tier 1 (Primary / Authoritative):**
   - Government statistical bureaus (e.g. NBS Tanzania, KNBS Kenya).
   - Regulatory bodies (e.g. TCRA, Central Banks, SEC/FCA).
   - Audited annual financial statements and earnings reports.
2. **Tier 2 (Secondary Industry Intelligence):**
   - Verified industry analyst databases (GSMA, World Bank, IMF, Statista).
   - Academic papers and peer-reviewed studies.
   - Public APIs cataloged in `public-apis/public-apis`.
3. **Tier 3 (Competitive Direct Observation):**
   - Direct inspection of competitor websites, pricing pages, terms of service, and app store listings via `competitor-teardown`.
   - Crawled landing page DOM structures and verified public social media profiles.

---

## 4. Quantitative Modeling Standards (TAM / SAM / SOM)

All market sizing models must adhere to these mathematical guidelines:
- **Bottom-Up First:** Prioritize bottom-up models ($\text{Target Customers} \times \text{Average Revenue Per Unit}$) over generic top-down percentages.
- **Explicit Parameter Disclosure:** Every model variable (e.g., target population, smartphone penetration rate, commuting frequency, average ticket size) must be documented in a dedicated parameter table.
- **Sensitivity Ranges:** Present Conservative, Expected, and Aggressive scenarios with clear variance drivers.

---

## 5. Zero-Spend Research Boundaries

- Rely strictly on open-access research, public directories, free API endpoints, and web extraction.
- Never require or purchase paid research reports (e.g., Gartner, Forrester, paid Euromonitor).
- If high-value data is gated behind a paywall, synthesize open proxy datasets and explicitly state the assumption boundary using `[INFERRED]` or `[ASSUMED]`.
