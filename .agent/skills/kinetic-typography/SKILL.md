---
name: kinetic-typography
description: Direct and implement broadcast-quality kinetic typography, text animation, spring easing curves, and audio-synchronized titles.
allowed-tools: Read, Glob, Grep
---

# Kinetic Typography & Motion Title Directing

> Elevate motion graphics through broadcast-quality kinetic typography, character-level spring physics, and frame-accurate audio synchronization.

---

## 🎯 When to Use This Skill

Use this skill whenever you need to:
- Script or animate high-impact text hooks, title cards, and lower thirds for video commercials.
- Implement physics-based spring animations (`mass`, `stiffness`, `damping`) for text reveals.
- Synchronize typography reveals with voiceover cadence or beat drops.
- Define HTML5 Canvas / CSS / Remotion typography animation code.

---

## 1. Core Kinetic Animation Techniques

### Technique 1: The Character/Word Stagger Spring
Instead of animating an entire sentence simultaneously as a static block, stagger each word by 2 to 4 frames (60-120ms):

```javascript
// Remotion / Vanilla JS Spring Simulation
function calculateSpringText(frame, wordIndex, fps = 60) {
  const delayFrames = wordIndex * 3; // 3-frame stagger per word
  const relativeFrame = Math.max(0, frame - delayFrames);
  
  // Spring parameters: mass=0.8, stiffness=180, damping=14 (punchy snap with minimal overshoot)
  const progress = Math.min(1, relativeFrame / (fps * 0.4));
  const easeOutBack = 1 + 2.7 * Math.pow(progress - 1, 3) + 1.7 * Math.pow(progress - 1, 2);
  
  return {
    opacity: Math.min(1, relativeFrame / 8),
    translateY: (1 - Math.min(1, easeOutBack)) * 40, // slides up 40px
    scale: 0.95 + 0.05 * Math.min(1, easeOutBack)
  };
}
```

### Technique 2: The Masked Headline Reveal
Text slides out from behind an invisible rectangular clipping mask (`overflow: hidden`):
- Creates a crisp, broadcast editorial appearance commonly seen in high-end automotive and luxury commercials.
- Slide direction matches visual momentum (e.g. text reveals from bottom to top as camera tilts upward).

### Technique 3: Word-by-Word Highlight & Audio Lock
- For fast-paced 9:16 vertical video (TikTok, Instagram Reels), keep active words highlighted in high-contrast accent yellow/gold (`#eab308` or `#10b981`), while upcoming words remain at 40% opacity (`#71717a`).
- Every highlighted word changes exactly on the spoken syllable boundary (150-250ms average duration).

---

## 2. Typographic Motion Hierarchy

| Screen Role | Target Duration | Entrance Animation | Dwell Time | Exit Animation |
| :--- | :---: | :--- | :---: | :--- |
| **Hero Hook Title** | 2.0s - 3.0s | Staggered slide-up + scale spring (0.4s) | 1.8s - 2.2s | Whip-blur or directional snap (0.2s) |
| **Metric Callout (e.g. +42%)** | 1.5s - 2.5s | Number counter tick-up + scale pulse | 1.2s | Fade out with subtle upward drift |
| **Lower Third Persona** | 3.5s - 4.5s | Clean horizontal rule wipe + text fade | 2.8s | Horizontal wipe reverse |
| **Final Call-to-Action (CTA)** | 3.0s - 5.0s | Centered elastic lockup + button glow | End of video | Holds until black fade |

---

## 3. Kinetic Typography Quality Checklist

- [ ] **Readability First:** Can an average viewer comfortably read the entire phrase twice during its dwell duration?
- [ ] **No Linear Easing:** Never use `linear` timing for text motion. Always use exponential ease-out or spring physics.
- [ ] **Focal Alignment:** Text placement does not collide with UI safe zones (keep vertical video text between 20% and 75% screen height).
- [ ] **Contrast Verification:** Text is legible over dynamic video backgrounds (use subtle backdrop scrims or text shadows if footage is varied).
