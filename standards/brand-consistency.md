# Standard: Brand Consistency & Asset Fidelity
**Category:** Brand Governance Standard  
**Governing Role:** The Creative Director & The Quality Assurance Inspector  
**Enforcement:** Mandatory across all client campaigns, copywriting, and visual media.

---

## 1. The Brand Profile as Single Source of Truth

Every campaign, video, ad, or strategy document must anchor directly to a verified brand profile in `brands/<brand-name>.md`:
- If an existing profile exists (e.g. `brands/little-ride-tz.md`, `brands/stratiq.md`), all design tokens, color hex codes, and messaging pillars are **strictly binding**.
- If working with a new client, an authoritative profile must be generated in `brands/<brand-name>.md` and approved by the Creative Director **before** any visual or copy production begins.

---

## 2. Design Token Immutability

1. **Color Hex Codes:** Brand colors must be utilized with 100% precision. Substituting a brand color with an arbitrary shade (e.g. using generic orange `#ff6600` instead of Little Ride Amber `#f59e0b`) is an automatic QA rejection.
2. **Typography Families:** Official brand font pairings must be respected in all rendered web assets and motion graphics. If a local system font is substituted, it must belong to the exact approved fallback family documented in the brand profile.
3. **Logo Integrity & Safe Zones:**
   - Maintain a minimum clear space surrounding the logo equal to the height of the logo's primary lettermark.
   - Never stretch, squash, rotate, recolor, or add heavy drop-shadows to official client logos.

---

## 3. Brand Tone & Voice Boundaries

Every brand profile defines explicit tone guardrails across 4 dimensions:

| Dimension | Spectrum A | Spectrum B | Governance Rule |
| :--- | :---: | :---: | :--- |
| **Formality** | Corporate / Institutional | Casual / Conversational | Match exact client target audience (B2B vs. D2C). |
| **Energy** | Calm & Grounded | Dynamic & High-Tempo | Governs kinetic animation velocity and copy rhythm. |
| **Humor** | Witty & Irreverent | Serious & Pragmatic | Ban sarcasm in risk-sensitive domains (fintech/logistics). |
| **Perspective** | Direct ("We / You") | Third-Person Narrative | Enforce direct second-person address for CTAs. |

---

## 4. Pre-Flight Brand Alignment Check

Before marking any project deliverable complete, the QA Inspector must confirm:
- [ ] Primary, secondary, and accent colors match `brands/<brand>.md` exactly.
- [ ] Primary headline directly reinforces at least one approved core brand value proposition.
- [ ] Tone conforms strictly to brand voice guardrails.
- [ ] Pricing models, currency codes (e.g. TZS, USD, EUR), and regional terminologies are accurate.
