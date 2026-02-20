# TOOL-SESSION-continue.md

```
TOOL: Session Handoff — Continue
GROUP: session
USE FOR: Ending a session and picking up exactly where you left off in a new one
PAIRS WITH: Any SYSTEM.md + skill combination
```

---

## What This Tool Does

When uploaded to a session, this tool instructs the AI to produce a precise handoff document. The output is designed to be uploaded to a new session — with the same or a different AI — so work can continue without losing context, decisions, or momentum.

The new AI receiving the handoff document should be able to continue mid-thought.

---

## Instructions For The AI Producing The Summary

When this tool is uploaded, generate a handoff document using the structure below. Be precise and factual. Do not editorialize. Do not summarize what could be stated exactly.

---

## Handoff Document Structure

### Session Identity
- **Role**: What role the AI was operating as
- **Stack / Constraints**: Every technical or creative constraint that was declared
- **Skills active**: Which skill files were in use
- **Goal**: What the session was trying to accomplish, in one sentence

---

### Current State
A clear, file-by-file or component-by-component snapshot of where things stand right now:
- What exists and is working
- What exists but is incomplete
- What was planned but not yet started

For code projects, list every file that was created or modified with a one-line description of its current state.

---

### Decisions Made
A numbered list of every significant decision that was made and locked in during the session. Include:
- What was decided
- Why (the reasoning that was accepted)
- Any constraints that decision introduced

---

### Things Tried That Didn't Work
A numbered list of approaches that were attempted and abandoned. Include:
- What was tried
- Why it failed or was rejected
- What was learned from it

This section is critical. It prevents the next session from repeating failed approaches.

---

### Open Questions
Anything that was unresolved, deferred, or actively being debated at the point the session ended.

---

### Exact Next Step
The single most immediate thing to do when the new session begins. Should be specific enough that the AI can state it back without ambiguity.

---

### Files To Carry Forward
List every file the user should upload or reference in the new session to restore full context.

---

## How To Use The Output

Start a new session with:
```
[upload SYSTEM.md]
[upload relevant skill files]
[upload this handoff document]

continue from the handoff document
```

The AI will read the handoff, confirm its understanding of the current state and next step, and wait for you to say proceed.
