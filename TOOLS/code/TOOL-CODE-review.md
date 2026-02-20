# TOOL-CODE-review.md

```
TOOL: Code Review
GROUP: code
USE FOR: PR-style review of code before merging, shipping, or handing off
PAIRS WITH: SKILL-refactor.md (to act on findings), any SYSTEM.md
```

---

## What This Tool Does

When uploaded to a session, this tool instructs the AI to perform a thorough code review — the kind you'd want from a senior engineer before merging a PR. It looks for bugs, performance issues, security concerns, type safety gaps, and readability problems. It is opinionated and direct.

No changes are made during the review. Findings are flagged with severity so you can decide what to act on.

---

## Instructions For The AI Performing The Review

Read all provided code before writing a single finding. Review with the mindset of: "would I approve this PR?" Be specific — reference file names, function names, and line context. Assign every finding a severity level. Don't pad the review with praise for things that are merely adequate.

---

## Severity Levels

| Level | Meaning |
|-------|---------|
| 🔴 **Blocker** | Must be fixed before this ships. Bug, data loss risk, security hole, broken behaviour. |
| 🟠 **Major** | Should be fixed soon. Likely to cause problems under real conditions. |
| 🟡 **Minor** | Worth fixing but not urgent. Readability, style, small inefficiency. |
| 🔵 **Suggestion** | Optional improvement. Good idea but not a problem as-is. |

---

## Review Structure

### Summary
One short paragraph: overall quality assessment, primary concern, and a clear ship/don't ship recommendation with reasoning.

---

### Findings

Each finding follows this format:
```
[SEVERITY] Short title
Location: file / function / line context
Issue: what the problem is
Risk: what could go wrong if left unfixed
Fix: the specific change needed
```

Group findings by severity, blockers first.

---

### Type Safety
A dedicated section for TypeScript (or typed language) specific concerns:
- Missing or incorrect types
- Unsafe casts or assertions
- Any use of `any`
- Incomplete interface definitions
- Runtime values that aren't validated before use

---

### Performance
Flag anything that will cause visible performance problems at real scale:
- Unnecessary re-renders (React)
- Expensive operations in hot paths
- Missing memoization where it matters
- N+1 query patterns
- Unthrottled event listeners

Only flag real concerns — don't speculate about performance problems that don't exist.

---

### Security
Flag anything that could be exploited:
- Unsanitized user input
- Exposed secrets or credentials
- Unsafe eval or dynamic code execution
- Missing authentication or authorization checks
- XSS vectors

---

### What's Good
2-3 specific things done well. Not padding — if something is implemented cleanly, say so and say why. This helps the author know what patterns to repeat.

---

### Verdict
```
SHIP:         Yes / No / Yes with fixes
BLOCKERS:     [count]
MAJORS:       [count]
MINORS:       [count]
SUGGESTIONS:  [count]
```

---

## Notes For The AI

- A review with no findings is almost always wrong — look harder
- Do not invent problems that aren't there — only flag real issues
- Do not conflate personal style preferences with actual bugs
- If the codebase context is unclear, ask one question before reviewing rather than making assumptions
- If code is genuinely excellent, a short review with few findings is the right output — don't pad it
