# Liam's Case

A zero-build GitHub Pages manuscript reader.

## Manuscript workflow

The site is driven by two files:

- `index.html` — landing page, cover art, Markdown renderer, listening controls, sharing, counters, and reading/listening progress.
- `manuscript.md` — the manuscript content.

To replace the manuscript, replace the contents of `manuscript.md`. No changes to `index.html` are required.

The reader fetches `./manuscript.md` from the same repository at runtime, converts it from Markdown to HTML, sanitizes it, and then builds its narration blocks from the rendered headings, paragraphs, and list items.

### Recommended Markdown structure

```md
# Book Title

## Chapter or major section

Normal prose paragraph.

### Subheading

More prose.
```

The first `#` heading is used automatically as the visible title and browser title.

## Hosting

The site is static and is ready for GitHub Pages from the repository root on the `main` branch.

No package install, compilation, server, database, or build step is required.
