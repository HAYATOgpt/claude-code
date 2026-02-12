---
allowed-tools: Read, Glob, Grep, Write, Bash(git log:*), Bash(git diff:*), Bash(git status:*), Bash(git branch:*)
description: Generate a HANDOVER.md session handover document for the next Claude session
---

## Context

- Current branch: !`git branch --show-current`
- Git status: !`git status --short`
- Recent commits this session: !`git log --oneline -20`

## Your task

You are generating a **session handover document** — like a shift change briefing for the next Claude session. This ensures continuity across sessions and prevents "memory loss" between context windows.

Create a file called `HANDOVER.md` in the project root with the following structure:

```markdown
# Session Handover

**Date:** [current date]
**Branch:** [current branch]

## What Was Worked On

[List all tasks and features that were addressed in this session. Be specific about file paths and changes.]

## What Was Completed

[List everything that was fully finished and is working.]

## What's Still In Progress

[List anything that was started but not finished, with details on current state.]

## What Worked Well

[Approaches, patterns, or solutions that worked effectively.]

## What Didn't Work (Bugs & Fixes)

[Problems encountered, failed approaches, bugs found. Include how they were resolved or worked around. This is critical institutional knowledge.]

## Key Decisions & Rationale

[Important architectural or design decisions made during this session and WHY they were made. This context is often lost between sessions.]

## Lessons Learned & Gotchas

[Non-obvious things discovered: tricky configurations, undocumented behaviors, edge cases, things that look right but aren't. These save the next session from repeating mistakes.]

## Next Steps

[Clear, actionable items for the next session. Prioritize them. Be specific enough that the next Claude can pick up immediately.]

## Key Files Map

[List the most important files touched or referenced in this session, with a brief description of each file's role.]

| File | Purpose |
|------|---------|
| `path/to/file` | Description |
```

### Instructions

1. **Review the full session context** — Look at the conversation history, git log, git diff, and current state of the codebase to understand everything that happened in this session.
2. **Be thorough but concise** — Every section should have actionable content. Skip sections only if truly not applicable.
3. **Focus on what the NEXT session needs to know** — The goal is for the next Claude to read this and immediately have full context.
4. **Include specifics** — File paths, function names, error messages, command outputs. Vague handovers are useless.
5. **Write the HANDOVER.md** to the project root directory.
6. **After writing**, confirm to the user that the handover document has been created and give a brief summary of what's in it.
