---
name: human-interface
description: >-
  Defines digital human interface rules: clarity, deference, depth, point-based
  layout, safe areas, elevation, translucency, motion, haptics, and accessible
  reflow. Use when writing HIG chapters, auditing UI behavior, or specifying
  interaction and motion systems.
---

# Human Interface

Logo and color rules are not enough for technology products. Digital interaction must feel fluid, instinctive, and native—without confusion or cognitive fatigue.

## Purpose

Specify behavior for interfaces: hierarchy, layout units, safe areas, depth materials, motion, haptics, and accessible reflow.

## Rules

### Pillar 1 — Clarity

Everything on screen has precise, immediate, unambiguous meaning.

- Typography legibility outranks artistic flourish
- Icons stay clean and geometrically focused—no second readings
- Remove any ornament that does not help complete a task
- Design in **points**, not absolute device pixels, so UI scales across `@1x` / `@2x` / `@3x` densities

### Pillar 2 — Deference

UI is not the protagonist. It is an invisible scaffold for content (imagery, data, text).

- Navigation bars, tabs, and modals fuse with structure
- Prefer subtle blur or minimal translucency over opaque overlays that compete for attention
- Respect **safe areas**: no primary interactive control may collide with or hide behind notches, home indicators, or rounded corners

### Pillar 3 — Depth

The brain needs spatial signals for hierarchy. Depth is controlled perspective and digital material—not skeuomorphic nostalgia.

| Property | Mandate |
|----------|---------|
| Shadows & elevation | Fixed Z-axis shadow recipes (blur, opacity) that mimic real light; signal what is tappable |
| Translucency | Frosted layers preserve context under overlays; **cap blur thresholds**—excess harms usability |

### Motion

Motion is not cosmetic charm.

**Allowed when it:**

- Explains a state change
- Confirms a successful transaction
- Responds to a gesture with physically plausible momentum

**Prohibited when it:**

- Delays task completion
- Exists only as decoration
- Competes with content for attention

Every action gets feedback that is perceptible, instantaneous, and meaningful.

### Haptics

Vibration may complement sound and graphics (e.g. a light thump when a switch seats).

**Restrict haptics to culminating interaction moments.** Overuse causes sensory exhaustion. Never spam vibration for routine navigation.

### Inclusive modular layout

Use resilient spatial logic (auto layout / flexible grids):

- When users enlarge system text, the interface expands and reflows organically
- Visual harmony and utility remain intact after reflow
- Never hard-clip critical controls at larger text sizes

## Workflow

1. Structure the chapter as Clarity → Deference → Depth before listing components.
2. Mandate point-based layout and safe-area insets.
3. Publish elevation tokens and translucency caps.
4. Gate every animation on a state-explanation test; delete the rest.
5. Limit haptic recipes to a short approved climax list.
6. Require large-text reflow proofs in UI review.

## Deliverables

- Pillar definitions with operational bullets
- Point vs pixel mandate
- Safe-area rules
- Elevation and translucency tokens
- Motion justification policy
- Approved haptic event list
- Reflow / text-scaling acceptance criteria

## Checklist

```
HIG chapter:
- [ ] Clarity / Deference / Depth defined operationally
- [ ] Points vs pixels mandate
- [ ] Safe-area collision ban
- [ ] Elevation and shadow tokens
- [ ] Translucency blur caps
- [ ] Motion justification rule + delay ban
- [ ] Haptic restriction to climax moments
- [ ] System text-scaling / auto-layout resilience
```

## Component review questions

1. Does every element have one clear job?
2. Does chrome yield to content?
3. Is layer order readable without decoration?
4. Does motion teach something?
5. Does it survive larger text and irregular device insets?

## Forbidden

- Ornament that does not aid the task
- Opaque chrome fighting content
- Controls under notches or home indicators
- Decorative or delaying animation
- Routine haptic spam
- Fixed layouts that break when text scales
