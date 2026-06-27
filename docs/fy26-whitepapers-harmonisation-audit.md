# FY26 Whitepapers Harmonisation Audit

Date: 2026-06-27  
Scope: static inspection of root index, numbered paper pages, and the FY26 year-in-review reference hub.  
Constraint: no visual or HTML changes were made in Tranche 0.

## Audit Basis

The harmonisation specification now lives at `docs/fy26-whitepapers-harmonisation-spec.md`. It was created in this tranche because the file existed as an empty placeholder at the start of the audit.

Divergence levels are based on the repeatable page shell: header/nav, classification, breadcrumb, hero, metadata, reading tools, and source handling. They do not judge the quality of the article content.

## Summary

- Relevant pages detected: 15 total.
- Numbered paper pages detected: 13.
- Companion/reference pages detected: root series index plus FY26 year-in-review hub.
- Low divergence: root index, papers 02, 03, 05, 06, 09, 10, 11, 13.
- Medium divergence: papers 01, 07, 08, 12.
- High divergence: paper 04 and FY26 year-in-review reference hub.

## Page Audit

### Series Index

- Detected path: `index.html`
- Current header/nav pattern: sticky `.utility-bar`, `.brand-lockup`, visible classification, `header.site-header`, `.nav-shell`, and `nav.primary-nav` for series map links.
- Current classification wording: head metadata and visible pill both use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: none, appropriate for the root index.
- Current hero pattern: series-level `.hero` with `.hero-main`, lede, route metadata, and side cards.
- Metadata present: Yes, series-level head metadata and internal JSON-style metadata are present.
- Reading tools present: Partial by design. The page has section navigation and progress/TOC-like behaviour, but no article reading-tools panel is required for the index.
- Divergence: Low.
- Preserve: series map, all-paper routing, reading paths, themes, metadata block, and internal-only positioning.

### FY26 Year In Review Reference Hub

- Detected path: `fy26-year-in-review-reference-hub/index.html`
- Current header/nav pattern: sticky `.utility` bar, Oracle/FY26 reference hub brand, classification pill, `header.hero`, and sticky `nav.toc`.
- Current classification wording: head and visible page text use `Confidential - Oracle Restricted Employees Only`, but the rendered source contains a stray backslash before `Employees` in several places.
- Current breadcrumb pattern: `Series / FY26 Year in Review / Reference Hub`.
- Current hero pattern: large reference-hub hero grid with `.hero-main`, `.hero-side`, metadata card, takeaway card, and hero actions.
- Metadata present: Partial. Head has robots, generator, and classification, but lacks the standard series/conversion/source-route set. Visible source and classification metadata are present.
- Reading tools present: Partial. TOC, print/save as PDF, and section copy links exist; no standard article tools block or progress indicator.
- Divergence: High.
- Preserve: reference-hub role, year-in-review narrative structure, timeline/reference map, copy-link affordances, and stronger classification if it is intentional.

### Paper 01 - The Visionaries Who Shaped Our Cloud

- Detected path: `paper-01-visionaries-who-shaped-our-cloud/index.html`
- Current header/nav pattern: sticky `.utility-bar`, `header.site-header`, top nav links to index, contents, pioneer profiles, source notes, and print.
- Current classification wording: head metadata and visible pill use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: none.
- Current hero pattern: split `.hero` and `.hero-inner` with paper kicker, H1, subtitle, summary, side key takeaway, and metadata card.
- Metadata present: Yes. Full head metadata, visible metadata, and page metadata script are present.
- Reading tools present: Yes. Progress bar, sticky TOC, print, copy section link, profile expand/collapse, and profile filters are present. It lacks a standard back-to-index reading-tools panel.
- Divergence: Medium.
- Preserve: timeline treatment, pioneer profile filters, profile expand/collapse behaviour, source notes, and no-external-research caveat.

### Paper 02 - Masters of Many: Champions of Choice

