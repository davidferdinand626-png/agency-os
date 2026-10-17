# Agency OS — Autonomous Marketing & Motion Graphics System
**Google Antigravity Production Framework**  
**Authoritative Repository:** `https://github.com/davidferdinand626-png/agency-os`

---

## 1. System Mission & Scope

Agency OS is a persistent, reusable operating system configured inside Google Antigravity. It enables autonomous, high-end execution across five core disciplines:

1. **Cinematic Video Production & Motion Graphics:** Storyboard direction, scene timing, shot maps, kinetic typography, and broadcast-grade rendering at 60 FPS.
2. **Realistic 2D/3D Animation & Product Visualization:** Physics-based pacing, microinteractions, spring easing curves, lighting direction, and camera choreography.
3. **Marketing Research & Strategic Planning:** TAM/SAM/SOM analysis, competitor teardowns, audience segmentation, campaign roadmaps, conversion rate optimization, and influencer marketing frameworks.
4. **Multi-Agent Coordination & Independent QA:** Structured handoffs between strategic, creative, and technical roles, accompanied by frame-by-frame visual inspection and anti-slop standards.
5. **Zero-Budget Resilience & Host Safeguards:** 100% operational on local, free, and open-source capabilities without requiring paid API credits, subscription lock-in, or proprietary cloud render farms. Strictly respects the host's 16GB free disk limit.

---

## 2. Directory Architecture

```text
agency-os/
├── README.md                           # System overview, quickstart & tool status
├── AGENTS.md                           # Global persistent operating instructions for Antigravity
├── .agent/
│   └── skills/                         # 23 Modular specialist skills (Anthropic/Antigravity standard)
├── research/                           # Research deliverables & candidate audits
│   ├── github-repository-register.md   # Systematic audit of 50 open-source repositories
│   ├── approved-sources.md             # Tiered adoption roadmap & structural patterns
│   └── raw_github_data.json            # Live GitHub API metadata for all 50 candidates
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

## 3. Installed Skills Catalog (23 Modular Capabilities)

Every skill follows the official Anthropic/Antigravity `SKILL.md` packaging standard with YAML frontmatter, step-by-step procedures, and verification rubrics:

| Category | Skill Name | Primary Capability Delivered | Source / Inspiration |
| :--- | :--- | :--- | :--- |
| **Strategy & Research** | `competitor-teardown` | Competitive positioning, UX/ad audits, and gap matrices | `coreyhaines31` / `nguyenphp` |
| | `market-sizing-analysis` | Top-down & bottom-up TAM/SAM/SOM financial models | `e-motionlabs` |
| | `customer-journey-mapping`| 5-stage lifecycle touchpoints, trigger events, and friction audits | `coreyhaines31/marketingskills` |
| | `growth-experimentation` | Scientific hypothesis formulation, ICE scoring, and growth loops | `coreyhaines31/marketingskills` |
| | `launch-strategy` | Go-to-market orchestrations, phased channel rollout | `nguyenphp/antigravity-marketing` |
| | `influencer-marketing` | Creator discovery, tiering, outreach, and brief management | `nguyenphp/antigravity-marketing` |
| **Search & SEO** | `technical-seo-audit` | Crawling, indexability, canonicalization, Core Web Vitals | `AgriciDaniel/claude-seo` |
| | `schema-markup-generator` | Valid JSON-LD structured data for Rich Results | `AgriciDaniel/claude-seo` |
| | `geo-aeo-optimization` | Optimization for Perplexity, ChatGPT, Claude, and `llms.txt` | `AgriciDaniel/claude-seo` |
| **Creative & Copy** | `copywriting-frameworks` | PAS, AIDA, BAB, 4 U's headline formulas, CTA psychology | `coreyhaines31/marketingskills` |
| | `anti-ai-slop-design` | Eliminating purple neon gradients, generic icons, and clutter | `madebymustafa/design-taste` |
| | `subtractive-design-mies`| The Miesian reduction pass: stripping non-essential visual noise | `deeflect/mies` |
| | `emotional-arc-designer` | Narrative tension, pacing, and emotional resonance | `e-motionlabs` |
| | `social-distribution-engine`| Platform-native posts for LinkedIn, X/Twitter, and TikTok | `kostja94/marketing-skills` |
| | `email-marketing-sequences`| B2B cold outbound, inbound nurture, and onboarding sequences | `kostja94/marketing-skills` |
| **Motion & Video** | `motion-graphics-director`| Shot mapping, timing breakdown, camera angles | `RazorNub` |
| | `remotion-best-practices`| Programmatic video composition architectures | `remotion-dev/skills` |
| | `remotion-render` | Headless render pipelines and frame extraction | `remotion-dev/skills` |
| | `kinetic-typography` | Spring physics text reveals, staggered typography, audio sync | `remotion-dev/skills` |
| | `camera-choreography` | 2D/3D camera moves, parallax multi-plane depth, match cuts | `remotion-dev/skills` |
| | `video-marketing` | Retention hooks, safe zones, aspect ratio standards | `nguyenphp/antigravity-marketing` |
| **Quality Assurance** | `crossframe-review` | Frame-by-frame visual inspection, contrast, defect audit | `e-motionlabs` / `Dragoon0x` |
| | `conversion-rate-optimization`| LIFT model heuristic audits, form friction reduction | `coreyhaines31/marketingskills` |

---

## 4. Multi-Agent Coordination Protocol

Assignments execute through five specialized roles operating under strict handoff contracts:

```
[1. Strategy Director]  ───> Brief & ICP Journey Map ───>  [2. Creative Director]
                                                                  │
                                                           Storyboard & Copy
                                                                  │
                                                                  ▼
[4. QA Inspector]       <─── Rendered Composition ◄───  [3. Motion Engineer]
       │
   [VERDICT]
   ├── APPROVED ────────>  [5. Production Archivist] ───>  Delivery & Git Push
   └── REJECTED ────────>  Route back to Step 2 or 3 for immediate remediation
```

---

## 5. Host Tooling & Execution Engine Status

- **Host Operating System:** macOS (Darwin Kernel Version 21.6.0 x86_64, Intel Core i5, 8GB RAM)
- **Available Disk Space:** **~16 GB** (Diffusion weights and heavy Docker containers strictly prohibited)
- **Git Version:** 2.37.1
- **Python Version:** Python 3.9.6
- **Headless Video Engine:** Google Chrome 150.0 (Canvas 60 FPS, WebGL, Web Audio synthesis, native `video/mp4` export)
- **External Video Editors:** CapCut macOS 9.5.0 (`~/Movies/CapCut/User Data/Projects/com.lveditor.draft/`)
