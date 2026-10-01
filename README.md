# BrandBooker

A skill set for LLM agents that author, audit, and govern world-class brand systems. Treat a brandbook as an operating system for culture, design, and communication—not a static style guide.

## Purpose

These skills encode the anatomy of an excellence-grade brandbook: philosophy, architecture, visual policing, chromatic and typographic engineering, human interface rules, packaging ritual, and operational governance. Agents use them to produce or review brand documentation with mathematical precision and intentional restraint.

## Skill Map

| Skill | Path | Responsibility |
|-------|------|----------------|
| **Brandbook Orchestrator** | [`skills/SKILL.md`](skills/SKILL.md) | Entry point. Routes work across the skill set and enforces the global manifesto. |
| **Design Philosophy** | [`skills/design-philosophy/`](skills/design-philosophy/) | Functional essentialism, good-design principles, “less but better.” |
| **Brand Architecture** | [`skills/brand-architecture/`](skills/brand-architecture/) | Monolithic architecture, naming, lockups, sub-brand control. |
| **Visual Identity** | [`skills/visual-identity/`](skills/visual-identity/) | Logo construction, clear space, sizing, co-branding, merchandise bans. |
| **Color & Typography** | [`skills/color-typography/`](skills/color-typography/) | Neutral-led palettes, semantic color, type roles, modular spacing. |
| **Human Interface** | [`skills/human-interface/`](skills/human-interface/) | Clarity, deference, depth; motion, haptics, accessibility layout. |
| **Packaging Experience** | [`skills/packaging-experience/`](skills/packaging-experience/) | Unboxing ritual, structural friction, sustainable materials. |
| **Brand Governance** | [`skills/brand-governance/`](skills/brand-governance/) | DAM, taxonomy, permissions, design tokens, live sync to tools. |

## How Agents Should Use This

1. Start at [`skills/SKILL.md`](skills/SKILL.md) to select the right specialist skill(s).
2. Load only the skills required for the current task (progressive disclosure).
3. Embed rules as enforceable constraints—never as optional taste suggestions.
4. Prefer subtraction over decoration; every element must earn its place.

## Design Posture

- **Radical aesthetic suppression** — remove ornament; retain only what serves function and clarity.
- **Governance by technology** — clear space, contrast, type scales, and spacing become machine-enforceable tokens, not PDF suggestions.
- **Silent ergonomics** — interfaces defer to content; motion and haptics explain state, never delay it.
- **Tangible value** — physical packaging validates perceived worth through ritual, materials, and restraint.

## Repository Layout

```
BrandBooker/
├── README.md
└── skills/
    ├── SKILL.md                 # Master orchestrator (maps all skills)
    ├── design-philosophy/
    │   └── SKILL.md
    ├── brand-architecture/
    │   └── SKILL.md
    ├── visual-identity/
    │   └── SKILL.md
    ├── color-typography/
    │   └── SKILL.md
    ├── human-interface/
    │   └── SKILL.md
    ├── packaging-experience/
    │   └── SKILL.md
    └── brand-governance/
        └── SKILL.md
```

## Conventions

- All content is written in **English**.
- Every `SKILL.md` includes YAML frontmatter (`name`, `description`).
- Skills teach **concepts and enforceable rules**, not case-study citations.
- No third-party brand identities are referenced in this repository.
