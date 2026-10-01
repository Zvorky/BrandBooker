---
name: visual-identity
description: >-
  Polices logo construction, mathematical clear space, minimum sizes,
  monochrome rules, co-branding isolation, merchandise limits, and misuse
  catalogs. Use when writing logo guidelines, exclusion zones, partner lockups,
  badge rules, or branded apparel constraints.
---

# Visual Identity

The logo and primary iconography are the irrevocable signature of the brand. Application is never left to operator taste. Police the mark with engineering-grade precision.

## Purpose

Define construction, exclusion zones, minima, co-branding isolation, merchandise limits, and a visual catalog of prohibited misuse.

## Rules

### Clear space (exclusion zone)

Negative space is an **integrity shield**, not emptiness. It protects prominence and legibility against visual pollution.

Base clear space on the mark's intrinsic geometry. Publish diagrams **and** design tokens.

| Parameter | Strict directive |
|-----------|------------------|
| Standard clear space | `0.5 ×` primary symbol height (`X/2`) |
| Secondary badge clear space | `0.25 ×` badge height (when certification/partner badges exist) |
| Minimum digital height | 40 px |
| Minimum print height | 10 mm |
| Constrained hardware surfaces | Clear space may drop to `0.1 ×` height **only** with written approval |
| Monochrome applications | Black 100% (K) or white only |

**Why these numbers:**

- `X/2` prevents optical collision and protects authority
- `X/4` on badges preserves isolation without wasting scarce badge real estate
- 40 px preserves vector integrity across screen densities
- 10 mm prevents ink spread and micrometric detail loss in print
- Mono black/white maximizes contrast under color limits

**Clear space must not be invaded by** photographs, type blocks, outlines, or any layout graphics.

### Minimum sizing

Publish tables for every primary asset (symbol, wordmark, badges):

| Medium | Absolute minimum |
|--------|------------------|
| Digital UI / screens | ≥ 40 px height |
| Print | ≥ 10 mm height |
| Tiny hardware | Exception path only; reduced clear space `H/10` with written approval |

### Co-branding

Excellence includes saying **no**.

- Never combine the primary mark with a partner identity so they read as a **fused signature**
- The logo remains isolated, singular, and unaltered
- Partner marks use separate approved lockups with independent clear space

### Merchandise

| Rule | Directive |
|------|-----------|
| Garment colors | Black, white, and one approved neutral gray only (unless a stricter set is defined) |
| Logo application | Single application only |
| Decorations | No patterns, intricate fabric graphics, or product slogans on apparel |
| Surface bans | No vulgar, disposable, or prestige-misaligned items (paper cups, game chips, generic sports gear, and equivalents) |

Keep merchandise silent and controlled. Strong marks are easily misread when overloaded.

### Prohibition catalog (required)

Ship correct/incorrect pairs for at least:

- Rotation
- Artificial drop shadows
- Unapproved gradients inside the mark
- Complex photographic backgrounds that destroy legibility
- Stretching, condensing, or outlining
- Recoloring outside mono / brand palette rules
- Animation without a dedicated motion spec

From day zero, list **physical surfaces the brand refuses to appear on**.

## Workflow

1. Derive clear space from symbol geometry; tokenize (`logo.clearSpace = 0.5 * logo.height`).
2. Tabulate digital and print minima for every asset.
3. Define co-branding as isolation rules, not collaboration aesthetics.
4. Produce the misuse catalog with paired examples.
5. List banned merchandise categories and surfaces explicitly.

## Deliverables

- Construction grid / proportion notes for the primary mark
- Clear-space formula + tokens
- Min-size tables (digital, print, hardware exception)
- Co-branding isolation rules
- Merchandise color and application limits
- Banned surfaces list
- Visual misuse catalog (correct vs incorrect)

## Checklist

```
Visual identity chapter:
- [ ] Clear-space formula documented and tokenized
- [ ] Badge clear-space rule included if badges exist
- [ ] Digital and print minima tabulated
- [ ] Hardware exception path defined
- [ ] Mono rules (black / white) stated
- [ ] Co-branding isolation rules
- [ ] Merchandise color + single-application limits
- [ ] Banned surfaces / item types
- [ ] Visual misuse catalog with pairs
```

## Forbidden

- Operator taste overriding documented geometry
- Fused partner signatures
- Unapproved color fills, effects, or distortions
- Logo on banned surfaces
- Shipping guidelines without a prohibition gallery
