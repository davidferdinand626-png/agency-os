# Workflow: Crossframe Quality Assurance & Inspection
**Track:** Quality Assurance & Verification

---

## Objective
Conduct an independent, objective audit of rendered motion graphics and video compositions before client delivery.

## Inspection Checklist & Rubric

### 1. Frame-by-Frame Visual Audit (`crossframe-review`)
- [ ] **Contrast Check:** Does all kinetic text maintain $\ge 4.5:1$ contrast against background video?
- [ ] **Margin Safety:** Are text elements within mobile safe zones (clear of top 15% and bottom 20%)?
- [ ] **Asset Artifacting:** Are images and video plates rendered without pixelation, distortion, or improper aspect stretching?
- [ ] **Brand Tokens:** Are all colors conforming to `brands/<brand>.md` (e.g. Little Orange `#EA540F`, Navy `#060E1A`)?

### 2. Audio-Visual Synchronization
- [ ] Does the musical beat maintain tempo across transitions?
- [ ] Do SFX cues fire within $\pm 0.05\text{s}$ of their visual trigger (e.g., app ping precisely on phone reveal)?
- [ ] Is there any audio clipping, digital distortion, or abrupt pops at start or finish?

### 3. File & Metadata Verification
- [ ] Does the exported duration match the brief (e.g. $30\text{s} - 40\text{s}$)?
- [ ] Is the resolution accurate ($1080 \times 1920$ or $1920 \times 1080$)?
- [ ] Is the container format standard MP4 (`avc1` / `aac`) readable by QuickTime and browsers?

## Quality Gate Verdict Form
Every QA inspection must conclude with:
```text
VERDICT: [APPROVED | CHANGES REQUIRED | REJECTED]
Defects Found: [List with timestamps or "None"]
Remediation Steps: [Explicit instructions if changes required]
Signed By: QA Lead (Agency OS)
```
