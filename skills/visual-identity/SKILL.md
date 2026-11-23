---
name: visual-identity
description: >-
  Governs brand marks, vector/Bezier engineering, optical compensations,
  wordmark anatomy, supergraphics, responsive lockups, clear space, minimum
  sizes, co-branding, merchandise limits, and misuse bans. Use when creating,
  refining, auditing, or documenting logos, SVGs, wordmarks, or brand mark
  applications.
---

# Visual Identity & Vector Engineering

The brand mark is the geometric matrix of the entire identity system, never an isolated stamp. Proportions, cut angles, curves, and grid modules extracted from the mark govern supergraphics, iconography, layout framing, and motion.

## Purpose

Define vector path hygiene, optical compensations, wordmark craft, supergraphics, responsive lockups, clear space, minimum sizes, co-branding isolation, merchandise limits, and forbidden misuse rules.

## Rules

### 1. Vector & Bezier Engineering Standards
Every vector mark and inline SVG must pass structural path hygiene before release:
1. **Zero-Handle Elimination:** Every curved segment sits between two on-curve nodes and must possess two distinct off-curve Bezier control points belonging to the segment. Never collapse a handle onto an adjacent node coordinate (*zero handle* / dead curve).
2. **Magic Triangle Rule:** A curved segment must remain entirely inside the triangle formed by its two end nodes and the intersection of the tangent extensions of its two handles. Handles must never cross each other or the opposite handle's tangent line (prevents kinks, cusps, and self-intersections during rasterization).
3. **Orthogonal Extrema Nodes:** Place on-curve nodes at the horizontal and vertical extrema of curves with handles aligned orthogonally (`0 deg` or `90 deg`). Exception: omit extrema nodes on shallow curves (only a few units deep) where integer rounding causes flat distortion.
4. **Handle Proportion Calibration:** Maintain balanced handle lengths across opposing nodes: typically `55%-56%` of the bounding-box corner distance for geometric circles/ellipses, and `~58%-72%` for high-precision typographic and brand curves.
5. **Inflection Point Discipline:** Keep each curved segment single-sided (clockwise or counter-clockwise). When curvature reverses (e.g., an `S` curve or tilde), place a node at the inflection point unless orthogonal handles resolve it cleanly.
6. **G2 Curvature Continuity:** Adjacent curved segments must match their second geometric derivative (curvature rate) at the shared node so transitions flow without visual bumps, not merely share a linear tangent.
7. **Stray Point & Bounds Cleanup:** Purge stray anchor points, empty groups, and invisible path debris outside the artboard bounds before exporting.

### 2. Optical Compensations (Eye Over Pure Math)
Pure mathematical symmetry creates perceptual errors. Apply four mandatory optical corrections inherited from type and icon design:

| Optical Phenomenon | Pure Geometry Failure | Mandatory Correction |
|---|---|---|
| **Optical vs. Geometric Center** | A play triangle or directional arrow centered mathematically inside a circle/button appears shifted left; centered text blocks look low. | Shift asymmetric shapes toward their visual mass center (e.g., `+2px` right for play triangles in UI) and lift optical baselines slightly above mathematical center. |
| **Overshoot** | Circles, arches, and pointed vertices sharing the exact numerical cap-height/baseline of flat squares appear smaller. | Extend rounded curves and acute apexes slightly past the cap-line and baseline (`~1.5%-3%`) to equalize perceived height. |
| **Stroke Contrast & Joins** | Horizontal bars equal in numerical thickness to vertical stems look heavier; stroke intersections accumulate dark visual weight. | Draw horizontal strokes slightly thinner than vertical stems and subtly taper/recess counterforms into vertical stems at joins. |
| **Ink Traps** | Acute angles and dense stroke intersections visually clog or blur at small screen sizes and in print. | Carve controlled notches/openings at acute stroke junctions to preserve crisp vertex definition. |

### 3. Wordmark Anatomy & Typographic Craft
- **Never Stretch or Compress:** Mechanical horizontal or vertical scaling of a font is strictly forbidden because it destroys stem-to-crossbar contrast. Use native `condensed`, `expanded`, or variable-axis widths.
- **Surgical Glyph Customization:** Convert wordmark glyphs to vector outlines and introduce deliberate anatomical distinction in **1 or 2 key characters** (e.g., custom terminal angle, crossbar cut, or counter) without compromising legibility.
- **Ligature Restraint:** Use at most **one** custom ligature on natural pairs (`AV`, `TH`, `LA`, `ST`, `RN`). Over-linking turns the brand name into an illegible puzzle at small sizes.
- **Manual Optical Kerning:** Kern pair-by-pair (especially `AV`, `To`, `Wa`, `LT`) until negative-space volume between every letter appears uniform.

