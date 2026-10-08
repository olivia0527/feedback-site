# Issue tracker: Local Markdown

Issues and specs for this repo live as markdown files in `.scratch/`.

## Conventions

- One feature per directory: `.scratch/<feature-slug>/`
- The spec is `.scratch/<feature-slug>/spec.md`
- Implementation issues are one file per ticket at `.scratch/<feature-slug>/issues/<NN>-<slug>.md`, numbered from `01`, never a single combined tickets file
- Triage state is recorded as a `Status:` line near the top of each issue file
- Comments and conversation history append to the bottom of the file under a `## Comments` heading

## Publishing and fetching

- When a skill says to publish to the issue tracker, create the appropriate file under `.scratch/<feature-slug>/`, creating directories as needed.
- When a skill says to fetch a ticket, read the referenced Markdown path or issue file.

## Wayfinding operations

- Map: `.scratch/<effort>/map.md`, containing Notes, Decisions-so-far, and Fog.
- Child ticket: `.scratch/<effort>/issues/NN-<slug>.md`, numbered from `01`, with a `Type:` line (`research`, `prototype`, `grilling`, or `task`) and a `Status:` line (`claimed` or `resolved`).
- Blocking: use a `Blocked by: NN, NN` line near the top. A ticket is unblocked when every listed file is resolved.
- Frontier: scan `.scratch/<effort>/issues/` for open, unblocked, unclaimed files; choose the first by number.
- Claim: set `Status: claimed` and save before starting work.
- Resolve: append the answer under `## Answer`, set `Status: resolved`, then append a context pointer to the map's Decisions-so-far in `map.md`.
