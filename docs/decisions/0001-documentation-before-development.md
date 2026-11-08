# ADR 0001: Documentation before development

**Status:** Accepted

## Context

Most project failures I have seen were not caused by technology limitations. They came from unclear requirements, insufficient architecture, poor documentation, a lack of systems thinking, and excessive complexity. Work on this platform is also done with AI systems as engineering partners, and AI works best from a clear written intent.

## Decision

Every change follows the same sequence: **Understand → Document → Design → Review → Implement → Validate → Improve.**
Each revision begins as a written request that states the goal, the scope, and the expected outcome. The implementation follows the document, and the document is updated when the implementation teaches something new.

## Consequences

- Changes are traceable to a written intent and a revision number.
- AI collaboration is guided by human intention, not by improvised prompts.
- Writing comes first, so small changes take a little longer to start and much less time to review, transfer, and maintain.
