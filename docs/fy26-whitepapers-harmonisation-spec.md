# FY26 Whitepapers Harmonisation Specification

Status: Tranche 0 master specification  
Date: 2026-06-27  
Scope: FY26 UK-PS Whitepapers Series static HTML repo

## Purpose

This file defines the target repeatable shell for the FY26 UK-PS Whitepapers Series. It is intended to be consumed by later implementation tranches before editing the static HTML pages.

The original file was present as an empty placeholder at the start of Tranche 0. This specification has therefore been inferred from the strongest converged patterns already present across the series, especially the article pages that combine internal metadata, visible classification, breadcrumbs, reading tools, TOC, source notes, and page-level JavaScript metadata.

## Page Families

### Series Index

The root `index.html` is the series map. It should remain a navigation and reference hub rather than an article page.

Required index traits:

- Sticky utility bar with Oracle mark, series name, and visible classification.
- Series-level hero with route and series positioning.
- Navigation to all papers, reading paths, themes, and about/source handling.
- Complete internal metadata for the series.
- No article breadcrumb required.
- No article reading-tools panel required, although section navigation and reading progress may remain.

### Standard Paper Article

Each `paper-XX-*/index.html` page should use a common article shell while preserving the article-specific body design.

Required article traits:

- One `h1`, with title matching the paper title.
- Head metadata for description, robots, classification, series, paper number, paper version, and conversion version.
- Visible internal classification in the utility/header area, source notes where applicable, and footer.
- Series navigation back to the index and major index sections.
- Breadcrumb in the form `Series / Paper NN / Paper Title`.
- Hero with paper label, title, subtitle or summary, and a key takeaway or article orientation block.
- Bottom source and conversion record with paper number, version, source PDF filename, copyright, classification, route, conversion version, and status/date where available.
- Reading tools with table of contents, back-to-index, print/save as PDF, copy link where supported, and expand/collapse where the page uses `details`.
- Source and handling notes section.
- Footer repeating series, source/classification context, and copyright.

### Companion Reference Hub

The `fy26-year-in-review-reference-hub/index.html` page is a companion reference page rather than one of the numbered papers. It may keep its own information architecture, but should still align with the global classification, navigation, metadata, and source-note rules unless a stronger handling classification is intentional.

## Global Rules

### Classification

Target wording for the numbered whitepaper pages is:

`Confidential - Oracle Internal`

Use the same wording in:

- `<meta name="classification">`
- Top utility/header pill
- Article/source metadata
- Source notes
- Footer

If a companion page intentionally requires a stronger label, document that exception in the page metadata and source notes, and make sure the visible wording is not malformed.

### Head Metadata

All numbered papers should include:

```html
<meta name="description" content="...">
<meta name="robots" content="noindex,nofollow">
<meta name="classification" content="Confidential - Oracle Internal">
<meta name="series" content="FY26 UK-PS Whitepapers Series">
<meta name="paper-number" content="NN">
<meta name="paper-version" content="...">
<meta name="conversion-version" content="1.0">
```

Companion pages should include description, robots, classification, series, conversion version, source filename, and route where practical.

### Header And Navigation

The target shell should include:

- Skip link to main content.
- Sticky utility/header area.
- Oracle mark or wordmark.
- Series name: `FY26 UK-PS Whitepapers Series`.
- Visible classification pill.
- Series navigation links to index, all papers, reading paths, themes, and source notes/about page.

Class names may vary during transition, but future harmonisation should converge on semantic roles and consistent accessible labels before cosmetic naming.

### Breadcrumbs

Numbered papers should use a visible breadcrumb with `aria-label="Breadcrumb"`:

`Series / Paper NN / Paper Title`

The root index does not need a breadcrumb. The year-in-review hub may use:

`Series / FY26 Year in Review / Reference Hub`

### Hero

Article heroes should preserve each paper's editorial personality, but align to these elements:

- Paper number or series kicker.
- H1 title.
- Subtitle, dek, or summary.
- Key takeaway, orientation note, or summary card.
- Optional compact stat/metadata cards where already useful.

Avoid replacing a strong article-specific hero with a generic card layout. Harmonisation should standardise structure and metadata, not flatten the editorial treatment.

### Source And Conversion Record

Reader-facing article flow should not include a prominent `Article metadata`, `Source and conversion record`, or equivalent provenance card near the hero or immediately after the hero.

Source and conversion details are maintainability/provenance information. On numbered papers they should sit at the very bottom of the article flow, after article content, related-paper navigation, source notes, and handling notes, but before the footer.

Preferred implementation:

```html
<section class="source-record" aria-label="Source and conversion record">
  <details>
    <summary>Source and conversion record</summary>
    ...
  </details>
</section>
```

The `<summary>` label must be exactly:

`Source and conversion record`

The collapsed record should retain existing provenance fields where available:

- Paper number
- Title
- Version
- Source PDF filename
- Copyright
- Classification
- Route
- Conversion version
- Conversion date
- Last reviewed date
- Status
- Reading time

Known source caveats, such as filename-version mismatches, must be preserved. Do not delete provenance information unless it is clearly duplicated elsewhere and removal is safer than retaining it.

Classification may remain visible in the standard header and footer even when the detailed source record is collapsed.

### Reading Tools

Minimum article tools:

- Table of contents
- Back to index
- Print/save as PDF
- Copy page or current section link where JavaScript already supports it
- Expand all/collapse all where the page contains expandable sections

Preferred article tools:

- Reading progress indicator
- Active TOC state
- Reading mode toggle when already present
- Article-specific filters where they support the source content

Do not remove useful local tools such as profile filters, sector filters, misconception filters, or section copy controls when harmonising the general shell.

### Source Notes

Every numbered paper should include source and handling notes that state:

- Source PDF filename
- Classification
- Conversion approach
- Whether external research was used
- Any known caveat or validation warning
- Internal-only positioning

### Footer

The footer should repeat:

- Series name
- Paper title or page role
- Internal classification
- Source/copyright context
- Conversion version or last-reviewed date where available

## Divergence Bands

Use these bands for planning:

- Low: Target ingredients are mostly present. Work is mainly naming, ordering, breadcrumb wording, or small control consistency.
- Medium: Several target ingredients are present, but a page lacks a standard breadcrumb, progress/tool pattern, or complete head metadata.
- High: A page is missing core metadata, uses a materially different classification pattern, or has a special shell that needs deliberate alignment before visual work.

## Preservation Rules

Later tranches must preserve:

- Article-specific narrative structures, tables, diagrams, filters, timelines, and cards.
- Source-derived caveats and validation warnings.
- Existing source PDF filenames and version notes.
- Internal-only and no-public-SEO posture.
- Accessibility affordances already present, including skip links, focus states, semantic landmarks, TOC labels, and print styles.
