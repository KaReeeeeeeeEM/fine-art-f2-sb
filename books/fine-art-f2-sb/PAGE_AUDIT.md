# Page fidelity audit

Source: `/Users/kareem/Documents/SECONDARY-ADT/NOT-CONVERTED/FINE ART F2 SB/FINE ART F2 SB.pdf`

Reference viewport: 558 x 768 px. Physical page numbers, printed folios, ADT page IDs, and output filenames must be recorded separately after extraction.

| Physical page | Family | First web-render pass | Final package pass | TTS/highlight gate | Notes |
|---:|---|---|---|---|---|
| 1-12 | Front matter, contents, introduction | Pass | Pass | Pass | Pilot reviewed individually; malformed TOC leaders on physical page 3 normalized to dots and removed from narration. |
| 13-112 | Chapters, activities, exercises, figures, tables, revision, glossary | Pass | Pass | Pass | All pages compared in source/output contact sheets; no blank pages, missing figures, or material shifts found. |

## Automated package checks

- 112 HTML page documents present.
- 0 missing local `src`/`href` targets.
- 0 U+FFFD replacement characters or backspace controls.
- 0 duplicate `data-adt-reading-order` values within pages.
- Pages 81 and 103 were rechecked after packaging completed; their images load
  correctly (the initial failures occurred while files were still being copied).
- Small out-of-frame fragments are intentional source crop/registration marks,
  not clipped instructional content.
