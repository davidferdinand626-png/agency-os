---
name: anti-ai-slop-design
description: Enforce human-grade design taste, typographic restraint, and layout rigor by eliminating clichéd AI aesthetics, neon gradients, and visual clutter.
allowed-tools: Read, Glob, Grep
---

# Anti-AI-Slop Design & Visual Taste Standards

> Banish generic AI aesthetics. Enforce mature, editorial-grade visual design rooted in typographic discipline, deliberate negative space, and functional restraint.

---

## 🎯 When to Use This Skill

Use this skill whenever you are:
- Designing or reviewing marketing websites, landing pages, banners, or motion graphics.
- Generating HTML/Canvas visual layouts or video storyboards.
- Reviewing UI components for brand alignment and professional credibility.
- Conducting a Creative Director quality gate review before client delivery.

---

## 1. The Anti-AI-Slop Redlines (Banned Patterns)

Reject and immediately remediate any creative artifact displaying these hallmarks of unrefined AI generation:

| Banned AI Slop Cliché | Why It Destroys Credibility | Mandatory Professional Replacement |
| :--- | :--- | :--- |
| **Purple/Indigo Neon Gradients** | Scream "cheap AI wrapper SaaS". | Neutral dark palette (e.g. rich zinc `#09090b` or warm stone `#0c0a09`) with a single, high-contrast brand accent color. |
| **Over-Rounded Corners (`rounded-3xl` / 24-32px)** | Makes interfaces feel childish and ungrounded. | Crisp, disciplined border radius: `4px` (`rounded-sm`), `6px` (`rounded-md`), or `8px` (`rounded-lg`) max. |
| **Floating Glassmorphic Blobs & Blurred Orbs** | Meaningless visual noise with zero communication value. | Intentional negative space and clean, unblurred background canvases. |
| **Low-Contrast Gray-on-Dark Text** | Unreadable; fails WCAG AA accessibility standards. | High-contrast hierarchy: Primary text at `95-100%` contrast (`#f4f4f5`), secondary text at `60-70%` (`#a1a1aa`). Never drop below `4.5:1` contrast ratio. |
| **Glossy 3D Isometric AI Icons** | Generic, distracting, and disconnected from brand reality. | Crisp, single-stroke monochrome iconography (Lucide, Heroicons) or authentic high-resolution photography. |
| **Pointless Drop Shadows (`shadow-2xl` colored)** | Creates visual mud and obscures layout boundaries. | Subtle, single-pixel hairline borders (`border border-zinc-800`) or crisp, directional 2px shadows. |

---

## 2. Core Pillars of Professional Design Taste

### Pillar 1: Typographic Discipline & Modular Scales
- **Font Pairing:** Use maximum 2 typefaces: one expressive, characterful serif or technical grotesk display face for headlines, paired with a rock-solid, highly legible sans-serif for body (e.g., *Inter*, *Geist*, *SF Pro*, *Playfair Display*).
- **Scale:** Adhere strictly to a proportional type scale (Major Third 1.25x or Perfect Fourth 1.333x):
  - Hero Display: `48px` - `64px` (Letter-spacing: `-0.03em`)
  - Section H1/H2: `32px` - `40px` (Letter-spacing: `-0.02em`)
  - Subhead H3: `20px` - `24px` (Letter-spacing: `-0.01em`)
  - Body Text: `15px` - `16px` (Line-height: `1.6`, Letter-spacing: `0`)
  - Micro-copy / Meta: `12px` - `13px` (Uppercase tracking: `+0.05em`)

### Pillar 2: The 8px Baseline Spacing Grid
- Every margin, padding, gap, and dimension must be an exact multiple of `8px` (or `4px` for tight micro-spacing):
  - `4px`, `8px`, `16px`, `24px`, `32px`, `48px`, `64px`, `96px`, `128px`.
- Avoid arbitrary values like `17px`, `23px`, or `53px`. Grid consistency creates subconscious visual harmony.

### Pillar 3: Purposeful Color Hierarchy (60-30-10 Rule)
- **60% Dominant Base:** Clean background (Neutral dark or crisp light).
- **30% Structural Secondary:** Card backgrounds, hairline borders, body typography, subtle hover states.
- **10% High-Voltage Accent:** Reserved strictly for primary CTAs, active status indicators, and key metric callouts.

---

## 3. Creative Director Review Rubric

Score every visual deliverable before delivery:
- [ ] **Contrast:** Every text element passes WCAG AA (`\ge 4.5:1` ratio).
- [ ] **Restraint:** No neon gradients or pointless background blobs.
- [ ] **Alignment:** Every element snaps to the 8px grid.
- [ ] **Hierarchy:** Eye naturally travels: 1. Headline -> 2. Key Graphic/Proof -> 3. Action CTA.
- [ ] **Whitespace:** At least 40% of the canvas consists of clean, breathing negative space.
