# Portfolio Doctrine

How a library gets into this fleet. Read this before trusting why a library
exists here - it is the selection bar, made public.

## Two prongs (owner directive 2026-09-03)

The fleet builds PIONEERING tools, not duplicates. Every candidate must pass a
concept-level gap check (`libforge gapcheck`) BEFORE any scaffold:

**Prong 1 - genuine gaps.** A niche that is genuinely unserved and makes a real
difference. `gapcheck <concept>` (default): if an established, maintained
package already does the core thing, the idea is a duplicate -> HOLD unless we
have a sharp documented differentiator.

**Prong 2 - comparison-table beats.** A defensible simplification of an
established heavy library, winning on a real axis. `gapcheck <concept>
--beat <incumbent>`: the incumbent is the TARGET, not a blocker. The
differentiator must be MEASURED (KB size, dependency count, hot-path speed, no
build step) - never a rename. We never re-serve an already-optimal library
(e.g. picomatch, semver - already tiny).

## Why (the politefetch lesson)

`politefetch` appeared to have a free name (exact-match 404 on every registry)
but collided with the established `polite-fetch` (created 2026-06-06, same
purpose). npm's similarity guard blocked it. Exact-name availability is NOT
coverage of a niche -> the guard is a stage-0 requirement now.

## The bar

- Zero runtime dependencies. Zero install scripts. No build step. Pure ESM.
- Auditable in one sitting: the core is one self-contained file.
- AI-assisted, but every release is human-approved (owner merges the release PR).
- Tests prove every documented behavior and failure mode; a documented deviation
  is stated, never silent.

## Selection, live

The active champion is decided by evidence: measured gap-check + a real
differentiator + name safety across all registries. See forge-queue.jsonl in
this repo for the log and each idea's verdict.
