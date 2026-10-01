---
name: color-typography
description: >-
  Engineers restrained color hierarchies, WCAG-safe semantic color, display/
  text/mono type roles, and modular spacing tokens. Use when defining palettes,
  contrast rules, typography systems, leading, or spacing scales for a brand.
---

# Color & Typography

Indiscriminate color dilutes institutional impact. Sophisticated systems run under severe chromatic restriction. Typography is the most prominent element users read—and the silent foundation of brand voice.

## Purpose

Define a hierarchical palette, accessibility-safe semantic color, strict type roles, and a modular spacing scale—all as tokens.

## Rules

### Color hierarchy

1. **Neutrals first** — refined spectrum from polar white to deep charcoal; focus stays on product and content.
2. **Spatial proportions** — stricter than classic 60-30-10:
   - **80%** neutral / negative space
   - **15%** secondary structural elements
   - **≤5%** accent to guide attention
3. **One primary action color** — CTAs and isolated highlight moments only; **forbidden** as body-text color.
4. **One secondary** (optional) — structural support only.
5. **Semantic feedback** — success, danger, warning, info; target **WCAG AAA** contrast where feasible; never rely on hue alone.

### Accent restraint

If a vibrant accent exists, use it with extreme sparseness—for support, assurance, and delight at critical moments—not as ambient fill.

### Accessibility

If a pair fails contrast requirements, **do not force approval**. Adjust the color until legibility is met. Prefer modular semantic variables over ad-hoc hex values.

### Color tokens

```
color.primary            → CTAs / isolated emphasis only
color.secondary          → structural support
color.accent             → rare highlight moments
color.neutral.0-6        → refined grayscale spectrum
color.feedback.success
color.feedback.danger
color.feedback.warning
color.feedback.info
```

Expand neutrals and feedback ramps as needed; keep **jobs** semantic. Resist decorative free colors outside this map.

### Type roles

| Role | Context | Structural rules |
|------|---------|------------------|
| Display | Headlines, advertising, key conversion moments | Fits a rigid grid. No mechanical condensation. No false italics. |
| Text / Body | Technical copy, product descriptions, UI reading | Accessibility-aligned; support system text scaling. Leading ≥ **150%** of font size. |
| Mono (Technical) | Specs, numeric IDs, metadata | Black, gray, or pure white only. Signals precision in dense data. |

### Family discipline

Resist a third type family unless a structural use case cannot be met by the primaries. Random families accumulate into visual noise.

Prefer optical sizes that scale from tiny hardware readouts to large panels. Separate Display vs Text cuts when available; never use Display for long reading.

### Modular spacing

Spacing is a fixed coordinate in brand code—not a style suggestion.

| Rule | Directive |
|------|-----------|
| Margins, padding, gaps | Scalar increment system only |
| Random values | Prohibited |
| Example base scale | 4 / 8 / 16 / 24 / 32 / 48 / 64 (px or rem equivalent) |

## Workflow

1. Build palette from neutrals outward; introduce accent last and sparsely.
2. Assign every color a semantic job; ban free decorative use of primary.
3. Lock type to Display / Text / Mono; ban false italics and forced distortion.
4. Set body leading floor at 150%; require system text-scaling support.
5. Tokenize spacing on one base grid; reject one-off values in review.

## Deliverables

- Neutral spectrum + primary / secondary / accent roles
- Feedback colors with contrast targets
- Token map (color + type styles + spacing)
- Type role table with Do/Don't
- Spacing scale definition

## Checklist

```
Color & type chapter:
- [ ] Neutral foundation defined
- [ ] 80 / 15 / 5 (or documented equivalent) proportion rule
- [ ] Primary CTA color restricted; banned in body text
- [ ] Semantic feedback colors + contrast targets
- [ ] Display / Text / Mono roles specified
- [ ] False italics and mechanical distortion banned
- [ ] Leading ≥ 150% for body
- [ ] System text-scaling support stated
- [ ] Modular spacing scale tokenized
- [ ] Third-family policy (resist by default)
```

## Forbidden

- Rainbow palettes without semantic jobs
- Primary color as paragraph text
- Forced contrast exceptions
- False italics / stretched type
- One-off spacing values outside the scale
- A third family without a proven structural need