### 4. Supergraphics & Systemic Unification
- Extract structural motifs from the primary mark (cut angles, curve intersections, emblem contours, or base grid modules) to construct **supergraphics**, patterns, framing masks, data-visualization accents, and motion transitions.
- A surface must remain unmistakably attributable to the brand through its graphic language even when the primary logo is absent.

### 5. Responsive Mark Architecture, Clear Space & Minima
Deploy a four-tier responsive mark system governed by measurable clear space and hard minimum-size floors:

| Responsive Variant | Minimum Clear Space | Minimum Size Floor (Digital / Print) | Deployment Context |
|---|---|---|---|
| **Full Lockup (with tagline)** | `1.5x - 2x` (measured by x-height or primary grid module) | `120 px` width / `35 mm` width | Hero headers, covers, primary institutional surfaces |
| **Stacked Lockup** | `1x - 1.5x` (increased vertical buffer) | Governed by internal legibility floor | Square containers, cards, vertical formats |
| **Isolated Logomark (Symbol)** | `0.5x - 1x` from outermost visible contour | `24 px` width / `15 mm` width | Compact UI headers, badges, social avatars |
| **Favicon / Micro-Scale** | Fixed pixel grid (proportional rules fail at micro scale) | `16x16 px` single solid color | Browser tabs, app icons, micro-indicators |

#### Mandatory Color Variants
Every applicable mark tier must ship in four chromatic states:
1. **Primary Polychromatic** (standard brand background)
2. **Monochrome Black / Dark** (single-ink print, embossing, light surfaces)
3. **Monochrome White / Light** (dark surfaces, photography overlays)
4. **Inverted** (high-contrast dark-mode primary lockup)

### 6. Co-Branding, Merchandise & Misuse Prohibitions
- **Co-Branding Separation:** Never fuse partner marks into a hybrid logo. Separate co-branded signatures with a vertical hairline (`1px` or `0.5pt`) enforcing full clear space on both sides, keeping visual weight balanced.
- **Merchandise Restraint:** Restrict garments to black, white, and one approved neutral gray (unless a stricter set is defined), allow a single logo application, forbid patterns/slogans on apparel, and ban vulgar, disposable, or prestige-misaligned surfaces.
- **Catalog of Forbidden Uses:**
  1. Non-orthogonal rotation or skewing of the mark.
  2. Drop shadows, outer glows, bevel/emboss filters, or unauthorized multi-stop gradients.
  3. Re-coloring individual letters or fragments in ways that break sigla recognition.
  4. Mechanical stretching/squashing of aspect ratio.
  5. Placement over uncalibrated photography where contrast drops below `4.5:1` (`WCAG AA`).
  6. Placing the full lockup below `120 px` / `35 mm` instead of switching to the isolated logomark or micro-scale variant.

## Workflow

1. Verify Bezier path hygiene (7 rules) and apply required optical compensations.
2. Build wordmark hierarchy and responsive mark tiers with clear-space and minimum-size floors.
3. Define supergraphic motifs, co-branding separation rules, merchandise limits, and misuse examples.

## Deliverables

- Clean vector marks (`SVG`/`PDF`/`EPS`) and optical compensation notes
- Responsive mark, clear-space, and minimum-size specification table
- Co-branding, merchandise, and forbidden-use catalog

## Checklist

```text
Visual identity chapter:
- [ ] Zero-handle, Magic Triangle, extrema, handle ratio, inflection, G2, and cleanup rules applied
- [ ] Optical center, overshoot, stroke contrast/joins, and ink traps addressed
- [ ] Wordmark custom glyphs, ligature restraint, and kerning defined without font stretching
- [ ] Responsive tiers, clear space, and minimum sizes documented
- [ ] Co-branding, merchandise limits, and misuse prohibitions documented
```

## Forbidden

- Zero-handle curves, uncompensated nested radii, or mechanical font stretching
- Fused partner marks or unauthorized drop shadows/gradients on the mark
- Merchandise on vulgar, disposable, or prestige-misaligned surfaces
