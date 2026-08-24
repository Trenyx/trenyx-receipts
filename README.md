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

## Where this history starts (read this before trusting the timestamps)

This repository was created on **2026-08-24**. Its first commit is a snapshot
of runs #1–#10 exported in one go — so for those ten runs, GitHub's timestamp
proves only that the data existed by 2026-08-24, not the week-by-week
chronology. From **run #11 onward**, every run lands as its own commit within
minutes of being recorded, and the commit history is the witness.

For runs #1–#10 the external evidence is weaker but not absent: the weekly
scoreboard notes published on Substack carried the run checksums on their
publication dates (e.g. run #9's checksum in the 2026-08-20 note), and the
internal run log's `recorded_at` column is in the CSV. Weigh accordingly.

If a row is ever edited rather than appended, the commit history will show it.
That's the point.
