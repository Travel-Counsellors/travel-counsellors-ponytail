---
name: travel-counsellors-ponytail-debt
description: >
  Collect `ponytail:` comments into a debt ledger. Use when the user asks what
  shortcuts were deferred, wants the Ponytail debt ledger, or asks to list
  deliberate simplifications.
license: MIT
---

# Travel Counsellors Ponytail Debt

Collect deliberate `ponytail:` shortcuts into a ledger so temporary simplifications do not become invisible.

## Scan

Search the repo for comment markers such as:

```text
ponytail:
```

Skip dependency folders, build output, and `.git`.

## Output

Group by file:

`<file>:<line>, <what was simplified>. ceiling: <limit>. upgrade: <trigger>.`

Flag any marker without a clear revisit trigger as `no-trigger`.

End with `<N> markers, <M> with no trigger.` If none exist, say `No ponytail: debt. Clean ledger.`

## Boundaries

Read and report only. If the user asks to persist the ledger, write it to `PONYTAIL-DEBT.md`.
