# Standard: Visual Quality & Design Taste
**Category:** Creative Standard  
**Governing Role:** The Creative Director & The Quality Assurance Inspector  
**Enforcement:** Mandatory for all landing pages, graphic assets, video storyboards, and motion compositions.

---

## 1. Core Philosophy: Human Craft vs. AI Slop

Agency OS rejects generic AI aesthetics. Every visual artifact must demonstrate deliberate restraint, typographic maturity, disciplined spacing, and purposeful color application.

---

## 2. The Anti-AI-Slop Redlines (Strictly Prohibited Patterns)

Any creative deliverable containing the following patterns is subject to immediate rejection by the QA Inspector:

1. **Purple/Violet Neon Gradients:** The universal hallmark of unrefined AI SaaS design. Prohibited. Use neutral dark palettes (deep zinc `#09090b` or warm obsidian) paired with a singular brand accent.
2. **Over-Rounded Corners (`>12px`):** Giant pills and `rounded-3xl` corners create a toy-like appearance. Enforce crisp, mature radii: `4px` (`rounded-sm`), `6px` (`rounded-md`), or `8px` (`rounded-lg`).
3. **Floating Glassmorphic Blobs & Blurred Orbs:** Decorative fluff that serves no communication function. Strip all ungrounded floating background orbs.
4. **Low-Contrast Muted Gray Text:** Fails accessibility and strains readability. Primary text must maintain at least `90%` luminance contrast against dark backgrounds; secondary text must maintain `65-70%`. Never drop below a `4.5:1` contrast ratio.
5. **Generic 3D Glossy / Clay Icons:** Cluttered, juvenile, and unbranded. Use crisp, single-stroke monochrome line icons (Lucide / Heroicons) or authentic high-resolution photography.
6. **Colossal Fuzzy Drop Shadows:** Creates muddy layouts. Replace heavy shadows with subtle 1px hairline borders (`border border-zinc-800/80`) or clean 2px directional offsets.

---

## 3. Typographic Hierarchy & Scale Discipline

1. **Maximum 2 Font Families:**
   - **Display Face:** An expressive serif or technical grotesque for headlines (e.g. *Playfair Display*, *Geist*, *Inter Display*).
   - **Body Face:** A clean, highly legible sans-serif for body and UI micro-copy (e.g. *Inter*, *SF Pro Text*).
2. **Modular Proportional Scale:**
   - **Hero Display:** `48px` to `64px` | Line-height: `1.05` | Tracking: `-0.03em`
   - **Section H1/H2:** `32px` to `40px` | Line-height: `1.15` | Tracking: `-0.02em`
   - **Card / Subhead H3:** `20px` to `24px` | Line-height: `1.30` | Tracking: `-0.01em`
   - **Body Copy:** `15px` to `16px` | Line-height: `1.60` | Tracking: `0em`
   - **Meta / Micro-Label:** `11px` to `13px` | Line-height: `1.40` | Tracking: `+0.05em` (Uppercase)

---

## 4. The 8px Baseline Spacing Grid

All layout dimensions, margins, paddings, and flex/grid gaps must adhere to exact multiples of `8px` (or `4px` for tight micro-spacing):
- `4px`, `8px`, `16px`, `24px`, `32px`, `48px`, `64px`, `96px`, `128px`.
- Fractional or arbitrary margins (e.g. `13px`, `27px`) are strictly forbidden.

---

## 5. The 60-30-10 Color Architecture

- **60% Dominant Base:** Deep neutral canvas (`#09090b` dark or `#fafafa` light).
- **30% Structural Secondary:** Card surfaces (`#18181b`), divider hairlines (`#27272a`), muted text (`#a1a1aa`).
- **10% Brand Accent:** The signature brand color (e.g. Little Ride Amber `#f59e0b` or Stratiq Cyan `#06b6d4`). Reserved exclusively for primary CTAs, active status badges, and critical data callouts.

---

## 6. The Miesian Reduction Pass

Before submitting any visual asset for QA approval, execute the 4-step subtractive reduction protocol:
1. Strip unnecessary container boxes and borders; let negative space separate elements.
2. Delete decorative icons adjacent to clear text labels.
3. Prune copy by 30% while sharpening meaning.
4. Eliminate extraneous accent colors; consolidate into a disciplined palette.
