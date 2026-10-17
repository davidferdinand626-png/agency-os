# Provider Setup

Use this reference when the user wants to run generation, not just plan prompts.

## Provider Discovery Checklist

Inspect the active environment for:

- MCP tools with names like `higgsfield`, `generate_image`, `generate_video`, `media_upload`, `models_explore`
- fal client code or SDK dependency
- env vars: `FAL_KEY`, `FAL_API_KEY`, `HIGGSFIELD_API_KEY`, `REPLICATE_API_TOKEN`, `RUNWAY_API_KEY`, provider-specific keys
- existing API routes wrapping generation providers
- local `.env.example` documenting supported providers

If none are available, ask the user which provider they want to configure. Ask them to place the key in a local env/secret store and tell you the variable name. Do not ask them to paste a production key into chat.

## Provider Capability Contract

The skill needs three capabilities:

```ts
type ImageGeneration = {
  generateImage(input: {
    prompt: string;
    aspectRatio: string;
    referenceIds?: string[];
    count?: number;
  }): Promise<{ id: string; url?: string; path?: string }[]>;
};

type RefToVideo = {
  generateVideo(input: {
    prompt: string;
    negativePrompt?: string;
    durationSec: number;
    aspectRatio: string;
    referenceIds: string[];
  }): Promise<{ id: string; url?: string; path?: string }>;
};

type MediaUpload = {
  uploadMedia(input: { pathOrUrl: string }): Promise<{ id: string }>;
};
```

## Higgsfield MCP Mode

If Higgsfield MCP tools are available, prefer them:

1. Upload user references with media upload.
2. Generate three direction hero frames with image generation.
3. Use the selected hero frame as the identity/style anchor.
4. Generate per-shot frames.
5. Generate per-shot videos with ref-to-video.
6. Capture every job/media ID.

Use provider model exploration tools when aspect ratio, duration, or media role constraints are unclear.

## fal Mode

If fal is available, map the pipeline to fal models:

- image generation: any configured image model suitable for graphic frames
- ref-to-video: Seedance 2.0 / Seedance 2.0 Pro / another configured i2v model
- optional text/image model: for storyboard sheets or style frames

The agent should not hard-code model IDs unless the project already uses them. Read the provider docs or local wrapper code when available.

If a project has no fal wrapper yet, create a small adapter that accepts the capability contract above and reads `FAL_KEY` from env.

## Manual Mode

Use manual mode when no provider is available or the user does not want to configure credentials. Output:

- three direction cards
- storyboard JSON
- image prompts
- video prompts
- negative prompts
- Remotion text overlay component
- edit assembly notes

Manual mode should be complete enough that the user can paste prompts into fal, Higgsfield, Runway, Kling, or another gen-media UI.

