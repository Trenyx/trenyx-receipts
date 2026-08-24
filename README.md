# trenyx-receipts

The public, third-party-timestamped trail for **Model B — The Watchlist Book**
(https://trenyx-site.onrender.com/records/watchlist-book.html): one operator's
stock picks vs. 20 random shadow books on identical machinery, $1M paper each.

Every weekly run commits three files here within minutes of recording:

| file | columns | what it proves |
|---|---|---|
| `runs.csv` | run_id, as_of, recorded_at, status, checksum, superseded_by, note | the run log — halts, restatements, and checksums, in append order |
| `picks.csv` | id, ticker, picked_on, recorded_at, reason | each pick existed (with its reason, verbatim) before its outcome — GitHub's commit timestamp is the witness |
| `nav.csv` | book_id, date, equity | every book's paper NAV, so the scoreboard can be recomputed |

**What is not here, and why:** trades, fill prices, share counts, position sizes.
The price data is licensed (Sharadar) and cannot be redistributed. Anyone with
their own price feed can reconstruct the path from the decisions above.

**What a checksum proves:** that the record hasn't changed since it was
written — not that it was right. What this repo adds is the *when*: a commit
here is a timestamp Trenyx doesn't control.

If a row is ever edited rather than appended, the commit history will show it.
That's the point.
