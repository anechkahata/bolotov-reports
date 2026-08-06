# bolotov-reports

Static hosting for password-protected team reports (GitHub Pages).

Each subfolder is one report, published as `index.html`. The files are
AES-encrypted client-side: the page asks for a password and decrypts in
the browser, so the repository may stay public.

## What is published here

| Path | What | Runbook |
|---|---|---|
| [`finance/`](finance/) | Monthly supervisor report (P&L, cash, channels) — **all months in one encrypted page**, password once, months switch instantly | `finance` repo → `finance/MONTHLY-CLOSE.md` §6 |
| `reels-quality/` | Reels quality report | `analytics` repo |

The finance link handed to the supervisor:
`https://anechkahata.github.io/bolotov-reports/finance/` — it does not change month
to month. One page holds every month: the password is asked once, then the months
are tabs, so moving from July to June never asks again. A new month is added by
rebuilding that one page (`lock_reports_bundle.py`), not by adding a folder.

Nothing in this repository is readable without the password: the finance page is
one AES-256-GCM blob holding every month, with a password gate in front of it.
