# BrandBooker

Skill set for LLM agents that author, audit, and govern brand systems.

A brandbook is not a style guide. It is an **operating system** for culture, design, and communication—the single source of truth for how an organization looks, speaks, and ships.

## What This Repo Contains

Eight skills that encode a complete excellence-grade brandbook:

| Order | Skill | Path | Owns |
|------:|-------|------|------|
| 0 | Orchestrator | [`skills/SKILL.md`](skills/SKILL.md) | Routing, manifesto, full-build workflow |
| 1 | Design Philosophy | [`skills/design-philosophy/`](skills/design-philosophy/) | Doctrine, good-design principles, voice posture |
| 2 | Brand Architecture | [`skills/brand-architecture/`](skills/brand-architecture/) | Monolithic model, naming, lockups |
| 3 | Visual Identity | [`skills/visual-identity/`](skills/visual-identity/) | Logo, clear space, minima, co-branding, merch |
| 4 | Color & Typography | [`skills/color-typography/`](skills/color-typography/) | Palette hierarchy, contrast, type roles, spacing |
| 5 | Human Interface | [`skills/human-interface/`](skills/human-interface/) | Clarity, deference, depth, motion, haptics |
| 6 | Packaging Experience | [`skills/packaging-experience/`](skills/packaging-experience/) | Unboxing ritual, friction, sustainable materials |
| 7 | Brand Governance | [`skills/brand-governance/`](skills/brand-governance/) | DAM, taxonomy, permissions, tokens, sync |

## How to Use

1. **Start at the orchestrator** — [`skills/SKILL.md`](skills/SKILL.md) selects specialist skills and enforces the global manifesto.
2. **Load only what the task needs** — progressive disclosure; do not dump every skill into context.
3. **Treat rules as constraints** — measurable, tokenizable, enforceable. Never as optional taste.
4. **Subtract first** — every element must earn its place.

## Non-Negotiable Posture

- **Suppression** — remove ornament; keep only what serves function and clarity.
- **Enforcement** — clear space, contrast, type, and spacing live as tokens and tool locks, not PDF prose alone.
- **Silent ergonomics** — UI defers to content; motion and haptics explain state, never delay it.
- **Tangible worth** — packaging and merchandise validate premium perception through ritual and honest materials.

## Layout

```
BrandBooker/
├── README.md
└── skills/
    ├── SKILL.md                      # Orchestrator
    ├── design-philosophy/SKILL.md
    ├── brand-architecture/SKILL.md
    ├── visual-identity/SKILL.md
    ├── color-typography/SKILL.md
    ├── human-interface/SKILL.md
    ├── packaging-experience/SKILL.md
    └── brand-governance/SKILL.md
```

## Conventions

- English only.
- Every `SKILL.md` has YAML frontmatter (`name`, `description`).
- Skills embed concepts as enforceable rules—no research citations, no third-party brand identities.
- Specialist skills share a fixed section schema: Purpose → Rules → Workflow → Deliverables → Checklist → Forbidden.
