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
