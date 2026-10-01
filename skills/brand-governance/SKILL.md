---
name: brand-governance
description: >-
  Turns brand guidelines into enforceable systems via DAM, immutable taxonomy,
  permission profiles, auditable approvals, design tokens, and bidirectional
  sync to design tools. Use when preventing brand equity dilution, building
  asset pipelines, or operationalizing compliance.
---

# Brand Governance

A long PDF or intranet deck is a stillborn model. Teams dilute brand equity when they treat systemic design as a one-off project without continuous alignment. As headcount and agencies grow, fragmented rulebook versions proliferate.

## Purpose

Evolve the brandbook into a living Digital Asset Management (DAM) and token-driven compliance ecosystem so non-compliance is hard at creation time.

## Rules

### DAM as active control

DAM guards formal language coherence. It must connect guidelines to executable templates and searchable libraries—one source of truth, discoverable, continuously synchronized.

### Mandatory pillars

1. **Immutable taxonomy and naming**
   - Directory matrix example:
     `Identity Area → Geography → Campaign / Tactic → Format & Function`
   - Prevents duplicate re-renders and lost productivity

2. **Granular permission profiles**
   - Vendors receive least-privilege access
   - Block accidental edits to master matrices that would miscalibrate color or damage logo hierarchy

3. **Auditable approvals**
   - Final art approval lives in integrated panels—not fractured email chains
   - Every variation is logged and reversible

### Bidirectional sync with design tools

Guidelines must propagate into primary design environments via **design tokens** and shared libraries.

When leadership validates even a micro-change to a neutral for contrast:

- Tokens update at the source
- Remote canvases consuming shared libraries adopt the change
- Type styles and spacing matrices converge without manual chase-down

Modular systems should **block** construction that violates standardized distances (margins, leading, padding, gaps). Documentation becomes a proactive constraint at creation time.

### Token propagation map

| Brand rule domain | System artifact |
|-------------------|-----------------|
| Clear space & logo minima | `logo.*` sizing/padding tokens + component locks |
| Color hierarchy & contrast | Semantic color tokens; raw hex banned in production |
| Type roles | Text styles: Display / Text / Mono only |
| Spacing | Scalar spacing tokens only |
| Elevation / motion | Elevation and duration tokens; unlisted animations rejected |

### Success metric

Measure success as **inability to ship non-compliant exports easily**—not as PDF page count.

## Workflow

1. Never ship guidelines without a governance plan (DAM + tokens + permissions).
2. Design taxonomy before uploading assets.
3. Prefer tool-level locks (shared libraries, style tokens) over training decks alone.
4. On any brand change, specify the sync path to every consuming surface.
5. Schedule periodic compliance audits of assets and live UI.
6. Maintain a deprecation path for legacy non-compliant files.

## Deliverables

- DAM designated as system of record
- Taxonomy path pattern
- Permission matrix (roles × actions)
- Approval workflow with audit trail
- Token list covering identity, color, type, space, motion
- Design-tool sync architecture
- Audit cadence + deprecation policy

## Checklist

```
Governance chapter:
- [ ] DAM role defined as system of record
- [ ] Taxonomy path pattern documented
- [ ] Permission matrix (roles × actions)
- [ ] Auditable approval flow
- [ ] Token list covering identity, color, type, space, motion
- [ ] Design-tool sync architecture
- [ ] Audit cadence and deprecation policy
```

## Forbidden

- Multiple competing "latest" brand PDFs
- Vendors with edit rights to master logo files
- Hex values pasted outside the token system
- One-off local styles disconnected from the central library
- Email-only approval with no asset version pin
- Guidelines shipped without an enforcement path
