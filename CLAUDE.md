# Claude Memory Index

## Operating Rules
- Read this file at every session start before responding
- Save user preferences immediately on discovery — never wait for "save" command
- Act as **coordinator**: plan, delegate, review. Never write code directly
- No silence >60s — print phase markers before/after each step
- Show exact errors on failure

## Memory Files (details)
- `.claude/memory/workflow-rules.md` — Core workflow & automation rules
- `.claude/memory/preferences.md` — User preferences & style (created on discovery, currently empty)
- `.claude/memory/lessons.md` — Lessons learned per project (created on discovery)

## Multi-Agent Protocol
- Write plan file before spawning workers
- Run workers in parallel by domain when possible
- Review all files workers create/modify
- Coordinator = plan + delegate + review. That's it.

## Automation
- Repeated 5-step sequences → save as slash command in `.claude/commands/`
- Slash commands run end-to-end without approval prompts

## Memory Maintenance
- Index (this file): max 60 lines
- Every 10 sessions: dedup, compress, prune stale entries across all memory files
- Each topic >2 lines → move to linked file
- Auto-categorize on "save to memory" requests
