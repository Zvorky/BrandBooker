---
name: brandbook-review
description: >-
  Critically audits an existing brandbook against the full BrandBooker skill
  set—philosophy, architecture, visual identity, color, typography, human
  interface, packaging, and governance. Use when reviewing, scoring,
  red-teaming, or remediating brand guidelines, identity PDFs, or design docs.
---

# Brandbook Review

Adopt a **critical auditor** posture. Do not flatter. Do not rubber-stamp. Measure the artifact against this entire skill set—not against taste.

## Required context (load these)

A competent review is **impossible** from this file alone. Before scoring, load:

| Priority | Skill | Why the auditor needs it |
|----------|-------|--------------------------|
| Always | [`../SKILL.md`](../SKILL.md) (orchestrator) | Manifesto, scope gates, output quality bar, sequencing rules |
| Always | [`../design-philosophy/SKILL.md`](../design-philosophy/SKILL.md) | Doctrine, ten principles, voice posture |
| Always | [`../brand-architecture/SKILL.md`](../brand-architecture/SKILL.md) | Monolithic default, naming, lockups |
| Always | [`../visual-identity/SKILL.md`](../visual-identity/SKILL.md) | Clear space, minima, co-branding, misuse catalog, merch |
| Always | [`../color-typography/SKILL.md`](../color-typography/SKILL.md) | Palette jobs, contrast, type roles, spacing scale |
| Always | [`../brand-governance/SKILL.md`](../brand-governance/SKILL.md) | DAM, taxonomy, permissions, tokens, sync |
| If digital products | [`../human-interface/SKILL.md`](../human-interface/SKILL.md) | Clarity / Deference / Depth, motion, haptics, safe areas |
| If physical goods / kits | [`../packaging-experience/SKILL.md`](../packaging-experience/SKILL.md) | Unboxing ritual, friction, materials |

**Rule:** For every `Partial` / `Fail`, cite the specialist skill path and the missing statute from that skill's Rules or Checklist. Remediation actions must name the skill that authors the fix.

## Purpose

Produce a structured critique that answers:

1. What is **absent** that the skill set requires?
2. What exists but is **too weak** to govern real work?
3. What **contradicts** the manifesto or other chapters?
4. What should be **fixed first**, and which skill owns the rewrite?

## Rules

### Auditor posture

- Stress-test the document as agencies, new hires, and rushed launches will use it.
- Praise only what is measurable, tokenizable, or shown as correct/incorrect pairs—criteria aligned with the orchestrator quality bar.
- Treat vibes, adjectives, and moodboards without rules as **failures**.
- If scope is unclear (digital? physical?), flag unjustified omission per orchestrator **Scope Gates**—do not invent a pass.
- Prefer severity + evidence + specialist-linked fix over generic advice.
- Prefer stronger constraints and subtraction ([`design-philosophy`](../design-philosophy/SKILL.md)); never “improve” by adding ornament.

### Severity scale

| Severity | Meaning |
|----------|---------|
| **P0 — Blocker** | Missing always-required domain, or unjustified N/A where products exist; enables dilution now |
| **P1 — High** | Present but fails specialist Pass criteria (vague, unenforceable, contradictory) |
| **P2 — Medium** | Incomplete vs specialist edge cases (hardware exceptions, badges, haptics list, etc.) |
| **P3 — Low** | Structure, clarity, cross-links between chapters |

### Manifesto gate ([`../SKILL.md`](../SKILL.md))

Fail the review's “system maturity” if the artifact cannot satisfy the orchestrator manifesto:

1. Confidence through suppression
2. Governance by enforcement (tokens/tool locks, not PDF prose alone)
3. Silent ergonomics (when digital)
4. Tangible worth (when physical)

Also check orchestrator **Output Quality Bar** and **Forbidden** list as global defect sources.

### Critical rubrics by skill

Score each domain: `Pass` | `Partial` | `Fail` | `N/A (justified)` | `N/A (unjustified)`.

Unjustified N/A on always-required domains, or on HIG/packaging when products clearly exist → **P0** or **P1**.

#### 1. Design philosophy — [`design-philosophy`](../design-philosophy/SKILL.md)

| Audit question | Fail if… |
|----------------|----------|
| Is “less but better” explicit? | Maxim absent or only decorative |
| Are all ten good-design principles present with operational implications? | List missing, slogans only, or no product/UI/packaging implications |
| Is voice posture defined (clear, confident, honest, calm, precise)? | Tone left to “brand personality” adjectives |
| Is language imperative (`must` / `shall` / `prohibited`)? | Suggestions and inspiration-only framing |
| Does doctrine bind partners as well as internal teams? | No external-partner applicability |

