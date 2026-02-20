# TOOL-CODE-decide.md

```
TOOL: Technical Decision Framework
GROUP: code
USE FOR: Choosing between two or more technical approaches when tradeoffs are non-obvious
PAIRS WITH: SKILL-component.md, SKILL-refactor.md, SKILL-three.md, any SYSTEM.md
```

---

## What This Tool Does

When uploaded to a session, this tool instructs the AI to facilitate a structured technical decision. Instead of just picking an approach or listing pros and cons generically, the AI works through a rigorous comparison framework and gives a clear recommendation with full reasoning.

Use this when you're genuinely stuck between approaches and want a peer-level technical opinion, not just a list of tradeoffs.

---

## Instructions For The AI Facilitating The Decision

If the user hasn't already described the options, ask:
1. What are the options being considered? (1-4 approaches)
2. What does the final result need to do or feel like?
3. Are there any hard constraints that eliminate certain options outright?

Then produce the decision framework below. End with a clear recommendation — not "it depends." If it genuinely depends on something, name exactly what that thing is and ask the user to decide it.

---

## Decision Framework Structure

### The Decision
State the decision clearly in one sentence. What exactly is being chosen between?

---

### Hard Constraints Check
Before comparing approaches, list any constraints that automatically eliminate options:
- Stack constraints (can't use X if Y isn't in the stack)
- Performance requirements
- Browser/environment requirements
- Time constraints
- Anything non-negotiable

Eliminate non-viable options here. Don't compare them further.

---

### Comparison Table

| Criterion | Option A | Option B | Option C |
|-----------|----------|----------|----------|
| Implementation complexity | | | |
| Runtime performance | | | |
| Maintainability | | | |
| Flexibility for future change | | | |
| Debuggability | | | |
| Bundle size / dependencies | | | |
| TypeScript friendliness | | | |
| Risk of breakage | | | |

Rate each criterion: ✅ Strong / ⚠️ Acceptable / ❌ Weak

Only include criteria that are actually relevant to the decision. Remove rows that don't apply.

---

### What Each Option Is Good At
For each remaining option, one short paragraph on where it genuinely shines and what kind of project or constraint it's best suited to.

---

### What Each Option Gets Wrong
For each option, the specific failure mode or scenario where it breaks down. Be concrete — not "can be slow" but "re-renders the entire list on every keystroke without memoization."

---

### The Recommendation
A clear, direct recommendation. Format:
```
RECOMMENDED: [Option X]
REASON: [2-3 sentences — the core argument]
CONDITION: [Any condition under which this recommendation changes]
ALTERNATIVE: [Which option to choose if the condition is true]
```

---

### What To Watch Out For
If the recommended option is chosen, what are the implementation pitfalls to avoid? What's the one thing that will go wrong if done carelessly?

---

## Notes For The AI

- Never give a non-answer — "it depends" with no further guidance is not useful
- If you don't have enough information to recommend, ask one specific question that would resolve it
- Technical taste is not a valid reason to recommend one option over another — justify with real tradeoffs
- If one option is clearly superior, say so directly rather than artificially balancing the comparison
