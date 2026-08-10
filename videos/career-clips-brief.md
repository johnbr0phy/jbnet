# Career video clips — Imagine prompts

Use these on **[grok.com/imagine](https://grok.com/imagine)** with your headshot (the cream sweater arms-crossed portrait).

Elon’s note (Aug 2026): Imagine Video 1.5 now supports **image + voice references**, text-to-video, and native 1080p.

---

## Voice clone (your voice, not a generic TTS voice)

1. Open [grok.com/imagine](https://grok.com/imagine)
2. Start a video with your photo as the **image reference**
3. Attach a **voice / audio reference** (short clean sample of *you* speaking)
   - 15–60s of natural speech, quiet room, no music
   - Read something neutral (or one of the scripts below)
4. Paste a clip prompt from below
5. Prefer **10s** or **15s** if the UI offers it; API in Grok Build is 6s/10s only

**Tip:** One good voice sample reused across all clips keeps the voice consistent.

---

## Scripts (spoken copy)

Rough timing: ~2.5 words/sec for natural talk. 10s ≈ 25 words; 15s ≈ 35–40 words.

### Clip 1 — Who I am (~10s)

> I'm John Brophy — builder and product leader. I went from design-led PM to shipping code myself with AI. Idea in the morning, live by lunch.

### Clip 1b — Who I am (~15s)

> I'm John Brophy — builder and product leader. For years I was a design-led PM who needed a team to build. Since late 2025 I ship myself with AI: idea in the morning, live by lunch. It's everything I dreamed this job could be.

### Clip 2 — Career arc (~10s)

> I joined Spotify early, then led product at Hearst, Whalar, and now Stensul. Two decades building products people actually use.

### Clip 2b — Career arc (~15s)

> I joined Spotify as employee two-hundred-something, rebuilt premium and sign-up flows that reached millions. Then product leadership at Hearst, Whalar, and Stensul — always closer to the build.

### Clip 3 — What I'm good at (~10s)

> What I'm good at is connecting vision to shipping. AI product strategy, agentic workflows, and hands-on building — design, code, and PM all at once.

### Clip 3b — What I'm good at (~15s)

> I'm good at connecting vision to shipping. AI product strategy, agentic workflows, customer discovery, and GTM. Design-led, data-driven, and now fully hands-on with the tools that write the code.

### Clip 4 — Builder identity (~10s)

> Scrappy and hands-on: I design, code, and PM in the same day. Shipping daily, sometimes hourly. Have an idea in the morning, get it live by lunch.

### Clip 5 — Proof / side projects (~15s)

> On nights and weekends I ship real products with AI: TigerTest has nearly ten thousand users and hundreds of thousands of practice questions answered. LLM-Wiki runs my job knowledge base. I build to learn.

---

## Imagine prompts (paste with photo)

Use a **front-facing portrait**, mouth visible, arms-crossed pose is fine. Keep dialogue in quotes so lip-sync has a clear target.

### Prompt — Clip 1

```
Medium close-up talking-head of the man in the photo. He speaks directly to camera with natural lip-sync, slight head nods, warm confident expression, soft studio light, subtle natural motion only. He says: "I'm John Brophy — builder and product leader. I went from design-led PM to shipping code myself with AI. Idea in the morning, live by lunch."
```

### Prompt — Clip 2

```
Medium close-up talking-head of the man in the photo. He speaks to camera with clear lip-sync, calm professional energy, arms still crossed, minimal camera drift. He says: "I joined Spotify early, then led product at Hearst, Whalar, and now Stensul. Two decades building products people actually use."
```

### Prompt — Clip 3

```
Medium close-up talking-head of the man in the photo. He speaks directly to camera with natural lip-sync and a slight smile, confident and approachable. He says: "What I'm good at is connecting vision to shipping. AI product strategy, agentic workflows, and hands-on building — design, code, and PM all at once."
```

### Prompt — Clip 4

```
Medium close-up talking-head of the man in the photo. Animated but controlled delivery, natural blinks and small nods, lip-synced speech. He says: "Scrappy and hands-on: I design, code, and PM in the same day. Shipping daily, sometimes hourly. Have an idea in the morning, get it live by lunch."
```

### Prompt — Clip 5

```
Medium close-up talking-head of the man in the photo. Friendly, proud tone, natural lip-sync, soft gray studio background. He says: "On nights and weekends I ship real products with AI: TigerTest has nearly ten thousand users. LLM-Wiki runs my job knowledge base. I build to learn."
```

---

## Drop-in for johnbrophy.net

When clips are ready, put files here:

```
videos/
  career-who-i-am.mp4
  career-arc.mp4
  career-skills.mp4
  career-builder.mp4
```

Then ask Grok Build (or Claude) to embed them on the resume hero / intro section of `index.html` (or `v2/`).

---

## What failed in Grok Build CLI (for context)

- `image_to_video` in this environment returned: **Zero Data Retention teams must provide output.upload_url** — so generated video can’t land here without that plumbing.
- Duration in Build tools is **6s or 10s only** (not 15s). Use grok.com/imagine for longer if offered.
- **Voice reference upload is not exposed** as a parameter in the Build video tools yet — use the Imagine UI for true voice clone.
