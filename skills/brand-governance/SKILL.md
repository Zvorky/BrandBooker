---
name: brand-governance
description: >-
  Governs Digital Asset Management (DAM) end-user folder taxonomy, vector/raster
  delivery specs, naming conventions, permissions, and bidirectional
  design-token synchronization. Use when structuring brand repositories, handover
  packages, or token pipelines.
---

# Brand Governance & DAM Architecture

A brand system fails when teams cannot locate the right asset in seconds or when code drifts from guidelines. Governance enforces consistency at the file-system and token levels.

## Purpose

Establish a decision-tree DAM folder structure, mandatory vector/raster deliverables, naming conventions, role permissions, and token synchronization rules.

## Rules

### 1. End-User Decision-Tree DAM Taxonomy
Organize brand delivery repositories around the **end user's selection decision**, never by internal designer workflow:

1. **Level 1 - Logo Variant:** `01-Full-Lockup/`, `02-Stacked-Lockup/`, `03-Logomark/`, `04-Favicon/`
2. **Level 2 - Color Space / Medium:** `01-Digital-RGB/` and `02-Print/` (subdivided into `01-CMYK/` and `02-Pantone-PMS/`)
3. **Level 3 - Chromatic Variant:** `01-Primary-Color/`, `02-Monochrome-Black/`, `03-Monochrome-White/`, `04-Inverted/`
4. **Level 4 - Format Type:** `Vector/` and `Raster/`
5. **Source Vault (`00-Source-Files/`):** Restricted folder holding master editable source files (`.ai`, `.glyphs`, `.fig`) separated from distribution folders.

#### Mandatory Delivery Formats & Scales
- **Vector Formats:**
  - `SVG` (RGB, clean viewBox, outlined typography, zero stray handles; mandatory for web/UI)
  - `PDF` (universal editable vector master for modern print/editorial workflows)
  - `EPS` (legacy print-shop compatibility across RGB, CMYK, and Pantone)
- **Raster Formats (Transparent `PNG` + `WebP` / `JPG`):**
  - `1920px` width - Primary / hero / presentation scale
  - `960px` width - Medium / standard web & document scale
  - `192px` width - Small / email signature & compact avatar scale
  - `16x16px` & `32x32px` - Solid micro-scale favicons

### 2. Naming Grammar & Single Source of Truth
- **File Naming Convention:** `{brand-slug}_{variant}_{colorspace}_{chromia}_{scale}.{ext}`
  - Example: `acme-corp_logomark_rgb_mono-white_960w.png`
- **Repository Partitioning:**
  - Core design system documentation (`brandbook.md`, `DESIGN.md`) lives alongside machine-readable tokens (`tokens.css`, `tokens.json`).
  - Downstream web projects consume brand tokens via inheritance (`Project > Brand > Fallback Baseline`) and never fork or mutate core brand assets locally.

### 3. Permissions, Versioning & IP Handover
- **Role-Based Governance:**
  - *Brand Architects / Maintainers:* Write access to `00-Source-Files/`, `brandbook.md`, `DESIGN.md`, and `tokens.*`.
  - *Developers / Marketing / External Vendors:* Read/consume access to distribution folders and token packages; changes require Pull Request + `brandbook-review` audit.
- **Semantic Versioning:** Increment `MAJOR` for mark/architecture shifts, `MINOR` for new tokens/components, `PATCH` for bug/contrast fixes, logging every decision in `history/`.
- **Commercial Handover:** Complete delivery packages include searchable `brandbook.pdf` (or interactive web portal), the audited DAM directory, and formal Intellectual Property (IP) transfer documentation.

## Workflow

1. Structure DAM folders around end-user selection decisions and isolate `00-Source-Files/`.
2. Export required vector (`SVG`, `PDF`, `EPS`) and raster (`1920px`, `960px`, `192px`, `16x16px`/`32x32px`) assets using the standard naming grammar.
3. Enforce role permissions, semantic versioning in `history/`, and token inheritance across projects.

## Deliverables

- Decision-tree DAM taxonomy and `00-Source-Files/` vault
- Required vector/raster exports, naming grammar, and token sync rules
- Permission roles, versioning log, and IP handover checklist

## Checklist

```text
Brand governance chapter:
- [ ] Decision-tree DAM hierarchy and 00-Source-Files vault defined
- [ ] SVG/PDF/EPS vectors and 1920px/960px/192px/favicon rasters specified
- [ ] Naming grammar, role permissions, history logging, and token inheritance defined
```

## Forbidden

- Multiple conflicting "latest" brand PDFs or unversioned asset drops
- External vendors editing master brand sources directly
- Hardcoded hex values or local asset forks bypassing token inheritance