**Weak signals:** trend language, feature accumulation as progress, design-as-art-first.

#### 2. Brand architecture — [`brand-architecture`](../brand-architecture/SKILL.md)

| Audit question | Fail if… |
|----------------|----------|
| Is architecture model chosen with rationale? | No model; or non-monolithic without structural exception |
| Are Primary / Secondary / Product / No lockup defined? | Lockups missing or “flexible” |
| Is naming grammar specified? | Ad-hoc product names; prefix proliferation unchecked |
| Are divisions barred from separate identities? | Teams allowed custom marks |
| Is font-weight misuse in body text banned? | Weight used as fake product hierarchy |

**Weak signals:** product mascots replacing parent mark; undocumented exceptions; no legacy migration plan.

#### 3. Visual identity — [`visual-identity`](../visual-identity/SKILL.md)

| Audit question | Fail if… |
|----------------|----------|
| Clear space formula tokenized (default `X/2`)? | “Give it room” without math |
| Digital (≥40 px) and print (≥10 mm) minima tabulated? | Specimens only |
| Mono rules (black K / white)? | Unrestricted recolor |
| Co-branding isolation (no fused signatures)? | “Collaborate visually with partners” |
| Misuse catalog with correct/incorrect pairs? | No don’t gallery |
| Merch colors + single application + banned surfaces? | Open merch policy |

**Also check:** badge clear space (`X/4`) if badges exist; hardware exception path (`H/10` + approval).

#### 4. Color & typography — [`color-typography`](../color-typography/SKILL.md)

| Audit question | Fail if… |
|----------------|----------|
| Neutrals-first + proportion rule (~80/15/5)? | Rainbow swatches, no hierarchy |
| Primary reserved for CTA / isolated emphasis; banned in body text? | Primary used as paragraph color |
| Semantic feedback + contrast targets (WCAG)? | Hue-only status colors; forced failing pairs |
| Display / Text / Mono roles? | Specimens without role locks |
| Body leading ≥ 150%; no false italics / mechanical distortion? | “Feel free to italicize” via software slant |
| Modular spacing scale; random values prohibited? | One-off padding everywhere |
| Third family resisted by default? | Decorative font buffet |

#### 5. Human interface — [`human-interface`](../human-interface/SKILL.md)

*Score N/A only if software is explicitly out of scope.*

| Audit question | Fail if… |
|----------------|----------|
| Clarity / Deference / Depth defined operationally? | Logo/color chapter substitutes for HIG |
| Points vs pixels; safe-area collision ban? | Absolute-px layouts; controls under insets |
| Elevation + translucency caps tokenized? | Unlimited blur/shadow fashion |
| Motion justified only for state/gesture/success; no delay? | Decorative animation celebrated |
| Haptics limited to climax moments? | Vibration on routine nav |
| System text-scaling / reflow resilience? | Fixed layouts that clip at large text |

Use that skill's **Component review questions** when sampling UI pages inside the brandbook.

#### 6. Packaging experience — [`packaging-experience`](../packaging-experience/SKILL.md)

*Score N/A only if physical goods/kits are explicitly out of scope.*

| Audit question | Fail if… |
|----------------|----------|
| Hero-first reveal; secondary tier for docs/cables? | Lifestyle photos only |
| Lid friction / tolerance (~< 2 mm) specified? | No engineering constraints |
| Rigid structure + nest strategy? | Soft mailers as the premium story |
| Typographic silence on outer pack? | Explainer-heavy exteriors |
| Polymer/film bans; fiber systems preferred? | Foam/plastic as default |

#### 7. Brand governance — [`brand-governance`](../brand-governance/SKILL.md)

| Audit question | Fail if… |
|----------------|----------|
| DAM as system of record? | PDF-only, no asset home |
| Taxonomy path pattern? | Folder chaos / duplicate masters |
| Permission matrix (vendors least privilege)? | Vendors can edit master marks |
| Auditable approval flow? | Email-only approvals |
| Tokens covering logo, color, type, space, motion? | Hex pasted ad hoc |
| Design-tool sync + audit cadence + deprecation? | “We’ll update the deck later” |

**Success metric from that skill:** inability to ship non-compliant exports easily—not page count.

### Cross-skill contradiction scan

Flag conflicts such as:

