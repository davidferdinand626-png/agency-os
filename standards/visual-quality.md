# Standard: Visual Quality & Motion Graphics

---

## 1. Frame Rate, Motion Easing & Interpolation
- **Frame Rate:** 60 FPS standard for fluid motion graphics. 30 FPS permissible only when matching vintage aesthetic or constrained mobile environments.
- **Easing Curves:** Linear animation is strictly forbidden for hero objects and camera movement.
  - Entrances: `easeOutExpo` or `cubic-bezier(0.16, 1, 0.3, 1)`
  - Continuous movement / drift: `easeInOutSine`
  - Scale bounces / badges: `easeOutBack` with overshoot $\le 1.15$
  - Exits: `easeInCubic`

## 2. Typography & Readability
- **Hierarchy:** No more than 3 distinct font scales per frame (Hero Headline, Secondary Feature, Micro Label).
- **Legibility:** Minimum contrast ratio of 4.5:1 (WCAG AA compliant) against active backgrounds. Use subtle dark gradient plates or frosted glass cards behind text when overlaying moving video.
- **Reading Speed:** Text overlays must remain visible for at least $0.3\text{ seconds per word} + 1.0\text{ second buffer}$.

## 3. Negative Space & Composition Balance
- **Rule of Thirds & Safe Margins:** Respect mobile safe zones:
  - Top margin: 15% clear (for platform headers/notches).
  - Bottom margin: 20% clear (for platform caption UI, audio discs, and interaction buttons).
- **Emissive & Decorative Elements:** Emissive glowing lines, particles, and outlines must serve visual hierarchy (directing the eye to the hero subject), not act as visual noise.
