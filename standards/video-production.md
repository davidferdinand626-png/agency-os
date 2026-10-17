# Standard: Video Production & Rendering Pipelines

---

## 1. Canvas Dimensions & Aspect Ratios
- **Vertical Master (9:16):** $1080 \times 1920$ pixels (Optimized for TikTok, Instagram Reels, YouTube Shorts).
- **Widescreen Master (16:9):** $1920 \times 1080$ pixels (Hero web headers, YouTube full-length, broadcast TV).
- **Square / Feed (1:1):** $1080 \times 1080$ pixels (Instagram & Facebook in-feed).

## 2. Rendering Engines & Local Capabilities
- **Browser-Based Automated Engine (Chrome Headless):**
  - Uses HTML5 Canvas + Web Audio API + MediaRecorder.
  - Video Codecs: `video/mp4;codecs=avc1,mp4a.40.2` (preferred) or `video/webm;codecs=vp9,opus`.
  - Bitrate: 8.0 Mbps to 12.0 Mbps.
- **Native Timeline Engine (CapCut Draft Exporter):**
  - Schema: CapCut macOS 9.5+ conforming (`version: 360000`, microsecond time units).
  - Multi-track timeline (Video plates, overlays, kinetic titles, audio channels).

## 3. Audio Engineering & Synchrony
- **Audio Sample Rate:** 44.1 kHz or 48.0 kHz.
- **Dynamic Range:** Master output normalized to $-14\text{ LUFS}$ to $-16\text{ LUFS}$ with true peak below $-1.0\text{ dBTP}$.
- **Sound Design Layers:**
  1. Musical Bed / Beat: Continuous rhythmic drive (e.g. 122 BPM Afro-tech).
  2. Environmental Foley: Subtle real-world atmosphere (city ambiance, engine revs).
  3. UI & Interaction Audio: Crisp high-frequency pings, confirmation dings, button clicks.
  4. Brand Sonic Mnemonic: Two-tone or three-tone distinct sonic logo on closing card.
