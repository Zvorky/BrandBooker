---
name: human-interface
description: >-
  Governs digital product ergonomics, concentric border-radius mathematics, G3
  squircles, 24x24 dp icon grids and keylines, elevation, translucency,
  safe areas, motion, haptics, and accessible reflow. Use when specifying UI
  rules, web design tokens, component geometry, or icon systems in a brandbook.
---

# Human Interface Guidelines (HIG)

Digital interfaces act as a quiet, deterministic stage for user intent, governed by **Clarity**, **Deference**, and **Depth**.

## Purpose

Specify geometric nesting, iconography grids, elevation/translucency limits, motion, haptics, and reflow rules for digital interfaces.

## Rules

### 1. Concentric Border-Radius Mathematics
Nested rounded containers (cards containing buttons, images, badges, or inputs) look visibly distorted at `45 deg` when inner and outer elements share the same `border-radius`: the diagonal gap widens while the inner corner appears pinched.

- **Mandatory Concentric Formula:** To keep inner and outer arcs strictly parallel with a shared geometric center:

$$R_{\text{inner}} = \max\left(0,\; R_{\text{outer}} - (\text{padding} + \text{border\_width})\right)$$

- **Example:** A card with `R_outer = 24px`, `border = 1px`, and `padding = 11px` requires `R_inner = 12px` (`24 - 11 - 1 = 12px`).
- **CSS Token Implementation:** Expose `--radius-outer`, `--shell-padding`, and `--shell-border`, computing `--radius-inner: max(0px, calc(var(--radius-outer) - var(--shell-padding) - var(--shell-border)))`.
- **Dimensional Cap:** Keep every radius `<= 50%` of the box's shortest side (except full pill shapes, which use `9999px`).
- **Independence Threshold:** When `padding > 24px`, inner elements behave as independent surfaces and are exempt from strict concentric coupling.
- **Sharp Inner Fallback & G3 Squircles:** When `border_width` approaches `R_outer`, a sharp `0px` inner corner reads cleaner than a tiny micro-arc. On flagship hardware/app surfaces, prefer continuous curvature transitions (**G3 squircles** / clothoid approximations) over abrupt circular arcs.

### 2. Iconography Grid & Perceptual Mass Equalization
Brand icon sets must operate as a unified visual alphabet with identical stroke weight, corner logic, and perceived mass:

- **Standard Grid:** Construct system/UI icons on a **`24x24 dp` (or `px`) grid** with an interior **`20x20 dp` live area**, preserving a **`2 dp` perimeter trim** on all four sides to prevent edge clipping.
- **Perceptual Mass Keylines:** Never fill the entire `20x20` square with square icons because a solid square appears significantly heavier than a circle or vertical rectangle of the same bounding box. Use canonical keylines (circle, square, vertical rectangle, horizontal rectangle) to equalize optical weight across the set.
- **Pixel-Grid Alignment & Concentric Details:** Snap straight strokes to whole-pixel boundaries for crisp rendering and apply the concentric radius formula to nested icon strokes.
- **Optical Centering:** Offset directional icons (play triangles, right arrows, chevrons) toward their visual mass center inside circular or square button containers.

### 3. Core Digital Ergonomics, Motion, Haptics & Reflow
- **Clarity:** Text is legible at every viewing distance (`>= 16px` base body on mobile/desktop), icons are unambiguous, and layout hierarchy relies on spacing and weight rather than decorative borders.
- **Deference:** Content occupies the full viewport (`min-h-[100dvh]`, never brittle `100vh`); chrome, headers, and translucent surfaces stay subtle and never compete with primary tasks.
- **Depth, Elevation & Translucency:** Use restrained Z-axis elevation and capped blur/translucency so background context stays readable without heavy drop shadows or excessive blur.
- **Purposeful Motion & Reduced-Motion Respect:** Transitions explain spatial state changes (`150ms-280ms`, `cubic-bezier(0.2, 0, 0, 1)`) and never block input. Always honor `@media (prefers-reduced-motion: reduce)`.
- **Haptics & Reflow:** Restrict haptics to culminating interaction moments (never routine navigation), enforce `>= 44x44 px` touch targets with `>= 8px` separation, respect `env(safe-area-inset-*)`, and ensure flexible layouts reflow cleanly when system text scales up.

## Workflow

1. Define Clarity, Deference, and Depth rules along with concentric radius and `24x24 dp` icon grid specs.
2. Specify elevation/translucency caps, motion curves, haptic limits, safe areas, and large-text reflow behavior.

## Deliverables

- Concentric radius and `24x24 dp` icon grid specification
- Ergonomics, elevation/translucency, motion, haptics, and reflow rules

## Checklist

```text
Human interface chapter:
- [ ] Concentric radius formula and CSS token / exception rules defined
- [ ] 24x24 dp icon grid, 20x20 dp live area, and perceptual mass keylines specified
- [ ] Clarity, Deference, Depth, translucency caps, and safe areas addressed
- [ ] Purposeful motion, prefers-reduced-motion, haptics limits, and text reflow verified
```

## Forbidden

- Uncompensated nested corner radii or brittle `100vh` full-height locks
- Decorative/delaying animations or routine navigation haptic spam
- Interactive targets clipping safe areas or breaking under system text scaling
