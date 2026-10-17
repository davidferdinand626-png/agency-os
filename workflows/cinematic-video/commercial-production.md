# Workflow: Cinematic Commercial Production Architecture
**Track:** Cinematic Video & Narrative Advertising  
**Primary Agent:** The Creative Director & Motion Engineer  
**Supporting Skills:** `emotional-arc-designer`, `camera-choreography`, `video-marketing`, `kinetic-typography`, `subtractive-design-mies`

---

## 1. Objective & Scope

Produce high-impact narrative commercials (15s, 30s, 60s) engineered for emotional resonance, viewer retention, and brand recall. Governed by classical 5-act narrative structures, cinematic camera choreography, and broadcast color grading.

---

## 2. The 5-Act Commercial Narrative Arc

Every cinematic commercial produced by Agency OS follows this emotional curve:

```
Tension Level
     ▲
 100 │                                [Act 3: Breakthrough / Climax]
  80 │                  [Act 2: Agitation]         /\
  60 │                         /\                 /  \
  40 │  [Act 1: Hook]         /  \               /    \   [Act 4: Evidence]
  20 │       /\              /    \             /      \        /\
   0 └───►──/──\────────────/──────\───────────/────────\──────/──\───[Act 5: CTA]───► Time
         0s    5s         5s      15s        15s       25s   25s  30s  30s       35s
```

### Act 1: The Pattern Interrupt (0.0s – 5.0s)
- **Goal:** Stop the scroll immediately. Shock, intrigue, or present an undeniable visceral reality.
- **Cinematic Style:** Tight macro close-up or unexpected visual scale. Kinetic headline snapping onto screen with immediate audio riser.

### Act 2: The Emotional Agitation (5.0s – 15.0s)
- **Goal:** Deepen identification with the problem. Amplify the daily frustration, friction, and hidden operational cost.
- **Cinematic Style:** Darker color palette, quickening cutting rhythm, rhythmic tension soundtrack, visual metaphors of disorder (traffic congestion, paper receipts piling up, ticking clocks).

### Act 3: The Breakthrough & Mechanism Reveal (15.0s – 25.0s)
- **Goal:** Introduce the client solution as the definitive hero. Show the unique mechanism that makes success effortless.
- **Cinematic Style:** Expansive camera reveal (push-in or crane shot), color palette shifts to clean illumination, signature brand accent colors flood the frame, triumphant musical shift.

### Act 4: The Empirical Proof & Transformation (25.0s – 30.0s)
- **Goal:** De-risk the decision with hard metrics, corporate trust badges, and tangible before-and-after contrast.
- **Cinematic Style:** Crisp UI demonstration, metric counters ticking upward, clean corporate logos, customer quotes.

### Act 5: The Frictionless Call-to-Action (30.0s – 35.0s)
- **Goal:** Drive immediate, unambiguous conversion with zero perceived friction.
- **Cinematic Style:** Brand logo lockup, primary offer code or web domain, risk-reversal micro-copy, clear voiceover directive.

---

## 3. Cinematic Color Grading & Atmosphere

To achieve a filmic look inside HTML5 Canvas/WebGL without commercial LUT plugins:
- **Canvas Filter Grading:**
  ```javascript
  ctx.filter = "contrast(1.08) saturate(1.05) brightness(0.98)";
  ```
- **Atmospheric Grain:** Overlay a dynamic, pseudo-random procedural noise canvas at 3-5% opacity to break digital color banding and simulate 35mm film stock.
- **Cinematic Aspect Ratio Letterboxing:** For 16:9 widescreen presentations, optional 2.39:1 Anamorphic black bars (`top: 0; height: 10%`) for theatrical authority.

---

## 4. Production Checkpoints & Review

Before releasing the commercial to the QA Inspector:
- [ ] Hook occurs within the first 1.8 seconds.
- [ ] Music riser peaks exactly as the core breakthrough mechanism appears (Act 3).
- [ ] Brand logo appears prominently in the final 5 seconds.
- [ ] Audio volume normalized to broadcast standard ($-14\text{ LUFS}$ target).