- Flexible architecture vs monolithic statutes ([`brand-architecture`](../brand-architecture/SKILL.md))
- “Expressive color” vs 80/15/5 + CTA lock ([`color-typography`](../color-typography/SKILL.md))
- Co-brand fusion art vs isolation ([`visual-identity`](../visual-identity/SKILL.md))
- Delight motion vs motion-justification test ([`human-interface`](../human-interface/SKILL.md))
- Beautiful PDF with zero DAM/tokens ([`brand-governance`](../brand-governance/SKILL.md) vs orchestrator manifesto item 2)
- Philosophy of subtraction vs ornamental packaging/UI chapters ([`design-philosophy`](../design-philosophy/SKILL.md))

### Critique ethics

- Critique the **system**, not the people.
- Separate **gaps** (missing vs specialist checklist) from **defects** (wrong/weak vs specialist rules).
- Do not cite third-party brand identities as examples.
- Every finding's fix path must name a specialist skill (or the orchestrator for structural sequencing).

## Workflow

1. **Intake** — Identify artifact(s), version/date.
2. **Load context** — Orchestrator + always-on specialists; add HIG and/or packaging per scope.
3. **Scope detect** — Digital / physical / both / unclear; apply orchestrator Scope Gates.
4. **Manifesto gate** — Score against the four manifesto directives.
5. **Matrix pass** — Score every domain using the rubrics above (not a thin summary table alone).
6. **Deep dive** — For each `Partial` / `Fail`, open the specialist skill and quote missing checklist items as findings.
7. **Contradiction scan** — Run the cross-skill list.
8. **Enforceability test** — Can each major rule become a token, lock, or correct/incorrect pair? If no → defect under governance + the owning domain skill.
9. **Prioritize** — P0→P3 with effort `S`/`M`/`L`.
10. **Remediation backlog** — Ordered actions, each tagged with the specialist skill that must author the rewrite.

## Deliverables

Always output:

```markdown
# Brandbook review: [name or artifact]

## Verdict
Maturity: Fragile | Emerging | Controlled | Excellent — primary risk in one paragraph.

## Scope assumed
Digital / Physical / Both / Unclear — N/A justifications accepted or rejected (cite orchestrator Scope Gates).

## Skills loaded
List which specialist SKILL.md files were used for this review.

## Manifesto gate
| Directive | Pass/Fail | Notes |
|-----------|-----------|-------|
| Suppression | | |
| Enforcement | | |
| Silent ergonomics | | or N/A |
| Tangible worth | | or N/A |

## Completeness matrix
| Domain | Specialist skill | Score | Notes |
|--------|------------------|-------|-------|
| Philosophy | design-philosophy | | |
| Architecture | brand-architecture | | |
| Visual identity | visual-identity | | |
| Color & typography | color-typography | | |
| Human interface | human-interface | | |
| Packaging | packaging-experience | | |
| Governance | brand-governance | | |

## Findings
### P0 — Blockers
- **[ID]** Title — Evidence → Impact → Fix via `skills/<specialist>/SKILL.md` (statute/checklist item)

### P1 — High
...

### P2 — Medium
...

### P3 — Low
...

## What already works
Only enforceable strengths; cite which skill's Pass criteria they meet.

## Remediation backlog
1. Action → role → effort → `skills/<specialist>/SKILL.md`
2. ...

## Rewrite targets
Headings/chapters to add or replace, mapped to the Full Brandbook Workflow in the orchestrator.
```

## Checklist

```
Review pass:
- [ ] Orchestrator + always-on specialists loaded (HIG/packaging if in scope)
- [ ] Artifact and version identified
- [ ] Scope gated per orchestrator
- [ ] Manifesto gate scored
- [ ] Completeness matrix scored with specialist skill column
- [ ] Each Partial/Fail cites a specialist statute or checklist item
- [ ] Cross-skill contradictions scanned
- [ ] Findings severity-tagged with evidence and skill-linked fixes
- [ ] Remediation backlog names specialist skills
- [ ] No unjustified praise; no third-party brand case studies
```

## Forbidden

- Reviewing without loading the specialist skills listed above
- Soft reviews (“great start”, “looks premium”)
- Passing vague prose that would fail any specialist checklist
- Ignoring governance because the PDF “looks finished”
- Inventing N/A for HIG or packaging when products clearly exist
- Findings without a fix path tied to a specialist skill
- Recommending more decoration instead of stronger rules from `design-philosophy`
