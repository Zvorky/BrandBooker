---
name: color-typography
description: >-
  Governs perceptual color systems (OKLCH/LCh/CIELAB), print gamut management
  (CMYK/Pantone Coated & Uncoated), 80/15/5 chromatic balance, WCAG 2.1 + APCA
  contrast auditing, color-blindness safety, modular spacing scales, and
  functional typography pairing. Use when defining brand palettes, color tokens,
  tonal ramps, spacing scales, or typographic hierarchies.
---

# Color & Typography Systems

Color and type must translate brand doctrine into deterministic tokens that hold perceptual uniformity on high-DPI screens and predictable pigment fidelity in print.

## Purpose

Define perceptual digital palettes, print gamut rules, accessibility contrast targets, spacing scales, and functional typographic roles as enforceable tokens.

## Rules

### 1. Perceptual Color Architecture (Digital & Print)
- **Author in `OKLCH` / `LCh` / `CIELAB`:** Build tonal ramps (`50`-`950`) in perceptually uniform color spaces (`OKLCH`: Lightness `L`, Chroma `C`, Hue `H`) before exporting to `HEX` and `RGB`. Never generate ramps via naive HSL lightness shifts, which cause perceived brightness spikes in yellows/cyans and muddiness in blues.
- **Chromatic Balance (`80 / 15 / 5`) & Surface Hierarchy:** Anchor layouts around `~80%` neutral/negative space, `~15%` secondary structural elements, and `<= 5%` accent. Reserve primary action color for CTAs and isolated emphasis (never body text), and define semantic tokens (`--bg-canvas`, `--surface-primary`, `--surface-elevated`, `--border-subtle`, `--text-primary`, `--text-secondary`, `--accent-primary`) instead of raw hex lists.
- **Ban Pure Void Black (`#000000`) for Surfaces:** Use calibrated deep neutral tones (`L: 10%-16%`) to prevent halation and harsh contrast fatigue unless hardware OLED constraints explicitly dictate true black.
- **Print & Gamut Management (`CMYK` & `Pantone PMS`):** Specify separate calibrated values for **Coated (`C`)** and **Uncoated (`U`)** paper stocks. Flag vibrant digital colors that fall **out of CMYK gamut** and prescribe spot **Pantone (PMS)** inks, Expanded Gamut (**OGV**), or recalibrated CMYK builds.

### 2. Dual Accessibility Auditing (`WCAG 2.1` + `APCA`)
Every foreground/background token pair must pass both legacy ratio checks and modern perceptual contrast:

| Role | WCAG 2.1 Minimum (AA / AAA) | APCA (`Lc`) Target |
|---|---|---|
| **Body Copy (`< 18pt`)** | `4.5:1` (AA) / `7.0:1` (AAA) | `Lc >= 60` (preferred `Lc 75+`) |
| **Large Headings (`>= 18pt` or `14pt bold`)** | `3.0:1` (AA) / `4.5:1` (AAA) | `Lc >= 45` |
| **UI Components, Borders & Focus Rings** | `3.0:1` (AA) | `Lc >= 30` (non-text structural) |

- **Color-Blindness Safety (~5% Global Population):** Never rely on hue alone to communicate status or hierarchy. Avoid overlapping high-risk pairs (**red/green**, **red/black**, **blue/yellow**) without a strong luminance (`L`) delta (`Delta L >= 35` in OKLCH). Prefer safer high-contrast pairings such as **blue + orange/amber** for critical differentiation.

### 3. Functional Typography Pairing, Roles & Modular Spacing
Limit the brand system to **two font families** (one expressive display/wordmark family + one utility/body family), assigning explicit **Display**, **Text/Body**, and **Mono** roles.

| Primary Wordmark / Display Style | Recommended Secondary Utility Font | Strategic & Visual Rationale |
|---|---|---|
| **High-Contrast Serif** (e.g., Bodoni, Didot) | Neutral Neo-Grotesque Sans (uppercase with open tracking for labels) | Serif carries emotional authority; neutral sans guarantees technical utility and clean UI legibility. |
| **Heavy Geometric Sans-Serif** | Light weight of the **same** geometric family (with generous kerning) | Preserves strict formal unity while establishing clear weight hierarchy. |
| **Calligraphic / Hand-Drawn Script** | Structured Monospace or clean humanist sans (stroke-weight matched) | Balances organic human expression with engineering rigor and visual stability. |
| **Robust Slab Serif** | Light, open modern sans-serif | Prevents visual congestion by contrasting heavy slab terminals with airy letterforms. |

- **System Fallback Metrics:** Every web font must declare a matched system fallback stack with calibrated `@font-face` metric overrides (`size-adjust`, `ascent-override`, `descent-override`) to eliminate Cumulative Layout Shift (CLS).
- **Body Leading, Measure & `tabular-nums`:** Keep body line-height (`leading`) at `>= 150%` of font size, constrain body prose width to `55-72` characters (`max-width: 65ch`), forbid fake/synthesized italics or bolds (`font-synthesis: none`), and enforce `font-variant-numeric: tabular-nums` on pricing, tables, telemetry, and financial readouts.
- **Modular Spacing Scale:** Use a scalar spacing system (e.g., `4 / 8 / 16 / 24 / 32 / 48 / 64` px or `rem` equivalent) and reject arbitrary one-off spacing values.

## Workflow

1. Build tonal color ramps in `OKLCH` and map `CMYK`/`Pantone` Coated and Uncoated equivalents.
2. Validate all foreground/background pairs against `WCAG 2.1` and `APCA`, checking color-blind luminance separation.
3. Lock Display, Text/Body, and Mono roles, `@font-face` fallback metrics, `tabular-nums`, and modular spacing tokens.

## Deliverables

- `OKLCH` and `CMYK`/`Pantone` color token specification with `WCAG 2.1` + `APCA` audit table
- Type role, pairing, fallback `@font-face`, and modular spacing token specification

## Checklist

```text
Color & typography chapter:
- [ ] OKLCH ramps and 80/15/5 chromatic roles defined
- [ ] CMYK / Pantone Coated & Uncoated values and out-of-gamut handling documented
- [ ] WCAG 2.1 and APCA contrast targets and color-blind luminance checks passed
- [ ] Display / Text / Mono roles, fallback metrics, tabular-nums, and modular spacing tokenized
```

## Forbidden

- Naive HSL lightness ramps or pure `#000000` backgrounds without justification
- Primary accent color used for body copy or unverified contrast pairs
- Mechanical font stretching, synthesized italics (`font-synthesis: none` violated), or ad-hoc spacing values
