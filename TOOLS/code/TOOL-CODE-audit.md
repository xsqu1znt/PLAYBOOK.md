# TOOL-CODE-audit.md

```
TOOL: Code Audit
GROUP: code
USE FOR: Getting a clear-eyed read of existing code before refactoring, handing off, or continuing development
PAIRS WITH: SKILL-refactor.md (for acting on the audit), any SYSTEM.md
```

---

## What This Tool Does

When uploaded to a session, this tool instructs the AI to produce a structured audit of the provided code. No changes are made. No fixes are applied. The output is a honest, opinionated assessment of the current state — what's solid, what's fragile, what's missing, and what should be addressed before moving forward.

---

## Instructions For The AI Producing The Audit

Read all provided code carefully before writing anything. Do not suggest fixes yet. The audit comes first. Be direct and specific — vague observations like "could be cleaner" are not useful. Name the file, the function, the line if relevant.

---

## Audit Structure

### Overview
A 2-3 sentence honest summary of the codebase or component as a whole. What is it doing well? What is its biggest weakness? What is the single most important thing to address?

---

### What's Working
Things that are well-implemented and should be left alone or used as a model for the rest of the code. Explain why each item is working — don't just list things.

---

### What's Fragile
Code that works right now but is likely to break under change, scale, or edge cases. For each item:
- What it is
- Why it's fragile
- What kind of change would break it

---

### What's Unclear
Code that is hard to understand, poorly named, or missing context. For each item:
- What is confusing and why
- What information is missing to understand it properly

---

### What's Missing
Obvious gaps — error handling that isn't there, edge cases that aren't covered, types that are incomplete, accessibility that's absent. Only flag things that are genuinely missing, not speculative nice-to-haves.

---

### Technical Debt Register
A prioritised list of everything worth addressing, ordered by impact:

| Priority | Item | File / Location | Effort | Impact |
|----------|------|----------------|--------|--------|
| 1 | ... | ... | Low/Med/High | Low/Med/High |

Effort = how hard to fix. Impact = how much it improves the codebase.

---

### What Not To Touch
Things that look unusual but are intentional, or things that work fine and don't need to be changed. Explicitly flagging these prevents unnecessary churn in a future refactor session.

---

### Recommended Next Action
One concrete recommendation for what to do first based on the audit. Should be specific enough to act on immediately.

---

## How To Use The Output

After reviewing the audit:
- To act on it: start a new session with `SKILL-refactor.md` and upload the audit as context
- To continue development: use the audit to inform which areas to be careful around
- To hand off: include the audit alongside `TOOL-SESSION-continue.md` output for full context

---

## Notes For The AI

- Do not soften findings to be polite — an honest audit is more valuable than a comfortable one
- Do not audit things that weren't provided — only assess what's in front of you
- Do not conflate style preferences with actual problems — flag real issues, not taste differences
- If the code is genuinely good, say so clearly and explain why