- Detected path: `paper-02-masters-of-many-champions-of-choice/index.html`
- Current header/nav pattern: `.series-header`, `.global-nav`, visible classification pill, breadcrumb nav, reading-tools bar, and sticky TOC.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 02 / Masters of Many: Champions of Choice`.
- Current hero pattern: `.hero` and `.hero-grid` with title, classification chip, hero actions, and metadata card.
- Metadata present: Yes. Full head metadata, visible article metadata, source notes, and page metadata script are present.
- Reading tools present: Yes. Progress, back to index, copy page link, copy current section link, print/save, expand/collapse, reading mode, active TOC.
- Divergence: Low.
- Preserve: strategic pillar tables/cards, portfolio breadth evidence, copyright metadata note, and reading mode.

### Paper 03 - Evolving Expectations In The Enterprise Cloud Market

- Detected path: `paper-03-evolving-expectations-enterprise-cloud-market/index.html`
- Current header/nav pattern: `.utility-bar` as banner, `.series-header`, `.global-nav`, breadcrumb nav, metadata panel, tools card, and sticky TOC card.
- Current classification wording: head metadata and visible pill use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 03 / Evolving Expectations in the Enterprise Cloud Market`.
- Current hero pattern: `.hero-wrap` and `.article-hero` with kicker, subtitle, summary, key takeaway, and stat grid.
- Metadata present: Yes. Full head metadata, visible article metadata, source notes, and page metadata script are present.
- Reading tools present: Yes. Reading progress, back to index, print/save, expand/collapse, section copy links, active TOC.
- Divergence: Low.
- Preserve: source evidence tables, Oracle differentiation signals, playbook details, section copy controls, and caveat about validating current claims.

### Paper 04 - Sovereignty And Trust In Cloud

- Detected path: `paper-04-sovereignty-and-trust-in-cloud/index.html`
- Current header/nav pattern: `.utility` header, visible classification pill, breadcrumb nav, global links, tools wrap, side TOC, and next/previous navigation.
- Current classification wording: visible page text uses `Confidential - Oracle Internal`; head classification metadata is missing.
- Current breadcrumb pattern: `Series / All papers / Paper 04`.
- Current hero pattern: `.article-hero` with `.hero-panel`, hero content, badges, and hero card.
- Metadata present: Partial. Visible article metadata exists, but head metadata lacks classification, series, paper-number, paper-version, and conversion-version.
- Reading tools present: Yes. Back to index, copy page link, print/save, expand/collapse, TOC, and active section handling are present; no progress indicator.
- Divergence: High.
- Preserve: sovereignty/legal caution language, comparison tables, technical patterns, field guidance, source notes, and validation caveats.

### Paper 05 - How And Why OCI's Technical Performance Is Real

- Detected path: `paper-05-oci-technical-performance-is-real/index.html`
- Current header/nav pattern: `.series-header`, `.nav`, breadcrumb nav, visible classification pill, tools section, side TOC, and metadata panel.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 05 / How and Why OCI's Technical Performance Is Real`.
- Current hero pattern: `.hero` and `.hero-grid` with hero actions and article metadata.
- Metadata present: Yes. Full head metadata, visible article metadata, source notes, and page metadata script are present.
- Reading tools present: Yes. Back to index, print/save, expand/collapse, reading mode, section copy links, and active TOC are present; no dedicated progress bar detected.
- Divergence: Low.
- Preserve: performance validation sections, technical evidence cards, limitations section, source conversion approach, and copy-link behaviour.

### Paper 06 - From ChatGPT To Enterprise AI

