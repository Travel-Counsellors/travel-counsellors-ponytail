---
name: ponytail-review
description: >
  Cursor-only over-engineering review for Travel Counsellors Ponytail. Use
  when the user asks for a Ponytail review, simplify review, review for
  over-engineering, what can we delete, or whether a diff is too complex.
license: MIT
---

# Travel Counsellors Ponytail Review

Review the current diff or requested files only for unnecessary complexity. Find what to delete, replace with existing code, or shrink.

## Findings

Lead with findings. Use one line per issue:

`<file>:<line>: <tag>: <what to cut>. <replacement>.`

Tags:

- `delete`: dead code, speculative feature, unused flexibility. Replacement: nothing.
- `reuse`: hand-written code duplicates something already in the repo. Name the existing helper/pattern.
- `stdlib`: hand-written code duplicates the language or standard library. Name the API.
- `native`: dependency or custom code duplicates a platform feature. Name the feature.
- `yagni`: abstraction, config, interface, or layer has no current need.
- `shrink`: same behavior can be expressed more clearly with less code.

End with `net: -<N> lines possible.` If there is nothing worth cutting, say `Lean already. Ship.`

## Boundaries

This is not a general correctness or security review. Do not flag essential validation, accessibility, security checks, data-loss handling, or the smallest useful test.
