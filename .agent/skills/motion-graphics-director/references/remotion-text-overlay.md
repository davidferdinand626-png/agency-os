# Remotion Text Overlay

Layer text after video unless the user explicitly wants baked-in text.

## Rules

- Animation must be deterministic from `useCurrentFrame()`.
- Do not use runtime randomness.
- Use masks, opacity, translate, scale, and slight blur sparingly.
- Keep text readable on mobile.
- Prefer word-by-word or line-by-line reveals.
- Use strong ease-out for entrances and clean fades/masks for exits.
- Keep text within safe zones for platform UI.

## Text Timeline

```json
[
  {
    "startSec": 0.2,
    "endSec": 2.2,
    "text": "Launch faster",
    "accentWord": "faster",
    "position": "center",
    "motion": "masked word reveal with staggered ease-out"
  }
]
```

## Component Pattern

```tsx
import React from 'react';
import { AbsoluteFill, interpolate, useCurrentFrame, useVideoConfig, Easing } from 'remotion';

type Cue = {
  startSec: number;
  endSec: number;
  text: string;
  accentWord?: string;
  position: 'top' | 'center' | 'bottom';
};

export function KineticTextOverlay({ cues }: { cues: Cue[] }) {
  const frame = useCurrentFrame();
  const { fps } = useVideoConfig();

  return (
    <AbsoluteFill style={{ pointerEvents: 'none' }}>
      {cues.map((cue, cueIndex) => {
        const start = cue.startSec * fps;
        const end = cue.endSec * fps;
        const enter = interpolate(frame, [start, start + 12], [0, 1], {
          extrapolateLeft: 'clamp',
          extrapolateRight: 'clamp',
          easing: Easing.out(Easing.cubic),
        });
        const exit = interpolate(frame, [end - 10, end], [1, 0], {
          extrapolateLeft: 'clamp',
          extrapolateRight: 'clamp',
        });
        const y = interpolate(enter, [0, 1], [18, 0]);
        const words = cue.text.split(' ');

        return (
          <div
            key={cueIndex}
            style={{
              position: 'absolute',
              left: '8%',
              right: '8%',
              top: cue.position === 'top' ? '12%' : cue.position === 'center' ? '42%' : '72%',
              opacity: enter * exit,
              transform: `translateY(${y}px)`,
              fontFamily: 'Inter, system-ui, sans-serif',
              fontWeight: 800,
              fontSize: 'clamp(42px, 8vw, 108px)',
              lineHeight: 0.92,
              color: 'white',
              textShadow: '0 8px 28px rgba(0,0,0,0.36)',
              textAlign: 'center',
            }}
          >
            {words.map((word, i) => (
              <span
                key={`${word}-${i}`}
                style={{
                  display: 'inline-block',
                  marginRight: '0.22em',
                  color: word === cue.accentWord ? '#7dd3fc' : 'white',
                  transform: `translateY(${interpolate(frame, [start + i * 2, start + i * 2 + 10], [16, 0], {
                    extrapolateLeft: 'clamp',
                    extrapolateRight: 'clamp',
                    easing: Easing.out(Easing.cubic),
                  })}px)`,
                }}
              >
                {word}
              </span>
            ))}
          </div>
        );
      })}
    </AbsoluteFill>
  );
}
```