- Detected path: `paper-06-chatgpt-to-enterprise-ai/index.html`
- Current header/nav pattern: `.series-header`, global nav, breadcrumb text inside hero area, sidebar with metadata/tools/TOC.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 06 / From ChatGPT to Enterprise AI`.
- Current hero pattern: `.hero-wrap`, `.hero`, and `.hero-panel` with summary, takeaway, metadata, and sidebar.
- Metadata present: Yes. Full head metadata, visible sidebar metadata, source notes, and page metadata script are present.
- Reading tools present: Yes. Back to index, copy section link, print/save, expand/collapse, reading mode, and TOC are present; no progress indicator detected.
- Divergence: Low.
- Preserve: expectation-gap framing, enterprise friction evidence, AI accountability structure, related papers, and reading-mode toggle.

### Paper 07 - The Miracle Of AI: From Probabilistic Foundations

- Detected path: `paper-07-miracle-of-ai-probabilistic-foundations/index.html`
- Current header/nav pattern: `.utility-bar`, `header.site-header`, `.nav-links`, breadcrumb nav, side rail with metadata/tools/TOC.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 07 / The Miracle of AI: From Probabilistic Foundations`.
- Current hero pattern: `.hero` with `.hero-panel`, hero content, summary, and metadata side rail.
- Metadata present: Partial. Visible metadata is strong, but head metadata lacks robots, series, paper-number, paper-version, and conversion-version.
- Reading tools present: Yes. Back to index, copy page link, print/save, expand/collapse, reading mode, TOC, and anchor links are present; no progress indicator detected.
- Divergence: Medium.
- Preserve: probability-to-trust pathway, governance framing, details sections, anchor links, and internal-only source note.

### Paper 08 - AI Risks And Cloud Realities

- Detected path: `paper-08-ai-risks-and-cloud-realities/index.html`
- Current header/nav pattern: `.utility` banner, `.series-nav`, visible classification pill, content-first article with side rail for tools/metadata.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: informal text in the header: `Series index / Paper 08 / AI Risks and Cloud Realities`; no formal breadcrumb nav detected.
- Current hero pattern: `.hero` and `.hero-grid` with article title, subtitle, and side/context panels.
- Metadata present: Yes. Full head metadata, visible article metadata, source notes, and page metadata script are present.
- Reading tools present: Yes. TOC, back to index, print/PDF, expand/collapse, reading mode, metadata panel, and anchor links are present; no copy-page tool or progress indicator detected.
- Divergence: Medium.
- Preserve: risk-domain matrix, regulation/governance mapping, AI mini-series positioning, caveat to revalidate live claims, and anchor-link structure.

### Paper 09 - The Mechanics Of Public Sector Procurement

- Detected path: `paper-09-public-sector-procurement-mechanics/index.html`
- Current header/nav pattern: `.utility-bar`, `.series-header`, breadcrumb nav, side rail with TOC, metadata card, and tools card.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 09 / The Mechanics of Public Sector Procurement`.
- Current hero pattern: `.hero-wrap` and `.article-hero` with hero content, summary, card, and classification chip.
- Metadata present: Yes. Full head metadata, visible metadata card, source notes, and page metadata script are present.
- Reading tools present: Yes. Back to index, copy page link, print/save, expand/collapse, TOC, and section copy links are present; no progress indicator detected.
- Divergence: Low.
- Preserve: procurement decision gates, routes-to-market treatment, assurance checkpoints, section copy links, and source-derived caveats.

### Paper 10 - Aligning OCI To UK Public Sector Policy

- Detected path: `paper-10-aligning-oci-uk-public-sector-policy/index.html`
- Current header/nav pattern: `.utility-bar`, `.series-header`, `nav.primary-nav`, breadcrumb nav, sidebar tools, metadata panel, and TOC.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 10 / Aligning OCI to UK Public Sector Policy`.
- Current hero pattern: `.hero` with `.hero-shell`, subtitle, summary, takeaway, stats, and hero-bottom metadata.
- Metadata present: Yes. Full head metadata, visible metadata panel, source notes, and page metadata script are present.
- Reading tools present: Yes. Progress, back to index, copy section link, print/save, expand/collapse, reading mode, sector filters, and active TOC are present.
- Divergence: Low.
- Preserve: policy landscape framing, sector filters, filename-version caveat, role-safe compliance language, and source notes.

### Paper 11 - The Real Economics Of OCI

