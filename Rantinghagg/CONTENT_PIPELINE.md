# RantingHagg Content Pipeline

## The Mission

Produce 10 years of content in 10 days. Autonomous, continuous, hysterical.

RantingHagg is not just a website — she's a **media empire in training**. Every piece of content feeds multiple outputs:

- Website rants
- Video scripts (TikTok, Reels, Shorts, YouTube)
- Social posts
- Merchandise
- Thumbnails & visual assets

---

## Pipeline Stages

```
RESEARCH → IDEA → RANT → SCRIPT → PROMPTS → ASSETS → MERCH → PUBLISHED
```

### Stage 1: RESEARCH 🔍
**What:** Find pain points, complaints, absurdities on Reddit, Twitter, forums
**Output:** Research notes in `RESEARCH/YYYY-MM-DD-topic.md`
**Triggers:** Heartbeat check, trending topics, user submissions

### Stage 2: IDEA 💡
**What:** Select topic, craft episode name, define the angle
**Output:** Episode entry in TASK_REGISTER.json
**Owner:** Creative director (you)

### Stage 3: RANT ✍️
**What:** Write the website article in Hagg's voice
**Output:** `EPISODES/XXX-episode-name/rant.md`
**Style:** Dry, British, observational, warm mockery

### Stage 4: SCRIPT 🎬
**What:** Convert rant to spoken video script (60-90 seconds)
**Output:** `EPISODES/XXX-episode-name/script.md`
**Format:** Exactly what Hagg says, with timing notes

### Stage 5: PROMPTS 🎨
**What:** Generate AI prompts for all visual/audio assets
**Output:** `EPISODES/XXX-episode-name/prompts.md`
**Includes:**
- Thumbnail prompt (for ComfyUI)
- Scene prompts (for video generation)
- Music/SFX prompts (for audio generation)

### Stage 6: ASSETS 🖼️
**What:** Generate images, thumbnails, video clips
**Owner:** You (ComfyUI)
**Output:** `ASSETS/XXX-episode-name/` folder
**Status:** Updated in TASK_REGISTER.json

### Stage 7: MERCH 👕
**What:** Extract quotable phrases, design merch concepts
**Output:** `MERCH/XXX-episode-name.md`
**Items:** Mugs, t-shirts, prints, stickers

### Stage 8: PUBLISHED 🚀
**What:** Deploy to website, schedule social posts
**Output:** Live URL, social posts scheduled
**Status:** TASK_REGISTER.json marked complete

---

## File Structure

```
Rantinghagg/
├── CONTENT_PIPELINE.md      # This file
├── TASK_REGISTER.json       # Master task tracker
├── PROMPTS.md               # Master prompt library
├── BRAND_GUIDE.md           # Voice, tone, visual identity
├── CONTENT_CALENDAR.md      # Planned topics
├── MONETIZATION.md          # Revenue strategies
├── SCRIPTS.md               # Script templates
│
├── RESEARCH/                # Research notes
│   ├── YYYY-MM-DD-topic.md
│   └── ...
│
├── EPISODES/                # Episode content
│   ├── 001-corporate-jargon/
│   │   ├── rant.md
│   │   ├── script.md
│   │   └── prompts.md
│   └── ...
│
├── MERCH/                   # Merchandise designs
│   └── ...
│
└── ASSETS/                  # Generated images, audio, video
    └── ...
```

---

## Heartbeat Schedule

**Every 10 minutes**, the agent checks:

1. **TASK_REGISTER.json** — What's next in the pipeline?
2. **RESEARCH/** — Any new pain points to explore?
3. **EPISODES/** — Any episodes ready for next stage?
4. **Social/Calendar** — Any scheduled posts due?

**Heartbeat actions:**
- Move tasks through pipeline
- Generate new content
- Update task status
- Alert when human input needed (e.g., ComfyUI generation)

---

## Task Register Format

Each episode tracked in `TASK_REGISTER.json`:

```json
{
  "id": "001",
  "episodeName": "The Corporate Jargon Death Loop",
  "topic": "corporate-jargon",
  "createdAt": "2026-03-26",
  "stages": {
    "research": { "status": "complete", "file": "RESEARCH/2026-03-26-corporate-jargon.md" },
    "idea": { "status": "complete", "approvedAt": "2026-03-26" },
    "rant": { "status": "complete", "file": "EPISODES/001-corporate-jargon/rant.md" },
    "script": { "status": "pending" },
    "prompts": { "status": "pending" },
    "assets": { "status": "pending", "note": "Awaiting ComfyUI generation" },
    "merch": { "status": "pending" },
    "published": { "status": "pending" }
  },
  "nextAction": "script",
  "priority": "high"
}
```

---

## Voice & Style Reference

**Hagg's Voice:**
- British, dry, observational
- Warm mockery, not cruel
- "I've seen it all" energy
- Tea always in hand
- Self-aware when she's being ridiculous

**Key Phrases:**
- "Right, so..."
- "Now explain this to me..."
- "We used to just..."
- "Meanwhile..."
- "That's not how that works, love."
- "Bless them."
- *[sips tea]*

**Visual Style:**
- YouTube thumbnail energy (bold, clickbaity)
- Exaggerated expressions
- Tea stains, reading glasses, cardigan
- Colours: Tea Cream (#F5E6D3), Burgundy (#8B2252), Cardigan Green (#4A6741)

---

## Automation Rules

1. **Never block the pipeline** — If one stage is waiting (e.g., ComfyUI), move to next episode
2. **Batch similar tasks** — Write multiple rants before generating prompts
3. **Update TASK_REGISTER.json after EVERY action** — Single source of truth
4. **Alert human only when necessary** — ComfyUI needs, approvals, decisions
5. **Prioritise by impact** — Viral potential > niche topics

---

*"Right then. Pipeline's set up. Now let's get to work."*
— The Hagg ☕
