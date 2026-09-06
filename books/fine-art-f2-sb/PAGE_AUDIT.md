# Page fidelity audit

Source: `/Users/kareem/Documents/SECONDARY-ADT/NOT-CONVERTED/FINE ART F2 SB/FINE ART F2 SB.pdf`

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
- Pages 81 and 103 were rechecked after packaging completed; their images load
  correctly (the initial failures occurred while files were still being copied).
- Small out-of-frame fragments are intentional source crop/registration marks,
  not clipped instructional content.
