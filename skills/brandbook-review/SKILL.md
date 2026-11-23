---
name: brandbook-review
description: >-
  Audits existing brandbooks, identity systems, and brand asset packages
  against the 6-Test Acceptance Protocol and Brandbooker standards, producing a
  scored remediation report. Use whenever a brand is created, materially
  updated, or audited before release.
---

# Brandbook Critical Review & 6-Test Acceptance Gate

Audit existing brandbooks, `DESIGN.md` files, `tokens.css`, and asset packages with empirical rigor. Do not praise; identify measurable gaps, score compliance, and prescribe exact remediations.

## Required Context (Load Before Scoring)

Always load [`../SKILL.md`](../SKILL.md), [`../design-philosophy/SKILL.md`](../design-philosophy/SKILL.md), [`../brand-architecture/SKILL.md`](../brand-architecture/SKILL.md), [`../visual-identity/SKILL.md`](../visual-identity/SKILL.md), [`../color-typography/SKILL.md`](../color-typography/SKILL.md), and [`../brand-governance/SKILL.md`](../brand-governance/SKILL.md). Load [`../human-interface/SKILL.md`](../human-interface/SKILL.md) for digital products and [`../packaging-experience/SKILL.md`](../packaging-experience/SKILL.md) when physical goods or kits are in scope.

## 1. Mandatory 6-Test Acceptance Protocol

Before approving any brand system for production or client handover, execute all six acceptance tests:

1. **Test 1 - Micro-Scale & Stress Test (`16x16 px` & `80 px`):**
   - Inspect the mark rendered in a single solid color at `16x16 px` (favicon) and `80 px` (mobile header).
   - **Fail Criteria:** Thin hairlines vanishing, internal counters clogging, reliance on gradients/drop shadows to separate shapes, or missing responsive fallback variant.
2. **Test 2 - Contrast, Gamut & Palette Audit:**
   - Verify all foreground/background token pairs against `WCAG 2.1 AA` (`4.5:1` body / `3:1` large & UI) and `APCA` (`Lc >= 60` body / `Lc >= 45` headings).
   - Verify color-blind safety (no uncompensated red/green, red/black, or blue/yellow overlaps with `Delta L < 35`) and confirm `CMYK`/`Pantone` Coated & Uncoated definitions if print is in scope.
3. **Test 3 - Fallback Typography & Metric Parity Test:**
   - Verify web fonts ship self-hosted (`woff2`) with universally available system fallback stacks and calibrated metric overrides (`size-adjust`, `ascent-override`) so layout does not break or shift when primary fonts fail or load slowly.
   - Confirm zero mechanical font stretching, `font-synthesis: none`, body leading `>= 150%`, and valid functional font pairing.
4. **Test 4 - Verbal Identity & Claim Integrity Audit:**
   - Verify sample headlines, CTAs, and voice rules align with the brand doctrine and avoid generic AI filler/cliches.
   - Verify every factual claim (ratings, credentials, prices, awards) is backed by an explicit primary source URL; flag or strip any unverified claim.
5. **Test 5 - Template & Token Usability Test:**
   - Verify `DESIGN.md` and `tokens.css` cover all required semantic tokens, modular spacing, and concentric border-radius math (`R_inner = max(0, R_outer - (padding + border))`), so non-designers or downstream agents can assemble pages without breaking visual rhythm.
6. **Test 6 - Independent Handover & DAM Completeness Test:**
   - Verify an external developer or print vendor can produce any deliverable solely from the brand folder without asking questions: clean `SVG`/`PDF`/`EPS` vectors (no zero-handles, proper `viewBox`), `1920px`/`960px`/`192px` rasters, clear-space/minimum-size tables, and forbidden-use catalog.

## 2. Audit Rubric & Scoring (`0-100`)

| Domain | Weight | Key Inspection Checks |
|---|---|---|
| **Doctrine & Stylescape** | `15%` | Manifesto clarity, stylescape direction, voice posture, verified claims |
| **Brand Architecture** | `10%` | Monolithic vs. endorsed rules, naming grammar, lockup hierarchy |
| **Vector & Optical Craft** | `20%` | Clean Bezier paths, optical compensations, responsive minima, misuse catalog |
| **Color & Typography** | `20%` | OKLCH scales, WCAG 2.1 + APCA scores, color-blind safety, pairing & fallbacks |
| **HIG & Geometry** | `15%` | Concentric radius formula, `24x24 dp` icon grid, touch targets, reduced-motion |
| **Governance & DAM** | `20%` | Decision-tree folder hierarchy, required formats/scales, token sync, history log |

- **Scope Note:** When physical goods or kits are in scope per `../SKILL.md`, audit `../packaging-experience/SKILL.md` as well and flag any packaging/unboxing/material gaps explicitly in the report.
- **Cross-Skill Contradiction Scan:** Check for conflicts between rules across loaded skills (e.g., architecture vs. lockups, chromatic budget vs. accents, motion vs. performance, and documentation vs. DAM/tokens).
- **Release Threshold:** Minimum score **`85/100`** with **zero `FAIL` flags** on Tests 1, 2, or 4.

## Workflow

1. Load required specialist skills for the declared scope.
2. Run all 6 acceptance tests, check cross-skill contradictions, and score each domain (`0-100`).
3. Write the audit report to `history/brandbook-review-YYYY-MM-DD.md` with prioritized fixes tied to the owning specialist skill.

## Deliverables

- Scored Markdown audit report saved to `history/brandbook-review-YYYY-MM-DD.md`

## Checklist

```text
Brandbook review chapter:
- [ ] Required specialist skills for scope loaded prior to scoring
- [ ] All 6 acceptance tests and cross-skill contradiction check executed
- [ ] Score calculated (0-100) with explicit 85/100 and zero-FAIL gate check on Tests 1, 2, and 4
- [ ] Findings prioritized with target specialist skill for every remediation
```

## Forbidden

- Scoring without loading the required specialist skills
- Flattery or passing vague rules without measurable constraints or evidence
- Ignoring physical/packaging scope when products exist or omitting remediation owners
