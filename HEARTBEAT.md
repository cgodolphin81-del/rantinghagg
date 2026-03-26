# HEARTBEAT.md — RantingHagg Content Pipeline

**Check interval:** Every 10 minutes

---

## Pipeline Checks (Rotate Through These)

### 1. TASK_REGISTER.json
- What's the next action in the queue?
- Move any episodes to the next stage?
- Update status after completed actions

### 2. RESEARCH/
- Check Reddit r/antiwork, r/technology, r/relationships for fresh pain points
- Scan Twitter trending topics
- Look for viral complaints, absurdities, contradictions
- Add new research notes: `RESEARCH/YYYY-MM-DD-topic.md`

### 3. EPISODES/
- Any episodes ready for script writing?
- Any scripts ready for prompt generation?
- Any prompts ready for asset generation (ComfyUI)?

### 4. Social/Calendar
- Any posts scheduled for today?
- Generate social captions from published rants

### 5. MERCH/
- Any new quotable phrases to add?
- Design concepts ready for review?

---

## Priority Order

1. **Script writing** (episodes 001, 002, 003 waiting)
2. **Prompt generation** (after scripts done)
3. **New research** (feed the pipeline)
4. **New rants** (from research)
5. **Merch extraction** (from completed scripts)

---

## When to Alert Human

- ComfyUI generation needed (you handle this)
- Episode approval required
- Merch designs ready for review
- Pipeline blocked (nothing to do)

---

## When to Stay Quiet (HEARTBEAT_OK)

- Pipeline flowing smoothly
- Waiting on human action
- Late night (23:00-08:00 UTC) unless urgent
- Nothing new since last check (<10 min)

---

*"Don't just sit there. Check the register. What's next?"*
— The Hagg ☕
