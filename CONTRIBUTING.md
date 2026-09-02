# Contributing to libforge libraries

## AI disclosure

This fleet is agent-assisted and human-approved. Commits carry an
`Assisted-by` trailer; every release PR is merged by a human after
independent review. Nothing publishes without that gate.

## Flow

- Branch off main. Conventional Commits only (`feat:`, `fix:`, `chore:`) -
  release-please derives versions and changelogs from them.
- Zero runtime dependencies is a hard rule. Zero install scripts too.
- Tests must cover the public API. `npm test` / `python -m unittest` / `cargo test`.
- ASCII hyphens only in all copy (no en/em dashes).
