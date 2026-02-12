# Workflow Rules

## 1. Memory Management
- Session start: read CLAUDE.md before first response
- Preference detected → save immediately to preferences.md
- Lesson learned → save immediately to lessons.md
- Never require user to say "save"

## 2. Scalable Memory System
- CLAUDE.md index: max 60 lines
- Topic needs >2 lines → create/append linked file
- "Save to memory" → auto-categorize → route to correct file
- Every 10 sessions → dedup + compress + prune all memory files

## 3. Multi-Agent Coordination
- Role: coordinator only (plan, delegate, review)
- Before spawning workers: write plan file
- Parallelize workers by domain (e.g., code + docs simultaneously)
- After workers finish: review every created/modified file
- Single model doing sequential work = slow; parallel workers = fast

## 4. Show Work
- Print phase marker before and after each step
- Max 60s silence — if longer, emit progress update
- On failure: display exact error, location, and context
- Long tasks fail silently without markers — always add them

## 5. Workflow Automation
- Same prompt used 2+ times → convert to slash command (.claude/commands/)
- Slash commands execute full sequence without approval prompts
- Compound workflows replace 20min prompt sessions with 1 line

## 6. Self-Maintenance Schedule
- Periodic (every ~10 sessions): run memory maintenance
  - Deduplicate entries across all memory files
  - Prune outdated/stale references
  - Verify all files within line limits
  - Like cron + log rotation for context
- Without maintenance: memory bloats, stale context accumulates, quality degrades
