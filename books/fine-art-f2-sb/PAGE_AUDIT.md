# Page fidelity audit

Source: `FINE ART F2 SB.pdf`

Reference viewport: 558 x 768 px. Physical page numbers, printed folios, ADT page IDs, and output filenames must be recorded separately after extraction.

| Physical page | Family | First web-render pass | Final package pass | TTS/highlight gate | Notes |
|---:|---|---|---|---|---|
| 1-12 | Front matter, contents, introduction | Pass | Pass | Pass | Pilot reviewed individually; malformed TOC leaders on physical page 3 normalized to dots and removed from narration. |
| 13-112 | Chapters, activities, exercises, figures, tables, revision, glossary | Pass | Pass | Pass | All pages compared in source/output contact sheets; no blank pages, missing figures, or material shifts found. |

## 2026-09-06 reported-page regression audit

- User-facing folios `(ii)`, `(iii)`, `(iv)`, `(v)`, `2`, `5`, `7`, `9`, `10`,
  `12`, `18`, `29`, `34`, `59`, and `62` map to physical PDF pages 2, 3, 4,
  5, 8, 11, 13, 15, 16, 18, 24, 35, 40, 65, and 68.
- Repaired systemic same-baseline and large horizontal-jump merging so adjacent
  table/list columns remain separate positioned text blocks.
- Repaired partial running-header/footer raster handling so decorative furniture
  no longer duplicates or suppresses nearby semantic text.
- Removed malformed tight-bbox footer background fragments that produced false
  vertical colour bars while preserving the source cyan/magenta/beige page frame.
- Repackaged all 112 pages and inspected every requested page in the packaged
  browser runtime. All requested pages have zero broken images, replacement
  characters, out-of-page semantic text boxes, or visually unintended text
  overlaps. Physical pages 15, 40, and 68 produced conservative bounding-box
  intersections; visual inspection confirmed these are normal adjacent source
  lines/columns rather than painted overlaps.
- Physical page 24 (printed page 18) received an additional narrow-header crop
  correction and was rechecked visually after regeneration.

## Automated package checks

- 112 HTML page documents present.
- 0 missing local `src`/`href` targets.
- 0 U+FFFD replacement characters or backspace controls.
- 0 duplicate `data-adt-reading-order` values within pages.
- 3,322 speech items and synchronized word-highlighting metadata packaged.

## 2026-09-06 hidden-content correction

- Printed pages 1 and 6 map to physical PDF pages 7 and 12.
- Removed erroneous lower-edge clipping from complete composite content panels;
  this restored the introduction on printed page 1 and the Exercise 1.3 question
  on printed page 6.
- Corrected raster-visibility bounds for clipped running headers so opening
  headings and first body lines remain visible as semantic text below the header.
- Regenerated the complete 112-page package and scanned physical pages 7-112 in
  the browser for broken images, replacement characters, and hidden semantic
  text lacking a visible raster counterpart.
- Visually reviewed all conservative scan candidates; pages 22, 24, 50, 59, and
  88 contain valid visible raster renditions rather than missing content.
- Pages 81 and 103 were rechecked after packaging completed; their images load
  correctly (the initial failures occurred while files were still being copied).
- Small out-of-frame fragments are intentional source crop/registration marks,
  not clipped instructional content.

## 2026-09-07 contents-page and narration correction

- Printed page `(iii)` maps to physical PDF page 3 (`pg003_sec001.html`).
- Restored every TOC leader row to the measured shared number edge: 472 px in
  the 558 px reference viewport. Main rows use `left: 86px; width: 386px` and
  indented rows use `left: 106px; width: 366px`.
- Regression-checked the continuation TOC on physical page 4; its hierarchy,
  leaders, and right-aligned number column remain consistent with the source.
- Decorative running labels and printed folios remain visually present but are
  marked presentational and omitted from the packaged read-aloud catalog.
- TOC dot leaders remain visual only. Terminal Roman folios are normalized to
  numeric values for speech; generated audio was transcribed as
  “Acknowledgments, five” and “Preface, six.”
- Removed the exposed PDF production timestamp text node from physical page 3.
- Full 112-page pipeline completed; package check found zero missing local
  `src`/`href` targets. Focused renderer/speech tests and repository typecheck pass.

## 2026-09-07 image-description speech audit

- Compared every meaningful image entry in the packaged English text catalog
  against the packaged audio map: 139 descriptions, 139 audio files, zero missing.
- Added the previously missing `pg001_im001` audio for the cover Certificate of
  Approval. Its narration identifies the issuing ministry, approval purpose,
  textbook and form, 2023 syllabus, date, signatory, and office.
- Transcribed the generated 26-second certificate audio to confirm the complete
  description is spoken. Decorative page furniture remains silent.

## 2026-09-07 anti-facsimile HTML audit

- Inspected all 112 packaged HTML files for canvases, embedded PDF viewers,
  CSS page backgrounds, page-sized rasters, hidden text, and large text-bearing
  image crops.
- Physical pages 39, 41, and 109 contained large raster composites painting
  ordinary textbook text. Removed those assets from the current versioned web
  render and reconstructed the pink panels, chapter blocks, and table rules in
  CSS while making the source text visible, selectable HTML.
- Browser verification at the 558 × 768 reference page size found 21, 19, and
  37 visible reading-order text nodes respectively, no large text raster, and
  no horizontal or vertical overflow. Page 68 independently retained 41 visible
  semantic text nodes and no large text raster.

## 2026-09-07 font-size consistency audit

- Confirmed the source hierarchy rather than forcing one size onto every role:
  body text is nominally 12 px, captions/source lines 10 px, contents rows
  11/13 px, and headings generally 16–20 px.
- Corrected runtime auto-fit, which had reduced some nominal 12 px paragraphs
  to approximately 7 px when extracted boxes were too narrow. Auto-fit now
  permits only modest metric compensation and restores the source size when
  the underlying geometry is substantially wrong.
- Browser-checked all 112 physical pages at the 558 × 768 reference geometry.
  Equivalent body-copy medians range from 11.5 to 12 px; no page median is
  below 11 px. Smaller remaining runs are intentional superscripts or distinct
  source roles.
