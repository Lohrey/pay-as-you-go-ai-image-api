# Pay-As-You-Go AI Image API — No Monthly Fees

> **The simplest way to generate AI images via API.** One endpoint. Credits never expire. No subscription.

[![API Status](https://img.shields.io/badge/API-Live-brightgreen)](https://api.pau1.cloud)
[![Price](https://img.shields.io/badge/Price-from%20%240.20%2Fimage-blue)](https://api.pau1.cloud)
[![No Subscription](https://img.shields.io/badge/Subscription-None-orange)](https://api.pau1.cloud)

**👉 [Start generating at api.pau1.cloud](https://api.pau1.cloud)**

---

## Why Pay-As-You-Go?

Most AI image APIs force you into monthly subscriptions:
- **DALL-E 3:** Tied to OpenAI API credit system (can be expensive)
- **Stability AI:** Subscription tiers, credit expiry
- **Midjourney:** No API at all
- **Google Imagen:** Requires GCP setup, complex billing

With api.pau1.cloud — **buy credits once, use them whenever**. No monthly charge. Credits never expire.

## Pricing

| Credits | Price | Cost Per Image |
|---------|-------|----------------|
| 10 credits | **$4.99** | $0.50/image |
| 50 credits | **$14.99** | $0.30/image |
| 200 credits | **$39.99** | **$0.20/image** |

## Quick Start

```bash
# 1. Get credits at https://api.pau1.cloud
# 2. Make your first API call:

curl -X POST https://api.pau1.cloud/generate-image \
  -H "x-api-key: YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "prompt": "a futuristic city at night, cyberpunk style, ultra detailed",
    "style": "digital art",
    "aspect_ratio": "16:9",
    "output_format": "jpg"
  }'
```

**Response:**
```json
{
  "success": true,
  "image_url": "https://cdn.example.com/generated/abc123.jpg",
  "credits_remaining": 49,
  "generation_time_ms": 5200
}
```

## Python Example

```python
import requests

API_KEY = "your-api-key"
BASE_URL = "https://api.pau1.cloud"

def generate_image(prompt, style="photorealistic", aspect_ratio="1:1"):
    response = requests.post(
        f"{BASE_URL}/generate-image",
        headers={"x-api-key": API_KEY, "Content-Type": "application/json"},
        json={
            "prompt": prompt,
            "style": style,
            "aspect_ratio": aspect_ratio,
            "output_format": "jpg"
        }
    )
    return response.json()

# Generate an image
result = generate_image(
    prompt="a serene Japanese garden in autumn, photorealistic",
    style="photorealistic",
    aspect_ratio="16:9"
)
print(f"Image URL: {result['image_url']}")
print(f"Credits left: {result['credits_remaining']}")
```

## Node.js / JavaScript Example

```javascript
const generateImage = async (prompt, options = {}) => {
  const response = await fetch('https://api.pau1.cloud/generate-image', {
    method: 'POST',
    headers: {
      'x-api-key': process.env.IMAGE_API_KEY,
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      prompt,
      style: options.style || 'photorealistic',
      aspect_ratio: options.aspectRatio || '1:1',
      output_format: options.format || 'jpg'
    })
  });
  
  return response.json();
};

// Usage
const result = await generateImage('a happy golden retriever puppy', {
  style: 'photorealistic',
  aspectRatio: '4:3'
});
console.log('Image URL:', result.image_url);
```

## Supported Options

### Styles
- `photorealistic` — Hyper-realistic photographs
- `digital-art` — Digital artwork and illustrations  
- `illustration` — Flat/2D illustration style
- `anime` — Anime and manga style

### Aspect Ratios
- `1:1` — Square (Instagram posts, avatars)
- `16:9` — Widescreen (YouTube thumbnails, banners)
- `9:16` — Portrait (Instagram/TikTok stories)
- `4:3` — Standard (blog images, presentations)
- `3:4` — Portrait photos

### Output Formats
- `jpg` — JPEG (smaller file size)
- `png` — PNG (transparency support)

## Free Trial

**Test the API without an account:** [api.pau1.cloud → Try Demo](https://api.pau1.cloud)

1 free image per IP per day. No signup required. See what you're paying for before you buy.

## Why Developers Choose This

✅ **Simple pricing** — Know exactly what you're spending  
✅ **No commitment** — Buy exactly what you need  
✅ **Production-ready** — SSL, 99% uptime, fast response (5-10s)  
✅ **No vendor lock-in** — Standard HTTP, works with any language  
✅ **Credits never expire** — Use them at your own pace  

## Use Cases

- **Side projects** — Add AI image generation without ongoing costs
- **Prototyping** — Test concepts before committing to enterprise pricing
- **Content creation tools** — Social media image generators
- **E-commerce** — Product image variations
- **Chat apps** — On-demand image generation
- **Education platforms** — Illustrate concepts dynamically

## Rate Limits

- **Free demo:** 1 image per IP per 24 hours (no account needed)
- **Paid accounts:** Varies by plan (burst + sustained limits)
- **Enterprise:** Contact for custom limits

## Support

- **Docs & Pricing:** [api.pau1.cloud](https://api.pau1.cloud)
- **Issues:** Open a GitHub issue on this repo
- **Email:** Contact via the site

---

**Ready to start?** [Get credits at api.pau1.cloud](https://api.pau1.cloud) — first image is free.
