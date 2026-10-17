# Standard: Video Production & Motion Graphics
**Category:** Production Standard  
**Governing Role:** The Technical Animator & Motion Engineer  
**Enforcement:** Mandatory for all video commercials, animated shorts, and kinetic graphics.

---

## 1. Frame Rate & Resolution Specifications

All agency video assets must conform to broadcast specifications:

| Video Type | Target Resolution | Aspect Ratio | Target Frame Rate | Minimum Duration | Maximum Duration |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Social Commercial (Reels/TikTok/Shorts)** | 1080 × 1920 | 9:16 (Vertical) | **60 FPS** | 15.0s | 45.0s |
| **Hero Brand Commercial (Web/YouTube/TV)** | 1920 × 1080 | 16:9 (Widescreen)| **60 FPS** | 30.0s | 90.0s |
| **Product Teaser / Feature Micro-Demo** | 1080 × 1080 | 1:1 (Square) | **60 FPS** | 10.0s | 30.0s |

---

## 2. Rendering Engine & Zero-Spend Pipeline

In adherence to host environment realities (`node` and `ffmpeg` are not installed in host PATH):

1. **Primary Execution Engine:** Google Chrome 150.0 Headless (`/Applications/Google Chrome.app/Contents/MacOS/Google Chrome`).
2. **Animation Stack:** HTML5 Canvas, WebGL, CSS 3D transforms, and requestAnimationFrame at synchronized 60 FPS.
3. **Encoding Pipeline:** Native `MediaRecorder` API with canvas stream capture (`canvas.captureStream(60)`), encoding directly to broadcast-compatible `video/mp4;codecs=avc1,mp4a.40.2`.
4. **Editor Integration:** CapCut macOS 9.5.0 draft automation via native JSON project construction (`draft_content.json`).

---

## 3. Kinetic Timing & Scene Rhythm

- **Shot Dwell Rhythm:** Average commercial shot duration must hold between **2.0s and 4.0s**. Shots under 1.2s cause cognitive fatigue; shots over 5.0s cause viewer drop-off.
- **Microsecond Precision:** Every scene cut, text entry, and graphic transition must be defined by exact frame index and millisecond timestamp in the storyboard.
- **Audio-Visual Lock:** Scene cuts, camera whip-pans, and kinetic text snaps must land precisely on audio accents (sub-bass hits, percussion transients, voiceover syllable endpoints).

---

## 4. UI Safe Zones & Mobile Overlay Avoidance

For 9:16 vertical video compositions:
- **Top Safe Margin:** Keep critical text and logos at least **150px (8%)** below the top edge (clears platform status bars and profile headers).
- **Bottom Safe Margin:** Keep primary CTAs and lower thirds at least **350px (18%)** above the bottom edge (clears username captions, sound title carousels, and search/comment bars).
- **Right Margin:** Keep text **120px (11%)** away from the right edge (clears like, comment, bookmark, and share icon stacks).

---

## 5. Web Audio Synthesis Standards

When generating zero-cost audio design without third-party sample packs:
- **Sub-Bass Impact:** Sine wave oscillator dropping from $120\text{Hz}$ to $38\text{Hz}$ over $0.4\text{s}$ with exponential gain decay.
- **Audio Risers (Tension Builders):** Sawtooth/Triangle sweep from $200\text{Hz}$ to $1,800\text{Hz}$ over $1.5\text{s}$ through a resonant low-pass filter ($Q=6$).
- **Kinetic Accent Clicks:** Bandpass-filtered white noise burst ($1,200\text{Hz}$ center) with $15\text{ms}$ envelope for UI microinteractions.
