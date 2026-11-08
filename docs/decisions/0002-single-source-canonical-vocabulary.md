# ADR 0002: One source for the canonical vocabulary

**Status:** Accepted

## Context

The ecosystem depends on exact wording. The canonical philosophy, the ecosystem statement, the names of the foundational documents, and their definitions appear on many pages, in PDFs, and in AI-readable files. Copying text by hand meant that every revision risked leaving an old phrase behind somewhere.

## Decision

Every canonical statement, name, and definition is defined once in a single source module. Pages refer to it through named tokens, and the PDF and AI-readable outputs are generated from the same source. Pages do not restate canonical text in their own words.

## Consequences

- A change of wording is made once and reaches every page and format.
- Tests check that canonical statements appear where they should and that retired wording does not return.
- Content authors work with tokens as well as prose, which takes a short learning step.
