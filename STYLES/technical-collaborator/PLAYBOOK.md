# PLAYBOOK.md
## Your Quick Reference for AI Collaboration

---

## File Structure

```
technical-collaborator/
  PLAYBOOK.md
  SYSTEM.md
  SKILLS/
    SKILL-refactor.md
    web/
      SKILL-art-director.md
      SKILL-awwwards.md
      SKILL-component.md
      SKILL-copywriting.md
      SKILL-motion.md
      SKILL-sitemap.md
      SKILL-three.md

TOOLS/
  session/
    TOOL-SESSION-continue.md
    TOOL-SESSION-riff.md
  code/
    TOOL-CODE-audit.md
    TOOL-CODE-review.md
    TOOL-CODE-decide.md
  creative/
    TOOL-CREATIVE-brief.md
    TOOL-CREATIVE-naming.md
    TOOL-CREATIVE-decide.md
```

**Skills** shape how the AI works with you throughout a session.
**Tools** are uploaded when you need a specific output — a review, a decision, a handoff.
**SYSTEM.md** is always first, every session, no exceptions.

---

## How A Session Works

```
1. Upload SYSTEM.md                    ← always first
2. Upload skill file(s)                ← sets the mode for the session
3. Upload tool file(s) if needed       ← for specific outputs
4. Upload image references if relevant
5. Write your prompt
```

**Your prompt format:**
```
you are a [role]
stack constraints: [your stack]
i want to [task]
```

The AI reads the files first, confirms what it understood, then asks one clarifying question or states its first planned step — and waits for you before doing anything.

---

## The Skills

| File | What It Does | Use When |
|------|-------------|----------|
| `SKILL-component.md` | React component creation, TypeScript, composition patterns | Building or fixing any UI component |
| `SKILL-sitemap.md` | Sitemap planning, layout ideation, section strategy | Starting a new site or page from zero |
| `SKILL-awwwards.md` | Bold design decisions, unconventional layouts, anti-generic execution | You want something that stands out |
| `SKILL-motion.md` | Framer Motion + GSAP, scroll animation, interaction design | Anything that moves |
| `SKILL-three.md` | Three.js, R3F, shaders, procedural 3D | Any WebGL or 3D work |
| `SKILL-copywriting.md` | Human copy, tone discovery, conversion writing | Writing any text that users will read |
| `SKILL-art-director.md` | Mood, palette, typography direction, creative brief | Defining a visual language before building |
| `SKILL-refactor.md` | Safe code cleanup, readability, reducing complexity | Improving existing code without adding features |

---

## The Tools

### Session Tools
Use at the end of a session to preserve context for a new one.

| File | What It Does | Use When |
|------|-------------|----------|
| `TOOL-SESSION-continue.md` | Precise handoff document — state, decisions, next step | You want to pick up exactly where you left off |
| `TOOL-SESSION-riff.md` | Loose directional brief — territory, what worked, open space | You want a fresh angle on the same problem |

### Code Tools
Use when you need a structured read or decision on code.

| File | What It Does | Use When |
|------|-------------|----------|
| `TOOL-CODE-audit.md` | Full codebase read — what works, what's fragile, what's missing | Before refactoring or handing off a project |
| `TOOL-CODE-review.md` | PR-style review — bugs, performance, security, readability | Before shipping or merging code |
| `TOOL-CODE-decide.md` | Structured technical comparison with recommendation | Stuck between two technical approaches |

### Creative Tools
Use when you need a structured read or decision on creative work.

| File | What It Does | Use When |
|------|-------------|----------|
| `TOOL-CREATIVE-brief.md` | Turns a vague idea into a clean actionable brief | You have a fuzzy concept that needs crystallising |
| `TOOL-CREATIVE-naming.md` | Naming options with rationale for anything | Naming components, features, products, copy |
| `TOOL-CREATIVE-decide.md` | Structured creative comparison with recommendation | Stuck between two design or copy directions |

---

## Skill Combinations

