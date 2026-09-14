# Black Rose Rollers — website

Interim website for **Black Rose Rollers**, a WFTDA women's flat track roller derby
league in Hanover, PA. This is a single static page served on GitHub Pages while the
full WordPress build is decided. It is intentionally a real, content-complete site
(not a "coming soon" placeholder) so it supports the league's Google for Nonprofits
review.

## What's here

```
index.html                 the whole site (one file, no build step)
assets/logos/              team + league logos
  black-rose-mark.png        primary league mark
  all-stars.png              All Stars team
  riveters.png               Riveters team
  grime-and-punishment.png   Grime & Punishment team
CNAME                      custom domain for GitHub Pages (blackroserollers.org)
.nojekyll                  tells GitHub Pages to serve files as-is
```

There is no framework and no build. Open `index.html` in a browser to preview locally.

## Editing

- **Text**: edit the copy directly in `index.html`. Sections are commented by id
  (`#about`, `#teams`, `#involved`, `#bouts`, `#contact`).
- **Logos**: replace the files in `assets/logos/` (keep the same names) or update the
  `<img src="...">` paths.
- **Colors / type**: the Black Rose design tokens live in the `:root` and `.t-light`
  / `.t-dark` / `.t-blood` blocks at the top of the `<style>` section. Primary is
  Oxblood `#700014`; accent is Gilt `#D0AC38` (used sparingly). Headings are PT Serif,
  body is DM Sans.

## Deploy on GitHub Pages

1. Push these files to the repo (root of the `main` branch).
2. **Settings → Pages → Source**: Deploy from a branch → `main` / `/ (root)`.
3. **Settings → Pages → Custom domain**: `blackroserollers.org` (the `CNAME` file
   already sets this). Enable **Enforce HTTPS** once the domain check passes.

### DNS (at GoDaddy)

Apex `@` → four A records:
`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
`www` → CNAME → `<your-username>.github.io`

Email (Google Workspace MX/TXT records) is separate and does not conflict.

## Later: WordPress

When the league moves to WordPress hosting, repoint the DNS records to the new host
and remove the custom domain from GitHub Pages. Nothing here is permanent.

## Links

- Instagram: https://www.instagram.com/blackroserollers/
- Facebook: https://www.facebook.com/blackroserollers/
- Linktree: https://linktr.ee/black_rose_rollers
- WFTDA: https://wftda.com/wftda-leagues/black-rose-rollers/
