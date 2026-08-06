# bolotov-reports

Static hosting for password-protected team reports (GitHub Pages).

Each subfolder is one report, published as `index.html`. The files are
AES-encrypted client-side: the page asks for a password and decrypts in
the browser, so the repository may stay public.

## What is published here

| Path | What | Runbook |
|---|---|---|
| [`finance/`](finance/) | Monthly supervisor report (P&L, cash, channels) — a month picker, one folder per month | `finance` repo → `finance/MONTHLY-CLOSE.md` §6 |
| `reels-quality/` | Reels quality report | `analytics` repo |

The finance link handed to the supervisor is the picker, not a month:
`https://anechkahata.github.io/bolotov-reports/finance/` — it does not change
month to month, a new month is added as one more row plus its folder.

Nothing in this repository is readable without the password: every month page
is ciphertext plus a password gate. The picker itself carries no figures.
