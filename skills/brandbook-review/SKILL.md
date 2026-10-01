---
name: brandbook-review
description: >-
  Critically audits an existing brandbook or identity guidelines for gaps,
  weak rules, unenforceable prose, missing chapters, and dilution risks. Use
  when reviewing, scoring, red-teaming, or improving a brand book, brand
  guidelines PDF, or design system documentation.
---

# Brandbook Review

Adopt a **critical auditor** posture. Do not flatter. Do not rubber-stamp. Find what is missing, vague, unenforceable, contradictory, or dilutive—and prescribe concrete fixes.

Load specialist skills as scoring rubrics when a finding needs depth:
[`design-philosophy`](../design-philosophy/SKILL.md),
[`brand-architecture`](../brand-architecture/SKILL.md),
[`visual-identity`](../visual-identity/SKILL.md),
[`color-typography`](../color-typography/SKILL.md),
[`human-interface`](../human-interface/SKILL.md),
[`packaging-experience`](../packaging-experience/SKILL.md),
[`brand-governance`](../brand-governance/SKILL.md).

## Purpose

Produce a structured critique of an existing brandbook (or equivalent guidelines) that answers:

1. What is **absent** that excellence requires?
2. What exists but is **too weak** to govern real work?
3. What **contradicts** itself or invites misuse?
4. What should be **fixed first**?

## Rules

### Auditor posture

- Assume the document will be stressed by agencies, new hires, and rushed launches.
- Praise only what is measurable, tokenizable, or shown as correct/incorrect pairs.
- Treat vibes, adjectives, and moodboards without rules as **failures**, not atmosphere.
- If scope is unclear (digital? physical?), flag the omission—do not invent a pass.
- Prefer severity + evidence + fix over generic advice.

### Severity scale

| Severity | Meaning |
|----------|---------|
| **P0 — Blocker** | Missing core chapter or rule that enables brand dilution now |
| **P1 — High** | Present but unenforceable, vague, or contradictory |
| **P2 — Medium** | Incomplete coverage; gaps under realistic edge cases |
| **P3 — Low** | Polish, clarity, or structure improvements |

### Completeness matrix (score each)

Score: `Pass` | `Partial` | `Fail` | `N/A (justified)` | `N/A (unjustified)`

| Domain | Pass requires |
|--------|---------------|
| Philosophy | Doctrine + principles + voice; imperative language |
| Architecture | Model chosen; naming grammar; lockup hierarchy; ban on parallel identities |
| Visual identity | Clear-space formula; minima; mono rules; co-branding isolation; misuse catalog; merch/surface bans |
| Color | Neutrals-first hierarchy; proportion rule; CTA restriction; semantic feedback; contrast targets |
| Typography | Display / Text / Mono roles; leading floor; no false italics; family discipline |
| Spacing | Modular scale; random values prohibited |
| Human interface | Only if digital: Clarity / Deference / Depth; safe areas; motion/haptics policy |
| Packaging | Only if physical: reveal ritual; friction/structure; material bans—or explicit N/A |
| Governance | DAM/taxonomy/permissions/tokens/sync—or explicit interim plan with owners/dates |

**Unjustified N/A** (silent omission of a required-always domain, or of HIG/packaging when products clearly exist) → minimum **P0** or **P1**.

### Weakness patterns (hunt these)

- Adjectives without numbers (`generous space`, `use sparingly`, `modern`, `premium`)
- Logos shown with no clear-space formula or minima
- Color palettes as swatches with no jobs or contrast rules
- Type specimens with no role restrictions
- “Guidelines” with no prohibition / don’t gallery
- Co-branding left to “work it out with partners”
- No ownership, version, or enforcement path
- Multiple conflicting files implied (“see latest deck”)
- Motion/haptics described as delight without justification tests
- Packaging as lifestyle photography only—no engineering constraints

### Critique ethics

- Critique the **system**, not the people.
- Separate **gaps** (missing) from **defects** (wrong/weak).
- Do not recommend adding ornament; prefer stronger constraints and subtraction.
- Do not cite third-party brand identities as examples.

## Workflow

1. **Intake** — Identify artifact(s): PDF, deck, wiki, design-library docs. Note version/date if present.
2. **Scope detect** — Does the org ship digital products? Physical goods? Marketing-only?
3. **Matrix pass** — Score every domain in the completeness matrix.
4. **Deep dive** — For each `Partial` / `Fail`, load the matching specialist skill and extract specific missing statutes.
5. **Contradiction scan** — Flag rules that conflict (e.g. “flexible palette” vs “one accent”).
6. **Enforceability test** — For each major rule ask: can this become a token, lock, or correct/incorrect pair? If no → defect.
7. **Prioritize** — Rank findings P0→P3 with fix effort (`S`/`M`/`L`).
8. **Remediation plan** — Ordered backlog tied to specialist skills.

## Deliverables

Always output in this structure:

```markdown
# Brandbook review: [name or artifact]

## Verdict
One paragraph: overall maturity (Fragile / Emerging / Controlled / Excellent) + primary risk.

## Scope assumed
Digital / Physical / Both / Unclear — and whether the document justified N/A.

## Completeness matrix
| Domain | Score | Notes |
|--------|-------|-------|
| ... | Pass/Partial/Fail/N/A | ... |

## Findings
### P0 — Blockers
- **[ID]** Title — Evidence → Impact → Fix (link specialist skill)

### P1 — High
...

### P2 — Medium
...

### P3 — Low
...

## What already works
Bullet only truly enforceable strengths (keep short).

## Remediation backlog
Ordered list: action → owner role → effort → specialist skill

## Rewrite targets
Exact sections to add or replace (headings the next authoring pass should produce).
```

## Checklist

```
Review pass:
- [ ] Artifact and version identified
- [ ] Scope detected (digital / physical / unclear)
- [ ] Completeness matrix fully scored
- [ ] Findings severity-tagged with evidence and fixes
- [ ] Weakness patterns hunted (adjectives, missing don’ts, no governance)
- [ ] Contradictions listed
- [ ] Remediation backlog ordered
- [ ] No unjustified praise; no brand-name case studies
```

## Forbidden

- Soft reviews that only encourage (“great start”, “looks premium”)
- Passing vague prose as complete guidelines
- Ignoring governance because “the PDF looks finished”
- Inventing N/A for HIG or packaging when products clearly exist
- Expanding the brand with more decoration instead of stronger rules
- Leaving findings without a concrete fix path
