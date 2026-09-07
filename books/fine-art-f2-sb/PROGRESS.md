# Conversion progress

## 2026-09-06

- Resolved source PDF and confirmed 112 physical pages at 557.906 x 767.669 pt.
- Surveyed all pages using low-resolution contact sheets.
- Classified recurring page families and selected an 18-page canonical pilot/regression set.
- Selected book-local `fixed_layout` rendering and disabled generated interstitial quizzes.
- Completed the ADT Studio pipeline for all 112 physical pages.
- Generated fixed-layout HTML, image descriptions, glossary, table of contents,
  easy-read content, 2,463 speech items, synchronized word highlighting, and
  accessibility assessments.
- Corrected malformed InDesign table-of-contents leader characters in both the
  visual renderer and speech normalization, then reran the affected stages.
- Compared all 112 packaged pages with the source using full-book contact sheets.
- Verified 112 HTML pages, zero missing local references, zero malformed control
  or replacement characters, and no duplicate reading-order identifiers.
- Verified representative playback/highlight behavior without text reflow or
  geometry movement.
- Final package: `adt/index.html`.
- Reworked fixed-layout extraction/rendering rules for the reported front matter
  and printed pages 2, 5, 7, 9, 10, 12, 18, 29, 34, 59, and 62, then applied the
  same systemic fixes across the complete book.
- Regenerated the complete pipeline successfully: 112/112 pages extracted and
  structured, 112/112 captions and accessibility assessments, and 3,322/3,322
  speech items.
- Verified the requested-page set in the packaged browser runtime, including the
  source top/bottom page furniture and the corrected revision/table pages.
- Restored content hidden by contradictory composite-crop clipping, including
  the complete introduction on printed page 1 and Exercise 1.3 on printed page 6.
- Aligned semantic duplicate suppression with the actually visible header crop,
  regenerated all 112 pages, and completed a browser scan from physical page 7
  through page 112 for the same failure pattern.

## 2026-09-07

- Corrected printed page `(iii)` and the continuing contents page to use the
  source-width leader rows and one measured, right-aligned page-number column.
- Kept top/bottom page furniture visible while excluding its labels and folios
  from accessibility narration and packaged audio.
- Converted TOC Roman folios to their numeric values in TTS input while
  preserving Roman glyphs in the visible page; verified the generated audio.
- Regenerated and checked the complete 112-page web package successfully.
- Regenerated read-aloud output from the latest text catalog so every meaningful
  image description is included in speech. Verified 139 image descriptions and
  139 corresponding audio files, with no missing image narration.
- Restored the cover Certificate of Approval narration in its visual reading
  position after the title hierarchy and before the publisher line.
- Completed an anti-facsimile audit across all 112 packaged pages. Removed the
  three large text-bearing page crops on physical pages 39, 41, and 109 and
  replaced their visible content with selectable HTML plus CSS-built panels.
