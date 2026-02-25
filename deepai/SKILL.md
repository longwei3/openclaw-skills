---
name: deepai
description: Generate images using DeepAI's free image generation API. Use when the user wants to create images from text prompts. Supports text-to-image generation with multiple models including standard HD, and various styles. No API key required for basic usage.
metadata:
  {
    "openclaw":
      {
        "emoji": "🎨",
        "homepage": "https://deepai.org",
        "requires": {},
      },
  }
---

# DeepAI Image Generation

Generate images using DeepAI's free image generation API. No API key required for basic usage.

## Usage

### Option 1: Web Interface (Easiest)

1. Visit https://deepai.org/machine-learning-model/text2img
2. Enter your text prompt
3. Click "Generate"
4. Download the generated image

### Option 2: Browser Automation

Use the browser tool to:
1. Navigate to https://deepai.org/machine-learning-model/text2img
2. Type prompt into the textbox
3. Click Generate button
4. Wait for image to generate
5. Click Download button

### Option 3: Direct API Call

Make HTTP requests directly to DeepAI's API:

```bash
# Using curl
curl -X POST "https://api.deepai.org/api/text2img" \
  -H "api-key: YOUR_API_KEY" \
  -F "text=your prompt here"
```

**Note:** Free tier has rate limits. For production use, consider getting an API key from https://deepai.org/api

## Supported Models

- **Standard/HD** — Default model, good quality
- **Genius** — Higher quality (requires DeepAI Pro)
- **Super Genius** — Ultra high resolution 2K (requires DeepAI Pro)

## Tips for Good Prompts

1. **Be specific** — Describe objects, lighting, mood, and style
2. **Use style keywords** — Add terms like "digital painting", "photorealistic", "cyberpunk"
3. **Include composition** — Mention camera angles, lighting, perspective
4. **Avoid ambiguity** — Clear descriptions produce better results

## Example Prompts

**Cyberpunk mascot:**
```
cute cartoon lobster mascot for pet game, round circular badge design, purple cyberpunk neon theme, friendly smile, big adorable eyes, holding a magic wand with sparkles, transparent background, app icon style
```

**Fantasy landscape:**
```
majestic floating castle in the clouds, golden sunset lighting, detailed fantasy art style, intricate architecture, dramatic sky with glowing clouds
```

**Product photography:**
```
modern wireless headphones on white background, professional product photography, soft lighting, clean minimalist style
```

## Legal Notes

- Generated images are considered public domain
- Commercial use is permitted
- You retain rights to your creations
