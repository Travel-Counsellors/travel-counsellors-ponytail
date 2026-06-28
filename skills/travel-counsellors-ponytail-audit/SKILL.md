---
name: travel-counsellors-ponytail-audit
description: >
  Repo-wide Travel Counsellors Ponytail audit for over-engineering. Use when
  the user asks to audit a codebase for bloat, find what can be deleted,
  simplify the repo, or run a Ponytail audit.
license: MIT
---

# Travel Counsellors Ponytail Audit

Scan the codebase for unnecessary complexity and rank the biggest useful cuts first.

## Hunt

Look for:

- Dead code, dead flags, and unused configuration.
- Single-implementation interfaces, factories with one product, and layers with one caller.
- Wrappers that only delegate.
- Hand-written standard-library or platform features.
- New dependencies used for trivial behavior.
- Repeated local code where an existing helper or component already exists.

## Output

One line per finding, ranked by impact:

`<tag>: <what to cut>. <replacement>. [path]`

Use the same tags as `travel-counsellors-ponytail-review`: `delete`, `reuse`, `stdlib`, `native`, `yagni`, `shrink`.

End with `net: -<N> lines, -<M> deps possible.` If there is nothing meaningful to cut, say `Lean already. Ship.`

## Boundaries

Report only. Do not apply fixes unless the user asks. Do not recommend removing validation, accessibility, security, data-loss handling, or the smallest useful test.
