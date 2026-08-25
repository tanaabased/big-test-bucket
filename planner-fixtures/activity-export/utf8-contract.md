# UTF-8 activity CSV contract fixture

This disposable fixture records the expected escaping behavior for
`PMPT-ACTIVITY-EXPORT-20260825`.

| Input value | Encoded CSV field |
| --- | --- |
| `café` | `café` |
| `alpha,beta` | `"alpha,beta"` |
| `say "hello"` | `"say ""hello"""` |
| `first` plus a line break plus `second` | one quoted field containing the line break |

The values must round-trip through a standards-compliant CSV parser without
changing UTF-8 text or splitting an escaped field into additional columns.

This is live-test evidence only. Remove it through a follow-up pull request
when the cleanup task for this planner run is executed.
