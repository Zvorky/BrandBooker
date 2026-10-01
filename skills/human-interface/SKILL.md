---
name: human-interface
description: >-
  Defines human interface guidelines for digital products: clarity, deference,
  depth, motion, haptics, and accessible layout. Use when writing HIG chapters,
  auditing UI behavior, or specifying interaction, elevation, and safe areas.
---

# Human Interface Guidelines

Aesthetic rules alone (logo and color) are insufficient for technology products. The brandbook must include human interface guidelines so every digital interaction feels fluid, instinctive, and native—avoiding confusion and cognitive fatigue.

## Three Pillars

### 1. Clarity

Everything on screen must have precise, immediate, unambiguous meaning.

- Typography legibility outranks artistic flourish
- Icons stay clean and geometrically focused—no second interpretations
- Remove any ornament that does not directly help complete a task
- Design in **points**, not absolute device pixels, so UI scales correctly across `@1x` / `@2x` / `@3x` densities

### 2. Deference

The UI is not the protagonist. It is an invisible scaffold that supports, interacts with, and elevates content (imagery, data, text).

- Navigation bars, tabs, and modals should fuse with structure
- Prefer subtle blur or minimal translucency over aggressive opaque overlays that compete for attention
- Respect **safe areas**: no primary interactive element may collide with or hide behind notches, home indicators, or rounded screen corners

### 3. Depth

In a 2D environment, the brain needs signals for spatial position and information hierarchy. Depth is not skeuomorphic nostalgia—it is controlled perspective and digital material properties that create logical layers.

Regulate physically:

| Property | Mandate |
|----------|---------|
| **Shadows & elevation** | Fixed Z-axis shadow recipes (blur, opacity) that mimic real light; signal what is tappable/pushable |
| **Translucency** | Frosted materials keep hierarchical context when menus overlay content; **cap blur thresholds**—excess harms usability |

## Motion

System motion is not cosmetic charm.

**Allowed when it:**

- Explains a state change
- Confirms a successful transaction
- Responds to a human gesture with physically plausible momentum

**Prohibited when it:**

- Delays the natural pace of task completion
- Exists only as decoration
- Competes with content for attention

Feedback must be perceptible, instantaneous, and meaningful for every action.

## Haptics

Vibratory feedback enriches experience when it complements sound and graphics—e.g. a light thump when a switch seats.

**Restrict haptics to culminating interaction moments.** Casual overuse causes sensory exhaustion. Never spam vibration for routine navigation.

## Inclusive Modular Layout

Adopt resilient spatial logic (auto layout / flexible grids):

- When users enlarge system text (Dynamic Type / accessibility text size), the interface must expand and reflow organically
- Visual harmony and utility must remain intact after reflow
- Do not hard-clip critical controls at larger text sizes

## Agent Instructions

1. Structure HIG chapters around Clarity → Deference → Depth before listing components.
2. Specify point-based layout and safe-area insets as hard requirements.
3. Publish elevation tokens and translucency limits.
4. Gate every animation on a state-explanation test; delete the rest.
5. Limit haptic recipes to a short approved list of climax moments.
6. Require Dynamic Type / large-text reflow proofs in UI reviews.

## Checklist

```
HIG chapter:
- [ ] Clarity / Deference / Depth defined operationally
- [ ] Points vs pixels mandate
- [ ] Safe-area collision ban
- [ ] Elevation & shadow tokens
- [ ] Translucency blur caps
- [ ] Motion justification rule + delay ban
- [ ] Haptic restriction to climax moments
- [ ] Dynamic Type / auto-layout resilience
```

## Component Review Questions

For any proposed UI:

1. Does every element have one clear job?
2. Does chrome yield to content?
3. Is layer order readable without decoration?
4. Does motion teach something?
5. Will it survive larger text and odd device insets?
