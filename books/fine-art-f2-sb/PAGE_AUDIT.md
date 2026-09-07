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
