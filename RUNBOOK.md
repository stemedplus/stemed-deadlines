# Runbook: Deadlines

This board uses the shared STEMEd+ pipeline. For how every board works and the common fixes, see the [stemedplus-theme runbook](https://github.com/stemedplus/stemedplus-theme/blob/main/RUNBOOK.md).

| | |
|---|---|
| **Site** | stemedplus.github.io/stemed-deadlines |
| **Repository** | stemedplus/stemed-deadlines |
| **Updates** | Daily at 13:41 UTC, after the boards it reads have built, on push, and by hand (`update.yml`) |
| **Sources** | The deadline calendars (`feeds/deadlines.ics`) of Funding, Awards, Conferences, and Professional Development, listed in `config/sources.json`. If one can't be reached, its deadlines from the last published `deadlines.json` are kept. |
| **Build** | `python -m stemed_deadlines --out output` |
| **Add or fix** | Fix the listing on the source board; Deadlines picks it up the next day |

**A deadline is missing:** check that it's on the source board first. If a source board's address changes, update `config/sources.json`. Add a new board by adding it, with its `ics` address, to `config/sources.json`.

_Written November 2026. Review with the yearly December review._
