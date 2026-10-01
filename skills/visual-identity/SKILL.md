---
name: visual-identity
description: >-
  Polices logo construction, clear space, minimum sizes, co-branding, and
  merchandise. Use when writing logo guidelines, exclusion zones, misuse
  catalogs, partner lockups, or branded apparel rules.
---

# Visual Identity

The logo and primary iconography are the irrevocable signature of the brand. Application is not left to operator taste. Document aggressive visual policing with engineering-grade precision.

## Clear Space (Exclusion Zone)

Negative space is not emptiness—it is an **integrity shield** that preserves prominence and legibility against visual pollution.

### Default formula

Base clear space on the mark’s intrinsic geometry. Provide both diagrams and **design tokens**.

| Parameter | Strict directive |
|-----------|------------------|
| **Standard clear space** | 50% of the primary symbol’s vertical dimension (`X/2`) |
| **Minimum digital height** | 40 px |
| **Minimum print height** | 10 mm |
| **Constrained surfaces (hardware only)** | Exceptional clear space of `1/10` height — requires strict approval |
| **Monochrome applications** | Black 100% (K) or white only |

Rationale encoded for agents:

- `X/2` prevents optical collision and protects authority
- 40 px preserves sub-pixel integrity of vector forms across densities
- 10 mm prevents ink spread and micrometric detail loss in offset/screen printing
- Monochrome black/white preserves maximum contrast under color limits

### Clear space must not be invaded by

Photographs, type blocks, outlines, or any layout graphics.

## Minimum Sizing Tables

Publish technical tables for every primary asset (mark, wordmark, badges):

| Medium | Absolute minimum |
|--------|------------------|
| Digital UI / screens | ≥ 40 px height (adjust only with density-aware review) |
| Print | ≥ 10 mm height |
| Tiny hardware | Exception path only; reduced clear space `H/10` with written approval |

## Co-Branding

Excellence is measured by the ability to say **no**.

- Never visually combine the primary mark with a partner name/identity so they read as a **fused signature**
- The logo remains **isolated, singular, and unaltered**
- Partner marks sit in separate approved lockup structures with independent clear space

## Merchandise Governance

For apparel and physical brand goods:

| Rule | Directive |
|------|-----------|
| Garment colors | Strictly limited (e.g. black, white, and one approved neutral gray) |
| Logo application | Single application only |
| Decorations | No superfluous patterns, intricate fabric graphics, or product slogans on apparel |
| Surface bans | Prohibit vulgar, disposable, or prestige-misaligned items (e.g. paper cups, game chips, generic sports gear) |

Misinterpretation risk is high when the parent mark is strong—keep merchandise silent and controlled.

## Catalog of Prohibitions

Mandate a visual “don’t” gallery covering at least:

- Rotating the logo
- Adding artificial drop shadows
- Filling the mark with unapproved gradients
- Placing the mark on complex photographic backgrounds that destroy legibility
- Stretching, condensing, or outlining the mark
- Recoloring outside the approved mono / brand palette rules
- Animating the mark without a dedicated motion spec

From day zero, define **physical surfaces the brand refuses to appear on**.

## Agent Instructions

1. Derive clear space from the symbol’s own geometry; express as tokens (`logo.clearSpace = 0.5 * logo.height`).
2. Ship min-size tables for digital and print.
3. Write co-branding as isolation rules, not collaboration aesthetics.
4. Produce a misuse catalog with correct vs incorrect pairs.
5. List banned merchandise categories explicitly.

## Checklist

```
Visual identity chapter:
- [ ] Clear-space formula documented + tokenized
- [ ] Digital and print minima tabulated
- [ ] Constrained-surface exception path defined
- [ ] Mono rules (black / white) stated
- [ ] Co-branding isolation rules
- [ ] Merchandise color + application limits
- [ ] Banned surfaces / item types
- [ ] Visual misuse catalog
```
