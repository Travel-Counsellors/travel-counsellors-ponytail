# Travel Counsellors Ponytail

Cursor plugin that keeps agents lazy in the good way: reuse existing code, prefer standard libraries and platform features, and ship the smallest correct diff.

## Install

Clone into your local Cursor plugins directory:

```bash
git clone https://github.com/Travel-Counsellors/travel-counsellors-ponytail.git \
  ~/.cursor/plugins/local/travel-counsellors-ponytail
```

Reload Cursor with **Developer: Reload Window**, then enable the plugin under **Customize**.

## Skills

| Skill | Purpose |
| --- | --- |
| `/travel-counsellors-ponytail` | Simplest correct solution mode |
| `/travel-counsellors-ponytail-review` | Review a diff for over-engineering |
| `/travel-counsellors-ponytail-audit` | Scan a repo for unnecessary complexity |
| `/travel-counsellors-ponytail-debt` | List deliberate `ponytail:` shortcuts |
| `/travel-counsellors-ponytail-help` | Show this reference |

Natural language also works: "TC Ponytail", "lazy mode", "YAGNI", or "review for over-engineering".

## Optional rule

Enable `travel-counsellors-ponytail` from **Customize** when the team wants the guidance available without invoking a skill.

## Attribution

Adapted from [Ponytail](https://github.com/DietrichGebert/ponytail) by Dietrich Gebert (MIT).