- Detected path: `paper-11-real-economics-of-oci/index.html`
- Current header/nav pattern: `.utility-bar`, `.series-header`, `.global-nav`, breadcrumb, metadata panel, reading tools, sidebar TOC, and next/previous navigation.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 11 / The Real Economics of OCI`.
- Current hero pattern: `.hero` and `.article-hero` with hero grid, economics chips, summary, and metadata.
- Metadata present: Yes. Full head metadata, visible metadata panel, source notes, and page metadata script are present.
- Reading tools present: Yes. Progress, back to index, copy page link, print/save, expand/collapse, reading tools, and active TOC are present.
- Divergence: Low.
- Preserve: economics caveats, FinOps/procurement/sustainability framing, comparison tables, and "not universally cheapest" warning.

### Paper 12 - OCI's Rich Differentiation

- Detected path: `paper-12-oci-rich-differentiation/index.html`
- Current header/nav pattern: `.utility-bar`, `.series-header`, `.top-nav`, breadcrumb div, tools band, later TOC aside, and source metadata section.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / All papers / Paper 12 / OCI's Rich Differentiation`, though the page currently displays mojibake for the apostrophe in some text.
- Current hero pattern: `.hero`, `.hero-card`, `.hero-grid`, micro metadata grid, and hero summary.
- Metadata present: Yes. Full head metadata, micro metadata snapshot, source and handling notes, and page metadata script are present.
- Reading tools present: Yes. Back to index, print/save, expand/collapse, reading mode, section copy buttons, and TOC are present; no progress indicator detected.
- Divergence: Medium.
- Preserve: rich differentiation argument, nuance zones, metadata/source-handling section, anchor-copy controls, and reading mode.

### Paper 13 - Misconceptions Of OCI

- Detected path: `paper-13-misconceptions-of-oci/index.html`
- Current header/nav pattern: `.utility-bar`, `.series-header`, series navigation, breadcrumb nav, hero, TOC/tools side rail, metadata section, and footer.
- Current classification wording: head metadata and visible page text use `Confidential - Oracle Internal`.
- Current breadcrumb pattern: `Series / Paper 13 / Misconceptions of OCI`.
- Current hero pattern: `.hero`, `.hero-card`, `.hero-grid`, subtitle, hero summary, and key takeaway.
- Metadata present: Yes. Full head metadata, visible source metadata section, source notes, footer metadata, and page metadata script are present.
- Reading tools present: Yes. Progress, TOC, back to index, copy section link, print/save, expand/collapse, misconception filters, and active TOC are present.
- Divergence: Low.
- Preserve: misconception filters, response taxonomy, source metadata section, current bounded-evidence tone, and last-reviewed footer note.

## Key Risks

- The master spec was inferred from current repo patterns because the spec file was empty at audit start. Later tranches should confirm the inferred target before broad HTML edits.
- Classification wording is mostly consistent, but the year-in-review hub uses a stronger label and has malformed visible text with a stray backslash.
- Paper 04 lacks core head metadata even though its visible body metadata is strong.
- Paper 07 has strong visible metadata but incomplete head metadata.
- Several pages use different URL styles (`../index.html`, `../`, `/index.html`, `/`) that may behave differently depending on hosting path.
- Paper 12 contains mojibake in visible/title text for the apostrophe in `OCI's`.
- Reading tools are functionally present on most pages, but button names, placement, copy behaviours, and progress indicators differ.

## Recommended Implementation Order

1. Confirm classification policy and companion-page exception handling, especially for the year-in-review hub.
2. Fix high-divergence metadata/classification issues first: Paper 04 and the year-in-review hub.
3. Bring incomplete head metadata into line next: Paper 07, then any companion metadata needed for the hub.
4. Harmonise breadcrumb patterns on medium-divergence pages: Paper 01, Paper 08, and Paper 12.
5. Standardise reading-tools wording and placement while preserving local tools such as profile filters, sector filters, and misconception filters.
6. Normalize link style for index/source anchors after confirming the intended deployment base path.
7. Leave article-specific visual/body treatments until a later tranche, after the shared shell is stable.
