# Storyboard Schema

Use this schema for structured output. It can be adapted to any app or API.

```ts
type MotionStoryboardProject = {
  brief: string;
  aspectRatio: '9:16' | '16:9' | '1:1' | string;
  durationSec: number;
  platform?: string;
  feeling: string;
  selectedDirection?: number;
  directions: Direction[];
  shots: Shot[];
  textTimeline: TextCue[];
};

type Direction = {
  idx: number;
  name: string;
  role: 'safe' | 'bold' | 'experimental';
  pitch: string;
  visualRegister: string;
  palette: string[];
  typography: string;
  motionDNA: string;
  heroFramePrompt: string;
  generatedFrameId?: string;
};

type Shot = {
  idx: number;
  startSec: number;
  endSec: number;
  purpose: string;
  visual: string;
  layerMotion: string;
  transitionOut: string;
  imagePrompt?: string;
  frameId?: string;
  videoPrompt?: string;
  videoId?: string;
};

type TextCue = {
  startSec: number;
  endSec: number;
  text: string;
  accentWord?: string;
  position: 'top' | 'center' | 'bottom';
  motion: string;
};
```

## Direction Spread

The three directions should fill these roles:

- safe: brand-clean, readable, lower risk
- bold: editorial, high-contrast, visually assertive
- experimental: memorable, textural, unusual composition or motion

Do not make three minor variants of the same look.

