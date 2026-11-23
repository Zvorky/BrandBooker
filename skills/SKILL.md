---
name: brandbooker
description: Routes brandbook authorship, audits, and governance across philosophy, architecture, visual identity (vector/Bézier & optical engineering), color (OKLCH/WCAG/APCA), typography, human interface (concentric radii & 24dp iconography), packaging, DAM, and 6-gate critical review. Use when building or reviewing a brand system, brandbook, identity guidelines, design OS, or brand consistency audit.
---

# Brandbook Orchestrator

Entry point for this skill set. Use this skill to choose specialists, enforce the manifesto, and produce a complete brandbook—not a decorative style PDF.

## Purpose

A brandbook is the **single source of truth** for aesthetics, strategy, tone, and execution. It governs every contact point: dense digital UI, marketing surfaces, vector/SVG construction, and the mechanical friction of opening a physical package.

## Manifesto (Apply Everywhere)

1. **Confidence through suppression** — Subtract until only structural essentials remain. Removing the non-essential is sophistication.
2. **Governance by enforcement** — Clear space, contrast, concentric radii, type roles, and spacing must exist as mathematical tokens and tool constraints—not prose alone.
3. **Optical & geometric precision** — Pure math distorts human perception. Clean Bézier geometry (zero-handle elimination, G2 continuity) must be paired with deliberate optical compensation.
4. **Silent ergonomics** — Digital products follow Clarity, Deference, and Depth. Motion and haptics explain change; they never create delay or sensory noise.
5. **Tangible worth** — Packaging and merchandise validate premium perception through ritual, honest materials, and restraint.

## Skill Router

| If the task involves… | Load |
|---|---|
| Critiquing an **existing** brandbook; 6-test acceptance gate, score, remediation | [`brandbook-review/SKILL.md`](brandbook-review/SKILL.md) |
| Doctrine, principles, strategic discovery, stylescapes, voice posture | [`design-philosophy/SKILL.md`](design-philosophy/SKILL.md) |
| Product naming, branded house, lockups, equity dilution | [`brand-architecture/SKILL.md`](brand-architecture/SKILL.md) |
| Logo, Bézier/vector rules, optical compensations, responsive marks, supergraphics | [`visual-identity/SKILL.md`](visual-identity/SKILL.md) |
| OKLCH/CMYK/Pantone palette, WCAG 2.1 + APCA contrast, type pairing & roles | [`color-typography/SKILL.md`](color-typography/SKILL.md) |
| UI behavior, concentric radii math, G3 squircles, 24dp icon grids, motion | [`human-interface/SKILL.md`](human-interface/SKILL.md) |
| Unboxing, lid friction, fiber packs, physical ritual | [`packaging-experience/SKILL.md`](packaging-experience/SKILL.md) |
| DAM decision-tree taxonomy, permissions, raster/vector scales, token sync | [`brand-governance/SKILL.md`](brand-governance/SKILL.md) |

**Existing artifact to audit?** Start with `brandbook-review`, then pull specialists as rubrics for each finding.

Load multiple specialists when the task spans domains. Always keep this manifesto in force.

## Full Brandbook Workflow

```
Brandbook build:
- [ ] 1. Philosophy, stylescape & voice locked      → design-philosophy
- [ ] 2. Architecture & naming statutes            → brand-architecture
- [ ] 3. Vector rules, optical fixes & mark matrix → visual-identity
- [ ] 4. OKLCH/CMYK color + type pairing tokens    → color-typography
- [ ] 5. HIG, concentric radii & 24dp icons        → human-interface
- [ ] 6. Packaging (if physical goods)             → packaging-experience
- [ ] 7. DAM taxonomy + token sync plan            → brand-governance
- [ ] 8. Pass all 6 technical acceptance gates     → brandbook-review
```

### Sequencing rules

1. **Strategy & stylescape before pixels** — Never define color, grid, or type before doctrine, competitive audit, and visual territory (stylescape) are explicit.
2. **One market front** — Default to monolithic (branded house) architecture; document any exception.
3. **Geometry corrected for the eye** — Enforce clean Bézier paths alongside explicit optical compensations (optical centering, overshoot, stroke contrast, concentric radii).
4. **Prohibitions are first-class** — Ship a visual catalog of unacceptable misuse.
5. **Ship as a living system** — Pair the document with end-user-oriented DAM folders, bidirectional tokens, and 6-gate QA verification so deviation is hard at creation time.

## Scope Gates

| Scope | Required chapters |
|---|---|
| Always | Philosophy & Stylescape, Architecture, Visual Identity (Vector/Optical/Responsive), Color & Typography, Governance & DAM |
| Digital products | + Human Interface (Concentric Radii & Icon Grid) |
| Physical goods / kits | + Packaging Experience |

If a gate does not apply, state that explicitly in the brandbook rather than omitting silently.

## Output Quality Bar

A brandbook produced with this skill set must:
- Open with enforceable philosophy, stylescape direction, and voice posture
- Specify architecture, naming grammar, and lockup hierarchy
- Enforce clean vector construction, optical compensations, clear-space, and responsive minimum-size tables
- Define perceptual (`OKLCH`) and print (`CMYK`/`PMS`) color systems validated under `WCAG 2.1` + `APCA`, plus functional type pairing
- Include HIG pillars, concentric radius formulas, and 24×24 dp iconography specs when software is in scope
- Include packaging ritual and material bans when physical goods are in scope
- Describe decision-tree DAM taxonomy, raster/vector export matrices, and token propagation
- Pass all 6 acceptance tests in `brandbook-review`

## Forbidden

- One-off PDFs with no governance path
- Divisions inventing separate visual identities
- Mechanical font stretching, uncompensated nested border-radii, or zero-handle Bézier artifacts
- Decorative animation, false italics, or random spacing
- Co-branding that fuses marks into a hybrid signature
- Merchandise on vulgar, disposable, or prestige-misaligned surfaces
- Rules that cannot be measured, tokenized, or shown as correct/incorrect pairs
