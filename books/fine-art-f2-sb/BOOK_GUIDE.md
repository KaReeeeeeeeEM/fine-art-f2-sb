# FINE ART F2 SB - visual conversion contract

## Source and page frame

- Source: `FINE ART F2 SB.pdf`, an Adobe InDesign print PDF with 112 physical pages.
- Fixed page: 557.906 x 767.669 pt; reference viewport: 558 x 768 px; aspect ratio: 0.727.
- Main pages use a repeated turquoise top wave and turquoise/magenta bottom wave. The normal text frame is approximately x=48-510 pt, between the top banner and footer.
- Folios are centered in a magenta device near the bottom edge. Running book and chapter labels sit in small cream tabs and alternate sides with page parity.
- Printed numbering begins after six front-matter pages, so physical page 7 is printed page 1.

## Page taxonomy and repeating components

| Family/component | Canonical physical pages | Required source behavior |
|---|---:|---|
| Cover | 1 | Centered magenta/teal title stack, certificate artwork, publisher line, and visible production marks. |
| Copyright/front matter | 2, 5, 6 | Open white composition; source-aligned credits and contact columns; footer retained where present. |
| Table of contents | 3-4 | Two-page contents with semantic leaders and a shared right-aligned number boundary. |
| Standard running shell | 8, 26, 43, 71, 86, 110 | Turquoise/magenta waves, alternating running tabs, centered magenta folio, and source content margins. |
| Chapter opener | 7, 25, 41, 70, 85 | Magenta chapter-number block, pale-pink title band, cyan introduction panel, Think prompt, and first section. |
| Exercise bar | 10, 21, 29, 44, 72, 80, 95, 104 | Teal title strip over a pale blue-grey question panel with consistent padding and source numbering. |
| Activity panel | 9, 12, 19, 38, 42, 75, 84, 89, 107 | Pink circular activity icon and pale-pink rounded prompt panel; continuation behavior must remain aligned. |
| Revision exercise | 24, 38-40, 67-69, 83-84, 108-109 | Large pale-pink question/table panels; borders, blanks, and option columns remain semantic and aligned. |
| Tables | 24, 40, 68, 84, 109 | Magenta headers and rules; stable column edges, complete cell text, and no text overlap. |
| Figure-heavy content | 8-18, 26-37, 42-66, 71-82, 86-106 | Preserve genuine artwork, photographs, diagrams, labels, crop, caption, scale, and z-order without duplicate visible text. |
| Perspective/process diagrams | 32, 51-60, 74, 78-80, 94-106 | Maintain ordered steps, same-baseline labels, arrows/guide lines, and exact figure placement. |
| Multi-column/tool layouts | 74, 86-88 | Preserve independent columns and gutters; captions and body text must not cross columns. |
| Glossary | 110 | Dense term-definition layout with teal term labels and stable left boundary. |
| Bibliography | 111-112 | Single-column references under the standard shell, preserving entry order and wrapping. |

## Source-backed design tokens

- Primary turquoise: repeated waves, section headings, exercise bars, and glossary terms.
- Primary magenta/pink: chapter blocks, activity icons/panels, revision panels, rules, and folio device.
- Pale cyan/blue-grey: introductions and exercise content areas.
- Body typography: Times New Roman family; Book Antiqua Bold for selected headings; Abadi MT Condensed Extra Bold and Helvetica/Arial for compact labels; Cambria Math for mathematical glyphs. Use bundled source fonts when available or measured metric-compatible fallbacks.
- Preserve extracted font size, weight, line height, baselines, and inline emphasis. Never globally shrink typography to solve a local collision.
- Component geometry is source-positioned. Registration/crop marks visible in the supplied PDF are retained, not invented.

## Canonical pilot and regression set

Pilot physical pages: 1, 3, 7, 10, 24, 32, 40, 41, 52, 67, 70, 74, 85, 92, 102, 109, 110, and 112.

This set covers the unique cover, contents, every chapter-opener pattern, standard text/figure pages, exercises, activities, revision panels, tables, perspective geometry, multi-column tools, long procedural sequences, glossary, and final bibliography. Any shared renderer/runtime/configuration correction must be rechecked on the affected canonical page and at least one earlier canonical page. New component variants discovered during expansion must be added here before conversion continues.

## Fixed-layout acceptance rules

- Every positioned box stays within 557.906 x 767.669 pt and preserves the source baseline/order.
- Source single-line headings, labels, captions, and contents rows remain single-line.
- Contents and table number columns share measured right edges; dotted leaders are visual and silent in TTS.
- Overlapping raster/vector crops must not visibly duplicate semantic text.
- Read-aloud order follows visual-semantic order and word highlighting must not alter text, wrapping, or geometry.

## Accepted exceptions

- Physical page 1 is a unique cover.
- Front matter pages 2-6 vary in use of the running shell.
- Figure sizes and white space vary by source page and should not be normalized into a generic layout.
