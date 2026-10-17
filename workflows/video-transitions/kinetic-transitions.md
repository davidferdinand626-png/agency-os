# Workflow: Kinetic Video Transitions & Visual Rhythm
**Track:** Video Transitions & Motion Design  
**Primary Agent:** The Technical Animator & Motion Engineer  
**Supporting Skills:** `motion-graphics-director`, `camera-choreography`, `remotion-best-practices`

---

## 1. Objective & Scope

Maintain relentless visual momentum and seamless spatial continuity across video scenes using a catalog of mathematical, physics-based transition mechanics.

---

## 2. Core Transition Catalog & Easing Mathematics

Every transition must complete within **6 to 18 frames** (100ms – 300ms @ 60 FPS). Transitions exceeding 20 frames drag pacing and reveal technical seams.

### Transition 1: The Directional Whip-Pan
- **Mechanics:** Camera accelerates horizontally along the X-axis (`-100%` to `+100%`) over 8 frames with simulated directional motion blur.
- **Easing Formula:**
  $$\text{Progress}(t) = \begin{cases} 4t^3 & \text{if } t < 0.5 \\ 1 - \frac{(-2t + 2)^3}{2} & \text{if } t \ge 0.5 \end{cases}$$
- **Sound FX Lock:** High-frequency filtered noise whoosh ($800\text{Hz} \to 2400\text{Hz} \to 400\text{Hz}$) peaking on Frame 4.

### Transition 2: The Geometric Match Cut
- **Mechanics:** The visual centroid of an element in Scene A (e.g., circular app icon) aligns perfectly in screen coordinates with an element in Scene B (e.g., spinning car wheel).
- **Scale Morph:** Rapid scale-pulse (`1.00 \to 1.15 \to 1.00`) on the exact cut frame to bridge the cut.
- **Sound FX Lock:** Crisp mechanical click or sub-bass snap ($60\text{Hz}$).

### Transition 3: The Camera Zoom-Through (Dolly Warp)
- **Mechanics:** The camera accelerates forward exponentially into a focal opening (e.g. an O in a headline, a smartphone screen, or a car window), scaling Scene A to $400\%$ while fading in Scene B from within the focal center.
- **Scale Math:**
  $$\text{Scale}(t) = 1.0 + 3.0 \times t^4$$
- **Sound FX Lock:** Sub-bass riser dropping into a clean impact transient.

### Transition 4: The Hairline Wipe (Miesian Sweep)
- **Mechanics:** A razor-sharp 1px brand accent hairline (`#f59e0b` or `#06b6d4`) sweeps across the canvas from left to right, revealing the subsequent scene via CSS `clip-path: inset(...)`.
- **Dwell:** 10 frames (166ms). Clean, architectural, and uncluttered.

---

## 3. Spatial Continuity Rules

1. **Vector Preservation:** If Scene 1 exits to the right, Scene 2 must enter from the left. Inverting transition vectors between adjacent scenes creates visual jarring.
2. **Subject Eye-Trace:** Position the primary focal point of Scene 2 within 15% screen distance of where the viewer's eye finished in Scene 1.
3. **Never Cut on Stillness:** Always initiate a transition while an element is already moving. Motion hides the cut; stillness exposes it.
