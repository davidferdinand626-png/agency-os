# Lesson Learned: Video Rendering & Pipeline Resilience on Constrained Environments

---

## Context & Finding
When working on macOS systems where standalone `ffmpeg`, `node`, or `npm` are not installed or where bundled ffmpeg binaries throw `SIGILL` due to architecture/instruction set mismatches (e.g. AVX2 compiled for newer architectures running on older Intel CPUs):

1. **Do not attempt repeated failing CLI binary calls:** A binary throwing illegal instruction will never succeed without recompilation.
2. **Google Chrome as a Zero-Cost Hardware-Accelerated Video Pipeline:**
   - Google Chrome Headless (`--headless=new --autoplay-policy=no-user-gesture-required --use-fake-ui-for-media-stream`) has built-in hardware acceleration for Canvas, WebGL, Web Audio, and `MediaRecorder`.
   - Chrome's native `MediaRecorder` supports `video/mp4;codecs=avc1,mp4a.40.2` directly.
   - A tiny local Python HTTP server can serve the HTML/assets and receive the recorded video stream chunked via POST to save the final `.mp4` file directly to disk with zero dropped frames.
3. **CapCut Draft JSON Architecture on macOS:**
   - CapCut drafts reside at `~/Movies/CapCut/User Data/Projects/com.lveditor.draft/<Project_Name>/`.
   - CapCut 9.5 uses `version: 360000` and `new_version: "187.0.0"`.
   - Timelines are measured in microseconds ($1\text{ second} = 1,000,000\text{ }\mu\text{s}$).
   - Registering a new project in `com.lveditor.draft/root_meta_info.json` makes it appear immediately on the CapCut user home screen.
