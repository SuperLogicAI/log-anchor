# log-anchor

Append-only anchor store for a hash chain. Each commit adds one
`head.json` containing a chain-head hash and a row id — nothing else.
No sensitive content, no request/response data, ever.

Pushed on an interval by an offline anchoring job. Branch protection
on `main` blocks force-push and deletion so this history can't be
silently rewritten.
