---
name: human-interface
description: Governs digital product ergonomics, concentric border-radius mathematics, G3 squircles, 24x24 dp icon grids and keylines, elevation, safe areas, motion, and haptics. Use when specifying UI rules, web design tokens, component geometry, or icon systems in a brandbook.
---

# Human Interface Guidelines (HIG)

Digital interfaces act as a quiet, deterministic stage for user intent—governed by **Clarity**, **Deference**, and **Depth**.

## 1. Concentric Border-Radius Mathematics

Nested rounded containers (cards containing buttons, images, badges, or inputs) look visibly distorted at `45°` when inner and outer elements share the same `border-radius`: the diagonal gap widens while the inner corner appears pinched.

### Mandatory Concentric Formula
To keep inner and outer arcs strictly parallel with a shared geometric center:

$$R_{\text{inner}} = \max\left(0,\; R_{\text{outer}} - (\text{padding} + \text{border\_width})\right)$$

- **Example:** A card with `R_outer = 24px`, `border = 1px`, and `padding = 11px` requires `R_inner = 12px` (`24 - 11 - 1 = 12px`).
- **CSS Token Implementation:** Expose `--radius-outer`, `--shell-padding`, and `--shell-border`, computing `--radius-inner: max(0px, calc(var(--radius-outer) - var(--shell-padding) - var(--shell-border)))`.
- **Dimensional Cap:** Keep every radius `<= 50%` of the box's shortest side (except full pill shapes, which use `9999px`).
- **Independence Threshold:** When `padding > 24px`, inner elements behave as independent surfaces and are exempt from strict concentric coupling.
- **Sharp Inner Fallback & G3 Squircles:** When `border_width` approaches `R_outer`, a sharp `0px` inner corner reads cleaner than a tiny micro-arc. On flagship hardware/app surfaces, prefer continuous curvature transitions (**G3 squircles** / clothoid approximations) over abrupt circular arcs.

## 2. Iconography Grid & Perceptual Mass Equalization

Brand icon sets must operate as a unified visual alphabet with identical stroke weight, corner logic, and perceived mass:

- **Standard Grid:** Construct system/UI icons on a **`24×24 dp` (or `px`) grid** with an interior **`20×20 dp` live area**, preserving a **`2 dp` perimeter trim** on all four sides to prevent edge clipping.
- **Perceptual Mass Keylines:** Never fill the entire `20×20` square with square icons—a solid square appears significantly heavier than a circle or vertical rectangle of the same bounding box. Use canonical keylines (circle, square, vertical rectangle, horizontal rectangle) to equalize optical weight across the set.
- **Pixel-Grid Alignment & Concentric Details:** Snap straight strokes to whole-pixel boundaries for crisp rendering and apply the concentric radius formula to nested icon strokes.
- **Optical Centering:** Offset directional icons (play triangles, right arrows, chevrons) toward their visual mass center inside circular or square button containers.

## 3. Core Digital Ergonomics

- **Clarity:** Text is legible at every viewing distance (`>= 16px` base body on mobile/desktop), icons are unambiguous, and layout hierarchy relies on spacing and weight—not decorative borders.
- **Deference:** Content occupies the full viewport (`min-h-[100dvh]`, never brittle `100vh`); chrome, headers, and translucent surfaces stay subtle and never compete with primary tasks.
- **Depth:** Visual layers and restrained elevation communicate hierarchy and spatial origin without heavy drop shadows.
- **Purposeful Motion & Reduced-Motion Respect:** Transitions explain spatial state changes (`150ms–280ms`, `cubic-bezier(0.2, 0, 0, 1)`) and never block input. Always honor `@media (prefers-reduced-motion: reduce)`.
- **Touch Targets & Safe Areas:** Enforce `>= 44×44 px` touch targets with `>= 8px` separation and respect `env(safe-area-inset-*)` on mobile viewports.
