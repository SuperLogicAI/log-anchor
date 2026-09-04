# safe-router-anchor

Append-only anchor store for `safe_router`'s log hash chain
(SPEC.md §11 Q4). Each commit adds one `head.json` (or equivalent)
containing the current log-head hash and row id — nothing else.
No client data, no request/response content, ever.

Pushed on an interval by `safe-router anchor` + a launchd job on the
router host. Branch protection on `main` blocks force-push and
deletion so history here can't be silently rewritten.
