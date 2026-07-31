# bolotov-reports

Static hosting for password-protected team reports (GitHub Pages).

Each subfolder is one report, published as `index.html`. The files are
AES-encrypted client-side: the page asks for a password and decrypts in
the browser, so the repository may stay public.

Publishing runbook lives in the `analytics` repo.
