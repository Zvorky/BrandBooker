---
name: color-typography
description: Governs perceptual color systems (OKLCH/LCh/CIELAB), print gamut management (CMYK/Pantone Coated & Uncoated), WCAG 2.1 + APCA contrast auditing, color-blindness safety, and functional typography pairing. Use when defining brand palettes, color tokens, tonal ramps, or typographic hierarchies.
---

# Color & Typography Systems

Color and type must translate brand doctrine into deterministic tokens that hold perceptual uniformity on high-DPI screens and predictable pigment fidelity in print.

## 1. Perceptual Color Architecture (Digital & Print)

### Digital Color Spaces (`OKLCH` First)
- **Author in `OKLCH` / `LCh` / `CIELAB`:** Build tonal ramps (`50`–`950`) in perceptually uniform color spaces (`OKLCH`: Lightness `L`, Chroma `C`, Hue `H`) before exporting to `HEX` and `RGB`. Never generate ramps via naive HSL lightness shifts, which cause perceived brightness spikes in yellows/cyans and muddiness in blues.
- **Surface Hierarchy:** Define explicit semantic tokens (`--bg-canvas`, `--surface-primary`, `--surface-elevated`, `--border-subtle`, `--text-primary`, `--text-secondary`, `--accent-primary`) rather than raw hex lists.
- **Ban Pure Void Black (`#000000`) for Surfaces:** Use calibrated deep neutral tones (`L: 10%–16%`) to prevent halation and harsh contrast fatigue unless hardware OLED constraints explicitly dictate true black.

### Print & Gamut Management (`CMYK` & `Pantone PMS`)
- Specify separate calibrated values for **Coated (`C`)** and **Uncoated (`U`)** paper stocks—ink absorption alters saturation and value significantly on uncoated stock.
- Flag vibrant digital colors that fall **out of CMYK gamut** (which print dull, dark, or greyish) and prescribe either spot **Pantone (PMS)** inks, Expanded Gamut (**OGV**), or manually recalibrated CMYK builds.

## 2. Dual Accessibility Auditing (`WCAG 2.1` + `APCA`)

Every foreground/background token pair must pass both legacy ratio checks and modern perceptual contrast:

| Role | WCAG 2.1 Minimum (AA / AAA) | APCA (`Lc`) Target |
|---|---|---|
| **Body Copy (`< 18pt`)** | `4.5:1` (AA) / `7.0:1` (AAA) | `Lc >= 60` (preferred `Lc 75+`) |
| **Large Headings (`>= 18pt` or `14pt bold`)** | `3.0:1` (AA) / `4.5:1` (AAA) | `Lc >= 45` |
| **UI Components, Borders & Focus Rings** | `3.0:1` (AA) | `Lc >= 30` (non-text structural) |

### Color-Blindness Safety (~5% Global Population)
- Never rely on hue alone to communicate status or hierarchy.
- Avoid overlapping high-risk pairs (**red/green**, **red/black**, **blue/yellow**) without a strong luminance (`L`) delta (`ΔL >= 35` in OKLCH). Prefer safer high-contrast pairings such as **blue + orange/amber** for critical differentiation.

## 3. Functional Typography Pairing & Hierarchy

Limit the brand system to **two font families** (one expressive display/wordmark family + one highly legible utility/body family), calibrating optical sizes so stroke weights harmonize across transitions.

### Functional Pairing Matrix

| Primary Wordmark / Display Style | Recommended Secondary Utility Font | Strategic & Visual Rationale |
|---|---|---|
| **High-Contrast Serif** (e.g., Bodoni, Didot) | Neutral Neo-Grotesque Sans (uppercase with open tracking for labels) | Serif carries emotional authority; neutral sans guarantees technical utility and clean UI legibility. |
| **Heavy Geometric Sans-Serif** | Light weight of the **same** geometric family (with generous kerning) | Preserves strict formal unity while establishing clear weight hierarchy. |
| **Calligraphic / Hand-Drawn Script** | Structured Monospace or clean humanist sans (stroke-weight matched) | Balances organic human expression with engineering rigor and visual stability. |
| **Robust Slab Serif** | Light, open modern sans-serif | Prevents visual congestion by contrasting heavy slab terminals with airy letterforms. |

### Typographic Governance Rules
- **System Fallback Metrics:** Every web font must declare a matched system fallback stack with calibrated `@font-face` metric overrides (`size-adjust`, `ascent-override`, `descent-override`) to eliminate Cumulative Layout Shift (CLS).
- **Tabular Figures (`tabular-nums`):** Enforce `font-variant-numeric: tabular-nums` on all pricing tables, calculators, telemetry, and financial readouts.
- **Line Measure & Rhythm:** Constrain body prose width to `55–72` characters (`max-width: 65ch`) and forbid fake/synthesized italics or bolds (`font-synthesis: none`).
