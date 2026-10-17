# Agency OS — Autonomous Marketing & Motion Graphics System
**Google Antigravity Production Framework**

---

## 1. System Mission & Scope
Agency OS is a persistent, reusable operating system configured inside Google Antigravity. It enables autonomous, high-end execution across five core disciplines:

1. **Cinematic Video Production & Motion Graphics:** Storyboard direction, scene timing, shot maps, kinetic typography, and broadcast-grade rendering.
2. **2D/3D Animation & Product Visualization:** Physics-based pacing, microinteractions, easing curves, lighting direction, and multimodal transitions.
3. **Marketing Research & Strategic Planning:** TAM/SAM/SOM analysis, competitor teardowns, audience segmentation, campaign roadmaps, and influencer marketing frameworks.
4. **Multi-Agent Coordination & Independent QA:** Structured handoffs between strategic, creative, and technical roles, accompanied by frame-by-frame visual inspection.
5. **Zero-Budget Resilience:** 100% operational on local, free, and open-source capabilities without requiring paid API credits, subscription lock-in, or proprietary cloud render farms.

---

## 2. Directory Architecture

```text
agency-os/
├── README.md                           # System overview, quickstart & tool status
├── AGENTS.md                           # Global persistent operating instructions for Antigravity
├── .agent/
│   ├── skills/                         # Reusable specialist skills (local repository discovery)
│   ├── workflows/                      # Pre-configured multi-step marketing workflows
│   ├── agents/                         # Persona definitions (Strategist, Creative Director, QA)
│   └── rules/                          # System guardrails and output constraints
├── workflows/                          # Human-readable production workflows
│   ├── research/                       # Market research & competitive intelligence
│   ├── marketing-strategy/             # Campaign launches, funnels & growth loops
│   ├── motion-graphics/                # Storyboard-to-video & Remotion kinetic design
│   ├── cinematic-video/                # Commercial advertising & narrative pacing
│   ├── video-transitions/              # Transition library, easing curves & visual rhythm
│   └── quality-assurance/              # Frame-by-frame verification & QA checklists
├── standards/                          # Non-negotiable quality and compliance standards
│   ├── research-integrity.md           # Research methodologies & data verification
│   ├── visual-quality.md               # Motion design standards, color & negative space
│   ├── video-production.md             # Codecs, framerates, canvas ratios & audio sync
│   └── brand-consistency.md            # Brand token preservation & visual hierarchy
├── brands/                             # Client and brand profiles
│   ├── little-ride-tz.md               # Little Ride Tanzania mobility profile & tokens
│   └── stratiq.md                      # Stratiq enterprise intelligence profile
├── project-logs/                       # Immutable production trajectory records
└── lessons-learned/                    # Technical takeaways, constraints & workarounds
```

---

## 3. Installed Core Skills

| Skill | Source | Primary Purpose | Execution Mode |
| :--- | :--- | :--- | :--- |
| **`motion-graphics-director`** | `RazorNub` | Storyboard direction, shot mapping, Remotion overlays | Local / Prompt-Only / Free |
| **`remotion-best-practices`** | `remotion-dev` | React programmatic video architectures | Local Code / Node (when installed) |
| **`remotion-render`** | `remotion-dev` | CLI render pipelines, frame extraction | Local CLI / Headless Canvas |
| **`video-marketing`** | `nguyenphp` | Hook construction, viewer retention, platform sizing | Local Strategy |
| **`launch-strategy`** | `nguyenphp` | Go-to-market roadmaps, budget allocation | Local Strategy |
| **`influencer-marketing`** | `nguyenphp` | Creator outreach, tiering, contract deliverables | Local Strategy |
| **`competitor-teardown`** | `nguyenphp` | Competitive positioning & feature gap matrices | Local Research |
| **`crossframe-review`** | `e-motionlabs` | Visual inspection, typography contrast, defect audit | Local QA |
| **`emotional-arc-designer`** | `e-motionlabs` | Cinematic narrative tension, pacing, and release | Local Creative |
| **`market-sizing-analysis`** | `e-motionlabs` | Quantitative TAM/SAM/SOM financial models | Local Analytics |

---

## 4. Operational Pipeline (The 7-Step Agency Loop)

Every assignment handled by Agency OS executes through seven deliberate phases:

1. **Intake & Brand Context:** Read brand profile from `brands/<brand>.md` and define format requirements.
2. **Research & Intelligence:** Gather verifiable data, competitor positioning, and user pain points.
3. **Strategic Blueprint:** Structure the narrative arc, campaign angle, budget breakdown, and distribution plan.
4. **Creative Direction & Storyboarding:** Produce 3 distinct visual directions with shot plans and kinetic copy.
5. **Production & Assembly:** Construct compositions (Canvas, Three.js, CapCut, or Remotion) with audio design.
6. **Crossframe QA & Inspection:** Audit frames for contrast, brand fidelity, pacing, and mechanical glitches.
7. **Delivery & Institutional Memory:** Save final assets, record in `project-logs/`, and document lessons in `lessons-learned/`.

---

## 5. Tooling & Environment Status

- **Host OS:** macOS (Darwin Kernel Version 21.6.0 x86_64)
- **Git Version:** 2.37.1
- **Python Version:** Python 3.9.6
- **Headless Browser Engine:** Google Chrome 150.0 (Canvas 60 FPS, WebGL, Web Audio, MediaRecorder MP4)
- **External Video Editors:** CapCut macOS 9.5.0 (`~/Movies/CapCut/User Data/Projects/com.lveditor.draft/`)
