# Branching Model

This doctrine applies to the libforge hub and to EVERY library it produces.
It is kept identical everywhere so any repo in the fleet reads the same way.

## Branches

| Branch | Purpose | Rules |
|--------|---------|-------|
| `main` | Always releasable | CI must be green. No direct pushes - everything lands via PR. |
| `feat/<slug>` | New features, new libraries | PR into `main`, squash-merge. |
| `fix/<slug>` | Bug fixes | PR into `main`, squash-merge. |
| `chore/<slug>` | Tooling, docs, deps | PR into `main`, squash-merge. |

## Commit and merge discipline

- Conventional Commits titles (`feat:`, `fix:`, `chore:`) - release-please
  derives versions and changelogs from them.
- Squash-merge only: one clean commit per PR on `main`.
- The producing agent may merge its own PR only after BOTH:
  1. independent fail-closed review returns APPROVE, and
  2. required CI checks are green.
- Releases: release-please opens a release PR from `main`. A human merging
  that PR is the only publish path to npm/PyPI/crates. The agent never
  publishes, never pushes tags.

## Test bar before anything lands

No scaffold-stub tests at ship time. The suite covers every documented
behavior and failure mode of the public API, deterministic (injected
sleep/clock where timing exists), and green locally AND in CI.

## AI disclosure

This fleet is agent-assisted and human-approved. Commits carry an
`Assisted-by` trailer; every release PR is merged by a human.
