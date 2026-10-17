# Workflow: Independent Crossframe QA & Quality Control
**Track:** Quality Assurance & Governance  
**Primary Agent:** The Quality Assurance Inspector (Independent Review)  
**Supporting Skills:** `crossframe-review`, `conversion-rate-optimization`, `anti-ai-slop-design`, `subtractive-design-mies`

---

## 1. Objective & Mandate

Provide independent, adversarial verification of all agency outputs (strategy reports, landing page designs, motion graphics, and video commercials) prior to client delivery. The QA Inspector holds full veto authority.

---

## 2. Multi-Dimensional Quality Gate Inspection

Every deliverable must pass through five rigorous quality gates:

### Gate 1: Visual Contrast & Accessibility (WCAG AA)
- [ ] Primary text luminance contrast meets or exceeds **4.5:1** against backgrounds.
- [ ] Large display text ($>24\text{px}$) meets or exceeds **3.0:1**.
- [ ] Interactive buttons and status indicators have distinct visual states (hover, active, disabled).
- [ ] Text is completely legible over dynamic video frames (tested across 10 random frame samples).

### Gate 2: Brand Token & Asset Fidelity
- [ ] Colors match the exact hexadecimal values documented in `brands/<brand>.md`.
- [ ] Typography follows approved modular scale and font pairings.
- [ ] Logos maintain mandatory clear-space buffers without distortion, skew, or unofficial coloring.

### Gate 3: Anti-AI-Slop & Subtractive Design Verification
- [ ] Zero purple/violet neon gradients or ungrounded glowing background blobs.
- [ ] Corner radii adhere to disciplined $\le 8\text{px}$ standard.
- [ ] No generic glossy 3D emojis or disconnected cartoon illustrations.
- [ ] Passed the Miesian reduction check: all extraneous decorative borders and clutter eliminated.

### Gate 4: Motion Continuity & Frame Integrity
- [ ] Video renders at consistent **60 FPS** without frame drops or micro-stutters.
- [ ] Zero accidental black frames, frozen screens, or clipping text.
- [ ] Transitions complete within 6 to 18 frames without spatial disorientation.
- [ ] Audio waveforms match scene cuts within $\pm 1$ frame (16.6ms precision).

### Gate 5: Factual Integrity & Citation Audit
- [ ] Every statistical claim and market figure carries an inline verification label (`[VERIFIED]`, `[INFERRED]`, `[ASSUMED]`).
- [ ] Primary sources and methodology formulas are documented.
- [ ] Zero unsubstantiated superlatives ("the best", "world's first") unless legally certified.

---

## 3. Formal Verdict Taxonomy & QA Report Schema

Every review conducted by the QA Inspector must conclude with a formal written report in `project-logs/`:

```markdown
# Quality Assurance Inspection Report: [Project Name]
**Inspector:** The QA Inspector (Agency OS)  
**Date:** [YYYY-MM-DD]  
**Asset Inspected:** [File Path or URL]  

## 1. Compliance Scorecard
| Quality Gate | Status | Notes / Findings |
| :--- | :---: | :--- |
| Visual Contrast & Accessibility | PASS / FAIL | Contrast ratio verified at 7.2:1 |
| Brand Token Fidelity | PASS / FAIL | Exact amber #f59e0b and zinc #09090b verified |
| Anti-AI-Slop & Taste | PASS / FAIL | Zero purple gradients, Miesian reduction applied |
| Motion Continuity & Pacing | PASS / FAIL | 60 FPS verified, cuts land on audio hits |
| Factual Integrity & Sources | PASS / FAIL | All statistics labeled and verified |

## 2. Identified Deficiencies & Required Action Items
1. [Deficiency 1]: [Specific fix required]
2. [Deficiency 2]: [Specific fix required]

## 3. Formal Quality Verdict
**VERDICT:** [APPROVED (Broadcast-Ready) | CHANGES REQUIRED (Minor Fixes) | REJECTED (Critical Defects)]

**Signature:** Independent QA Inspector, Agency OS
```