### New site or landing page from scratch
```
Phase 1:  SYSTEM.md + SKILL-art-director.md
Phase 2:  SYSTEM.md + SKILL-sitemap.md + SKILL-copywriting.md
Phase 3:  SYSTEM.md + SKILL-awwwards.md + SKILL-component.md
Phase 4:  SYSTEM.md + SKILL-motion.md + SKILL-component.md
```
Work phases in order. Don't touch code before phases 1 and 2 are signed off.

---

### Interactive animated component
```
SYSTEM.md + SKILL-component.md + SKILL-motion.md
```
Motion uses Framer Motion or GSAP based on your stack constraints.

---

### 3D scene or WebGL feature
```
SYSTEM.md + SKILL-three.md + SKILL-component.md
```
Add `SKILL-motion.md` if scroll-driven or timeline animations sit alongside the 3D.

---

### Design that needs to stand out
```
SYSTEM.md + SKILL-awwwards.md + SKILL-art-director.md
```
Art director sets the visual language. Awwwards executes bold decisions within it.

---

### Writing copy for a page
```
SYSTEM.md + SKILL-copywriting.md
```
Add `SKILL-art-director.md` if tone and brand voice haven't been established yet.

---

### Cleaning up existing code
```
SYSTEM.md + SKILL-refactor.md
```
Run `TOOL-CODE-audit.md` first if you want a read before touching anything.

---

## Tool Usage Patterns

### Ending a session
```
[in current session, upload TOOL-SESSION-continue.md or TOOL-SESSION-riff.md]
produce a handoff document for this session
```
Save the output. Upload it at the start of the next session.

---

### Continuing from a handoff
```
SYSTEM.md + [relevant skills] + [handoff document]
continue from the handoff document
```

---

### Before refactoring
```
SYSTEM.md + TOOL-CODE-audit.md + [paste or upload code]
audit this code
```
Then use the audit output to scope a `SKILL-refactor.md` session.

---

### Before shipping
```
SYSTEM.md + TOOL-CODE-review.md + [paste or upload code]
review this code
```

---

### Stuck on a decision
```
SYSTEM.md + TOOL-CODE-decide.md   ← for technical choices
SYSTEM.md + TOOL-CREATIVE-decide.md   ← for design/copy choices
```

---

### Starting from a vague idea
```
SYSTEM.md + TOOL-CREATIVE-brief.md
here's my rough idea: [brain dump]
```
Use the brief output to open a proper session with the right skills.

---

## When To Use Just One Skill

Don't over-stack. More files = more context for the AI to hold.

- Fixing a bug → just `SYSTEM.md`, no skill needed
- Refactoring one file → `SYSTEM.md + SKILL-refactor.md`
- Writing one section of copy → `SYSTEM.md + SKILL-copywriting.md`
- Tweaking a shader → `SYSTEM.md + SKILL-three.md`
- Naming a component → `SYSTEM.md + TOOL-CREATIVE-naming.md`

---

## Rules To Remember

**Before any code is written**, the AI should:
- State which files will change and which won't
- Explain the approach at a high level
- Wait for **proceed**

**If something breaks**, the AI should:
- Diagnose before suggesting a fix
- Apply the minimal fix
- Not refactor surrounding code

**If you say revert**, the AI restores the last known good state immediately.

**If output feels generic**, call it out — every skill has anti-slop rules baked in.

---

## Quick Cheat Sheet

```
No direction yet               → art-director + sitemap
Direction clear, start coding  → awwwards + component + copywriting
Needs to move                  → motion + component
3D / WebGL                     → three + component
Copy for a page                → copywriting
Code is messy                  → refactor (audit first)
Design feels safe              → awwwards + art-director
Stuck on a decision            → TOOL-CODE-decide or TOOL-CREATIVE-decide
Vague idea, need clarity       → TOOL-CREATIVE-brief
Session ending, want to resume → TOOL-SESSION-continue
Session ending, want new angle → TOOL-SESSION-riff
Need a name for something      → TOOL-CREATIVE-naming
About to ship code             → TOOL-CODE-review
```
