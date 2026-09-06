# FINE ART F2 SB

ADT Studio conversion workspace for the book **FINE ART F2 SB**.

The repository-local `adt-book-conversion` skill is installed under
`.agents/skills/adt-book-conversion`. The complete 112-page accessible HTML
conversion is published under `books/fine-art-f2-sb/adt/`.

## Open the converted book

Serve the repository over HTTP, then open:

```text
books/fine-art-f2-sb/adt/index.html
```

For example: `python3 -m http.server` from the repository root.

## Source book

The source PDF and rebuildable ADT Studio caches/intermediate assets are kept
outside Git. The checked-in `adt/` bundle is self-contained for publication.
