# TOOL-CREATIVE-naming.md

```
TOOL: Naming
GROUP: creative
USE FOR: Naming anything — products, components, files, variables, routes, features, copy, brands
PAIRS WITH: SKILL-copywriting.md, SKILL-component.md, TOOL-CREATIVE-brief.md
```

---

## What This Tool Does

When uploaded to a session, this tool instructs the AI to generate naming options with rationale. Good naming is specific, intentional, and consistent. This tool treats naming as a creative and technical discipline — not a quick task to rush through.

Works for any naming context: code, copy, brand, product, UI, or anything in between.

---

## Instructions For The AI Producing Names

Before generating options, confirm:
1. **What is being named?** (component, feature, product, page, variable, etc.)
2. **What context does it live in?** (codebase, brand, UI, copy)
3. **What constraints apply?** (naming conventions, character limits, must/must-not contain certain words)
4. **What feeling or meaning should the name carry?** (technical precision, warmth, wit, authority, simplicity)
5. **What names have already been rejected and why?**

If the context makes these obvious, skip the questions and go straight to options.

---

## Output Structure

### For Code Naming (components, variables, files, routes, functions)

Generate **5-8 options** across a range from literal to expressive. For each:
```
Name: ComponentName
Convention: PascalCase / camelCase / kebab-case / SCREAMING_SNAKE
Why: One sentence — what this name communicates and why it fits
Watch out: Any ambiguity, conflict with existing names, or reason to avoid
```

Then a recommendation:
```
RECOMMENDED: [Name]
REASON: [Why this one over the others]
```

---

### For Product / Feature / Brand Naming

Generate **6-10 options** across these categories:

**Descriptive** — says exactly what it is
**Metaphorical** — evokes the feeling or concept through analogy
**Coined** — invented word or portmanteau
**Referential** — nods to something cultural, technical, or historical
**Tonal** — prioritises how it sounds and feels over what it means

For each:
```
Name: [Name]
Type: [Descriptive / Metaphorical / Coined / Referential / Tonal]
Why: What this name does and who it works for
Doesn't work if: The scenario where this name fails
Domain available: [Unknown — user to check]
```

Then a shortlist of the top 3 with a recommendation and clear reasoning.

---

### For Copy Naming (headlines, CTAs, labels, section titles)

Generate **3 versions** across this range:

**Safe** — clear, direct, functional. No one will dislike it.
**Sharp** — more specific or unexpected. Has a point of view.
**Bold** — pushes further. Might need to earn it with context around it.

For each version explain the intent and what it assumes about the reader.

---

## Naming Principles The AI Should Apply

- **Specific beats generic** — "OrderConfirmation" beats "Success", "LaunchSection" beats "Hero"
- **Consistent beats clever** — a name that fits the existing pattern is better than a clever outlier
- **Pronounceable matters** — if you can't say it in a meeting without awkwardness, reconsider
- **Avoid abbreviations** unless they're universal in the codebase or domain
- **Length is a tradeoff** — longer names are clearer, shorter names are faster to type. Calibrate to context.
- **Names are promises** — a component called `Button` that does three different layout things is lying. Names should match behaviour.

---

## What To Avoid

- Names that describe implementation rather than intent (`useStateWithEffect` vs `useAnimatedToggle`)
- Generic placeholder names that defer the decision (`handleAction`, `MyComponent`, `utils`)
- Names that will age poorly (`NewDashboard`, `V2Header`, `TempFix`)
- Clever names that only make sense to the person who wrote them
- Names that conflict with reserved words, existing libraries, or established conventions in the codebase

---

## Notes For The AI

- Don't generate options you wouldn't actually recommend — quality over quantity
- If an obvious best name exists, say so immediately and explain why rather than padding with weak alternatives
- If the user rejects a recommendation, ask why before generating more — the rejection reason often unlocks the right answer
