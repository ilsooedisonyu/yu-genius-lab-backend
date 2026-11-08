# ADR 0003: Architectural boundaries enforced by automated contracts

**Status:** Accepted

## Context

Most failures emerge at boundaries. In a codebase, boundaries erode quietly: one shortcut import at a time, each reasonable on its own. A layered design that exists only in a diagram does not survive many revisions, especially when AI systems generate part of the code.

## Decision

The platform is layered: presentation, services, repositories, and domain models, with framework-independent renderers and an isolated kernel of shared primitives. The dependency rules are written as architecture contracts and run with the test suite:

- presentation never touches persistence directly;
- modules use one another only through their public interfaces;
- renderers never import the web framework;
- the kernel depends on nothing above it.

A change that breaks a rule fails the build.

## Consequences

- The architecture stays true to its diagram across revisions, whoever or whatever wrote the change.
- Boundary questions are settled by the contracts, so reviews can focus on design.
- Adding a new module means declaring its place in the layers first, which is the point.
