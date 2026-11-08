# ADR 0004: One publication, two formats, verified parity

**Status:** Accepted

## Context

Every publication can be read online or downloaded as a PDF. A reader should receive the same content regardless of format. PDFs produced by hand become legacy snapshots as soon as the website changes.

## Decision

PDFs are generated from the same sources as the web pages, never edited separately. Each PDF carries its publication metadata (Published, Updated, Revision) in the footer and in the document properties. Before release, an automated check extracts the text of each PDF and confirms that the web version's content is present in it, section by section.

## Consequences

- Website version = PDF version, and the claim is checked rather than assumed.
- Print-specific defects, such as clipped table columns or lost paragraphs, are caught before publication.
- Regenerating the library is a routine step of every content revision.
