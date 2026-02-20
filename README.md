```
██████╗ ██╗      █████╗ ██╗   ██╗██████╗  ██████╗  ██████╗ ██╗  ██╗   ███╗   ███╗██████╗
██╔══██╗██║     ██╔══██╗╚██╗ ██╔╝██╔══██╗██╔═══██╗██╔═══██╗██║ ██╔╝   ████╗ ████║██╔══██╗
██████╔╝██║     ███████║ ╚████╔╝ ██████╔╝██║   ██║██║   ██║█████╔╝    ██╔████╔██║██║  ██║
██╔═══╝ ██║     ██╔══██║  ╚██╔╝  ██╔══██╗██║   ██║██║   ██║██╔═██╗    ██║╚██╔╝██║██║  ██║
██║     ███████╗██║  ██║   ██║   ██████╔╝╚██████╔╝╚██████╔╝██║  ██╗██╗██║ ╚═╝ ██║██████╔╝
╚═╝     ╚══════╝╚═╝  ╚═╝   ╚═╝   ╚═════╝  ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝╚═╝     ╚═╝╚═════╝
```

##### An Opinionated Prompting Framework for AI Collaboration

---

## What is PLAYBOOK.md?

PLAYBOOK.md is an opinionated collection of prompting formats, guidelines, system prompts, skills, and tools designed to bring out the full potential of AI when working with Large Language Models.

It's not a template — it's a philosophy. A set of conventions that, when adopted, fundamentally changes how you collaborate with AI. It turns generic chatbot sessions into focused, high-signal partnerships.

---

## Philosophy

Most people approach AI prompting like using a search engine: a quick query, a quick answer, repeat. That works for simple tasks, but it leaves enormous capability on the table.

PLAYBOOK.md is built on the premise that **AI is a collaborator, not a tool**. When you define your role, state your constraints, and establish a working rhythm, the quality of output improves dramatically. It's the difference between having an intern who guesses at what you want and having a senior partner who knows exactly how you think.

This playbook captures what works — not as rigid rules, but as a living set of patterns you can adapt, extend, and make your own.

---

## Structure

```
PLAYBOOK.md/
├── STYLES/              # Collaboration styles (system prompts that define AI behavior)
│   └── technical-collaborator/
│       ├── SYSTEM.md   # Core collaboration principles
│       └── SKILLS/     # Domain-specific skills
│           └── web/    # Web development skills
│
└── TOOLS/              # Prompting tools for specific scenarios
    ├── code/           # Code-focused tools
    │   ├── TOOL-CODE-decide.md
    │   ├── TOOL-CODE-review.md
    │   └── TOOL-CODE-audit.md
    │
    ├── creative/       # Creative-focused tools
    │   ├── TOOL-CREATIVE-brief.md
    │   ├── TOOL-CREATIVE-decide.md
    │   └── TOOL-CREATIVE-naming.md
    │
    └── session/        # Session management tools
        ├── TOOL-SESSION-continue.md
        └── TOOL-SESSION-riff.md
```

### STYLES — How the AI Behaves

Styles are system prompts that define the AI's role, behavior, and collaboration approach. The `technical-collaborator` style, for example, establishes:

- **Role locking** — The AI immediately adopts the role and constraints you define
- **Planning before coding** — No code until you've approved the plan
- **One thing at a time** — Iterative, deliberate progress
- **Explicit file scope** — Clear boundaries on what changes and what doesn't
- **Minimal edits** — Targeted changes over full rewrites

### SKILLS — Domain-Specific Expertise

Skills are modular prompts that give the AI specialized knowledge for particular domains. Under `SKILLS/web/`, you'll find skills for:

- Component architecture
- Motion design
- Awwwards-level aesthetics
- Copywriting for the web
- Sitemap planning

### TOOLS — Situational Prompting Frameworks

Tools are structured prompts for specific situations. They don't just tell the AI what to do — they tell it **how to think** about the problem:

- **decide** — A structured framework for making technical decisions with clear recommendations
- **review** — Code review protocols that catch real issues
- **brief** — Creative brief formats that produce better outputs
- **audit** — Systematic analysis frameworks

---

## Usage

### The Basic Pattern

Every session starts the same way:

```
you are a [role]
stack constraints: [technologies]
i want to [what you're building]
```

The AI locks in your role and constraints immediately and stays within them for the entire session.

### Layering Tools

The real power comes from layering tools on top of styles:

1. **Start with a STYLE** — This defines how the AI collaborates
2. **Add SKILLS** — These provide domain expertise
3. **Apply TOOLS** — These handle specific situations as they arise

Not every session needs every layer. Sometimes you just need a skill. Sometimes a tool is enough on its own. The framework is modular — use what you need.

### Iterative Workflow

The collaboration flows like this:

1. **Define** — AI confirms your role and constraints
2. **Plan** — AI summarizes the approach and waits for your go-ahead
3. **Execute** — AI makes targeted, surgical changes
4. **Review** — AI explains what changed and why
5. **Iterate** — You give feedback, AI adjusts

This rhythm — define, plan, execute, review, iterate — is the heartbeat of effective AI collaboration.

---

## Why This Exists

Because most prompting advice is shallow. "Be specific." "Give examples." "Use role-playing." None of it tells you **how** to collaborate — it just tells you how to ask.

PLAYBOOK.md is different. It's built from real sessions, real failures, and real discoveries about what makes AI perform at its best. It's opinionated because neutrality doesn't produce results. It's structured because chaos doesn't either.

This is for people who treat AI as a serious part of their workflow — not a novelty, not a gimmick, but a genuine collaborator that deserves the same clarity, context, and respect you'd give a human partner.

---

## About

Created by [**xsqu1znt**](https://github.com/xsqu1znt)

---

<div align="center">

Built with 💜 for the coding + AI community

</div>
