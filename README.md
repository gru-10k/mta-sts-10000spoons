# mta-sts.10000spoons.com.au policy host

Serves the MTA-STS policy for 10000spoons.com.au via GitHub Pages.

Policy: `.well-known/mta-sts.txt` → https://mta-sts.10000spoons.com.au/.well-known/mta-sts.txt

- mode: testing → flip to `enforce` + max_age 604800 after 1-2 weeks clean TLS-RPT reports
- `.nojekyll` is REQUIRED — without it Pages silently drops `.well-known/` (404s)
- After ANY policy change, bump `id=` in `_mta-sts.10000spoons.com.au` TXT (Cloudflare 10KS account)
- Deployed 2026-09-04 by GruBot; recipe: botpedia operations/email-authentication-playbook.md §5a
