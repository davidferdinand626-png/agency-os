# Workflow: Storyboard-to-Video Production Architecture
**Track:** Motion Graphics & Programmatic Video  
**Primary Agent:** The Creative Director & Motion Engineer  
**Supporting Skills:** `motion-graphics-director`, `remotion-best-practices`, `remotion-render`, `kinetic-typography`, `camera-choreography`, `anti-ai-slop-design`

---

## 1. Objective & Scope

Transform marketing strategy briefs and narrative arcs into broadcast-grade programmatic video commercials, social motion ads, and animated explainers. Rendered at **60 FPS** via zero-cost Google Chrome Headless Canvas/WebGL pipelines.

---

## 2. Step-by-Step Procedure

### Step 1: Creative Concepting & 3-Direction Storyboard
1. Load `motion-graphics-director` and `anti-ai-slop-design`.
2. Generate 3 distinct aesthetic directions for client alignment:
   - **Direction 1 (Minimalist Swiss / Editorial):** Deep monochrome background, generous negative space, crisp typography, subtle 2px line animations.
   - **Direction 2 (High-Energy Kinetic):** Staggered spring typography, directional whip-pans, rhythmic cut pacing aligned with rapid percussion.
   - **Direction 3 (Technical 3D & Parallax):** 3-plane depth simulation, device mockups, dynamic camera zooms, floating UI cards.
3. Select the approved direction and establish the global color tokens from `brands/<brand>.md`.

### Step 2: Microsecond-Precision Shot Mapping
1. Load `camera-choreography` and `kinetic-typography`.
2. Break down the entire video into discrete scenes (typically 4 to 7 scenes for a 30-45s video).
3. For every scene, specify:
   - **Scene Index & Title:** e.g. Scene 1: The Commuter Dilemma.
   - **Frame Range & Time:** e.g. Frames `0` to `360` (`0.0s` to `6.0s` @ 60 FPS).
   - **Camera Choreography:** Focal framing, zoom vector, and parallax speed multipliers.
   - **Kinetic Typography:** Stagger intervals, spring parameters (`mass: 0.8, stiffness: 180, damping: 14`), and visual hierarchy.
   - **Audio Design:** Exact frequency sweeps, risers, sub-bass impacts, and voiceover cues.
   - **Exit Transition:** Precise transition mechanic into the next scene.

### Step 3: Programmatic Canvas / WebGL Construction
1. Create a self-contained HTML5 composition file (`workflows/motion-graphics/<project>_composition.html`).
2. Implement 60 FPS `requestAnimationFrame` render loop with deterministic frame counting (`currentFrame / totalFrames`).
3. Wire the Web Audio API synthesis engine directly to frame triggers for zero-latency audio-visual synchronization.

### Step 4: Headless Video Recording & Verification
1. Run the headless Chrome recording pipeline:
   ```bash
   "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
     --headless=new \
     --disable-gpu \
     --use-fake-ui-for-media-stream \
     --autoplay-policy=no-user-gesture-required \
     "file:///absolute/path/to/composition.html"
   ```
2. Capture the rendered `.mp4` stream via `MediaRecorder` API.
3. Verify file size, frame rate, duration, and audio playback integrity.

---

## 3. Shot Specification Schema

```markdown
### Scene [N]: [Title] (Frames [Start] - [End] | [Duration]s)
- **Visual Subject:** [Detailed description of animated elements]
- **Camera Vector:** [e.g. Dolly In 1.00x -> 1.08x with quadratic easing]
- **Kinetic Copy:**
  - Headline: "[Text]" (Font: [Family], Size: [Px], Reveal: [Stagger Spring])
  - Subtext: "[Text]" (Opacity: 70%, Delay: +12 frames)
- **Audio Synthesis:**
  - Oscillator: Sawtooth sweep (220Hz -> 880Hz, Q=4)
  - Impact: Sub-bass 55Hz drop at Frame [X]
- **Exit Mechanics:** [Directional whip-pan right with 6-frame motion blur]
```
