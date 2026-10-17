---
name: camera-choreography
description: Choreograph virtual 2D/3D camera movements, parallax depth layers, focal framing, and directional continuity across video scenes.
allowed-tools: Read, Glob, Grep
---

# Camera Choreography & Cinematic Movement Framework

> Direct virtual camera movement, multi-plane parallax depth, and spatial continuity to create cinematic visual momentum in digital video production.

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Script camera directions in video storyboards and shot lists.
- Implement 2D/3D camera transforms in WebGL, Canvas, CSS, or Remotion compositions.
- Design seamless match-cuts, whip-pans, and transition choreography.
- Structure multi-layer parallax scenes for product demos or animated commercials.

---

## 1. The 6 Cinematic Camera Moves

| Camera Move | Visual Psychological Effect | Optimal Implementation |
| :--- | :--- | :--- |
| **Push-In (Slow Dolly In)** | Increases dramatic tension, intimacy, or focus on a critical decision. | Camera scale increases from `1.0` to `1.08` over 3-4 seconds with quadratic ease-in-out. |
| **Pull-Back (Reveal Dolly Out)** | Reveals context, scale, scope, or isolation of the subject. | Camera pulls back from a tight macro detail to reveal the full environment or interface. |
| **Pedestal / Crane (Vertical Drift)** | Conveys prestige, elevation, or architectural grandeur. | Vertical Y-axis translation with subtle pitch tilt adjustment (`-2deg` to `+3deg`). |
| **Tracking / Lateral Truck** | Maintains momentum, urgency, and forward progression. | Horizontal X-axis translation locked parallel to subject motion. |
| **Orbit / Arc Rotation** | Highlights 3D form factor, premium materials, and product contours. | Camera orbits `15-30deg` around the center of mass in 3D perspective space. |
| **Whip-Pan / Snap Cut** | High-energy scene transition that bridges two disparate environments. | Rapid horizontal pan with simulated motion blur over `6-10 frames` (100-160ms). |

---

## 2. Multi-Plane Parallax Depth Architecture

To make 2D or pseudo-3D compositions feel deeply cinematic without heavy rendering engines, divide the scene into 3 distinct parallax planes:

```
[Camera Eye]
    │
    ▼
┌───────────────────────────────────────────────┐
│ Foreground (FG): Decorative bokeh, light      │  Speed: 1.4x (Fastest)
│ leaks, passing silhouettes. Blur: 4px         │
├───────────────────────────────────────────────┤
│ Midground (MG): Primary Hero Subject,         │  Speed: 1.0x (Baseline)
│ UI device frame, kinetic headline. Sharp.     │
├───────────────────────────────────────────────┤
│ Background (BG): Gradient canvas, city grid,  │  Speed: 0.25x (Slowest Drift)
│ ambient particle dust. Blur: 2px, Opacity: 40%│
└───────────────────────────────────────────────┘
```

### Parallax Coordinate Calculation:
$$\Delta X_{\text{FG}} = \text{Offset} \times 1.40, \quad \Delta X_{\text{MG}} = \text{Offset} \times 1.00, \quad \Delta X_{\text{BG}} = \text{Offset} \times 0.25$$

---

## 3. Directional Momentum & Match Cut Rules

1. **The 180-Degree Spatial Rule:** Establish a consistent vector of action. If a vehicle or workflow travels from Left to Right in Scene 1, Scene 2 must maintain left-to-right momentum. Flipping direction without an intermediate neutral shot disorients the viewer.
2. **Cut on Motion:** Execute cuts during peak camera velocity or subject movement. The human eye follows the momentum, making the scene transition feel completely invisible.
3. **Graphic Match Cut:** Align the final frame geometry of Shot A (e.g. circular app logo or coin) with the first frame geometry of Shot B (e.g. circular vehicle wheel or clock).

---

## 4. Camera Shot Specification Template

When authoring video shot plans in `workflows/motion-graphics/`:

```markdown
### Shot [N]: [Shot Title]
- **Duration:** [Start Frame] to [End Frame] ([Total Seconds]s @ 60 FPS)
- **Focal Framing:** [Macro Close-Up / Medium / Wide Establishing]
- **Camera Vector:** [e.g. Slow Dolly-In (1.00x -> 1.06x) + 5px upward Pedestal]
- **Subject Action:** [Describe subject animation]
- **Parallax Layers:**
  - Foreground: [Passing ambient particle streak, Speed: 1.5x]
  - Midground: [3D Smartphone displaying Little Ride corporate dispatch]
  - Background: [Dark Dar es Salaam topographic grid, Speed: 0.3x]
- **Exit Transition:** [Whip-pan right into Shot N+1]
```
