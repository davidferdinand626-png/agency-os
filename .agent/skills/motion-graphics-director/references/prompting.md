# Prompting

AI video tools often drift photoreal. Lock every prompt into a 2D motion graphics register unless the user explicitly asks otherwise.

## 2D Register Locks

Use phrases like:

- flat 2D vector illustration
- designed graphic frame
- cel animation frame
- kinetic typography
- solid color fills
- posterized shading
- hard-edged shapes
- paper cut-out motion graphics
- riso print texture
- no photorealism
- no 3D rendering

Avoid:

- cinematic
- DSLR
- lens flare
- bokeh
- ray-traced
- volumetric lighting
- shallow depth of field
- realistic skin texture

## Image Prompt Structure

Use this order:

1. 2D register lock
2. designed frame / shot type
3. subject and locked descriptors
4. graphic environment
5. shading approach
6. palette
7. texture/medium
8. composition rule
9. aspect ratio

Example:

```txt
Flat 2D vector illustration, designed graphic frame, no photorealism and no 3D rendering. A geometric productivity app icon opens into three floating feature panels, clean rectangular shapes, simple hard-edged shadows. Set against an off-white graphic background with a subtle grid. Palette: ink black, soft white, electric blue accent, warm coral alert color. Clean vector edges, no grain. Center-weighted composition with room for kinetic headline text. Vertical 9:16 composition optimized for mobile.
```

## Ref-To-Video Prompt Structure

Write prose, not tag soup:

1. restate 2D register
2. identify reference frame and subject
3. action
4. layer/camera motion
5. easing
6. duration/pacing
7. continuity constraints

Example:

```txt
Animate this as flat 2D vector motion graphics, preserving the exact geometric app icon, feature panels, palette, and clean hard-edged shapes from the reference frame. The icon holds for a beat, then opens with a snappy anticipation-and-release scale pop. Three feature panels slide out one by one with staggered heavy ease-out and a small overshoot settle. Camera remains locked; motion comes from layered graphic elements only. Duration is 3 seconds, energetic but controlled, with clean vector edges and no texture drift.
```

## Negative Prompt

Use for every video generation:

```txt
photorealistic, 3D rendering, photograph, DSLR, lens flare, depth of field, shallow focus, bokeh, anamorphic, ray-traced, volumetric lighting, PBR materials, subsurface scattering, cinematic film look, realistic skin texture
```

