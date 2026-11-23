---
name: brandbook-review
description: Audits existing brandbooks, identity systems, and brand asset packages against the 6-Test Acceptance Protocol and Brandbooker standards, producing a scored remediation report. Use whenever a brand is created, materially updated, or audited before release.
---

# Brandbook Critical Review & 6-Test Acceptance Gate

Audit existing brandbooks, `DESIGN.md` files, `tokens.css`, and asset packages with empirical rigor. Do not praise; identify measurable gaps, score compliance, and prescribe exact remediations.

## 1. Mandatory 6-Test Acceptance Protocol

Before approving any brand system for production or client handover, execute all six acceptance tests:

1. **Test 1 — Micro-Scale & Stress Test (`16×16 px` & `80 px`):**
   - Inspect the mark rendered in a single solid color at `16×16 px` (favicon) and `80 px` (mobile header).
   - **Fail Criteria:** Thin hairlines vanishing, internal counters clogging, reliance on gradients/drop shadows to separate shapes, or missing responsive fallback variant.
2. **Test 2 — Contrast, Gamut & Palette Audit:**
   - Verify all foreground/background token pairs against `WCAG 2.1 AA` (`4.5:1` body / `3:1` large & UI) and `APCA` (`Lc >= 60` body / `Lc >= 45` headings).
   - Verify color-blind safety (no uncompensated red/green, red/black, or blue/yellow overlaps) and confirm `CMYK`/`Pantone` Coated & Uncoated definitions if print is in scope.
3. **Test 3 — Fallback Typography & Metric Parity Test:**
   - Verify web fonts ship self-hosted (`woff2`) with universally available system fallback stacks and calibrated metric overrides (`size-adjust`, `ascent-override`) so layout does not break or shift when primary fonts fail or load slowly.
   - Confirm zero mechanical font stretching and valid functional font pairing.
4. **Test 4 — Verbal Identity & Claim Integrity Audit:**
   - Verify sample headlines, CTAs, and voice rules align with the brand doctrine and avoid generic AI filler/clichés.
   - Verify every factual claim (ratings, credentials, prices, awards) is backed by an explicit primary source URL; flag or strip any unverified claim.
5. **Test 5 — Template & Token Usability Test:**
   - Verify `DESIGN.md` and `tokens.css` cover all required semantic tokens, including concentric border-radius math (`R_inner = max(0, R_outer - (padding + border))`), so non-designers or downstream agents can assemble pages without breaking visual rhythm.
6. **Test 6 — Independent Handover & DAM Completeness Test:**
   - Verify an external developer or print vendor can produce any deliverable solely from the brand folder without asking questions: clean `SVG`/`PDF`/`EPS` vectors (no zero-handles, proper `viewBox`), `1920px`/`960px`/`192px` rasters, clear-space/minimum-size tables, and forbidden-use catalog.

## 2. Audit Rubric & Scoring (`0–100`)

| Domain | Weight | Key Inspection Checks |
|---|---|---|
| **Doctrine & Stylescape** | `15%` | Manifesto clarity, stylescape direction, voice posture, verified claims |
| **Brand Architecture** | `10%` | Monolithic vs. endorsed rules, naming grammar, lockup hierarchy |
| **Vector & Optical Craft** | `20%` | Clean Bézier paths, optical compensations, responsive minima, misuse catalog |
| **Color & Typography** | `20%` | OKLCH scales, WCAG 2.1 + APCA scores, color-blind safety, pairing & fallbacks |
| **HIG & Geometry** | `15%` | Concentric radius formula, `24×24 dp` icon grid, touch targets, reduced-motion |
| **Governance & DAM** | `20%` | Decision-tree folder hierarchy, required formats/scales, token sync, history log |

- **Release Threshold:** Minimum score **`85/100`** with **zero `FAIL` flags** on Tests 1, 2, or 4.

## 3. Required Output Format

Produce a structured Markdown report saved to `history/brandbook-review-YYYY-MM-DD.md`:

```markdown
# Brandbook Audit Report — {Brand Name}
- **Date:** YYYY-MM-DD
- **Overall Score:** XX/100 — [APPROVED | NEEDS REMEDIATION]

## 6-Test Acceptance Gate
| Test | Status | Finding & Evidence |
|---|---|---|
| 1. Micro-Scale Stress (16px / 80px) | PASS / FAIL | ... |
| 2. Contrast & Gamut (WCAG + APCA) | PASS / FAIL | ... |
| 3. Fallback Typography & Metrics | PASS / FAIL | ... |
| 4. Verbal Identity & Claim Sources | PASS / FAIL | ... |
| 5. Concentric Tokens & Usability | PASS / FAIL | ... |
| 6. Independent Handover & DAM | PASS / FAIL | ... |

## Prioritized Remediation Actions
1. **[CRITICAL]** ...
2. **[MAJOR]** ...
3. **[MINOR]** ...
```
