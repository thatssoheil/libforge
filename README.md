# libforge

Self-creating library forge for [thatssoheil](https://github.com/thatssoheil).

One hub, many tiny libraries. Each spoke repo is generated from the copier
templates in this repo, tested, independently reviewed, then published by a
human-approved release PR - never by the agent.

## The fleet

| Library | Ecosystems | Status | Badges |
|---------|------------|--------|--------|
| - | - | - | - |
## How a library is born

1. An idea lands in `forge-queue.jsonl` (agent triage findings + owner ideas).
2. The forge run (daily 12:00) picks the oldest, namechecks it across
   npm / PyPI / crates.io / GitHub, and scaffolds it from a template here.
3. The agent implements a minimal zero-dependency core with real tests.
4. An independent reviewer sees only the diff and returns APPROVE/REJECT.
5. The repo is created and CI must be green. `release-please` opens release PRs.
6. A human merges the release PR - that merge, not the agent, is the publish gate.

## Brand: auditability

Every library here is zero runtime dependencies, zero install scripts,
auditable in one sitting, and built with AI assistance under human review
and approval. Provenance proves origin, not safety - so we optimize for
the thing you can actually check: small code you can read before you trust it.

## License

MIT
