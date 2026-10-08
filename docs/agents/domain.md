# Domain Docs

This repository uses a single-context domain layout.

## Before exploring

- Read `GLOSSARY.md` at the repository root when it exists.
- Read ADRs under `docs/adr/` that touch the area being changed.
- If these files do not exist, proceed without creating them upfront; add them when domain terms or architectural decisions are actually resolved.

## File structure

```text
/
├── GLOSSARY.md
└── docs/adr/
    ├── 0001-example-decision.md
    └── 0002-another-decision.md
```

## Vocabulary and conflicts

- Use the glossary's terminology in issue titles, specs, refactor proposals, hypotheses, and tests.
- If a needed concept is not in the glossary, treat that as a signal to resolve whether it is a genuine domain gap before inventing a synonym.
- If a proposed change conflicts with an ADR, call out the conflict explicitly rather than silently overriding it.
