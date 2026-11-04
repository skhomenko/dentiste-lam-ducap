# Dentiste Lam-Ducap

A small, bilingual website for Tuan Lam and Diane Du Cap’s dental clinic in Châteauguay, Québec. Built for existing patients to find the current address and call the clinic.

## Local preview

From the repository root:

```sh
python3 -m http.server 4173 --bind 127.0.0.1 --directory public
```

Open http://127.0.0.1:4173. French is `index.html`; English is `index-en.html`.

No build dependencies, build step, or JavaScript runtime are needed. Fonts are bundled locally; no external resources are loaded. All essential navigation uses ordinary links. The only script is non-executable JSON-LD describing the clinic.

## Files

- `public/index.html`: French page.
- `public/index-en.html`: equivalent English page.
- `public/equipe.html` and `public/team.html`: French and English team pages.
- `public/404.html`: bilingual recovery page with home and phone links.
- `public/sitemap.xml` and `public/robots.txt`: search engine sitemap with language alternates, and crawler rules.
- `public/assets/fonts/`: self-hosted Latin WOFF2 fonts, licenses and provenance.
- `public/assets/styles.css`: shared responsive styles, keyboard focus, and print layout.
- `public/assets/brand-mark.svg`: the clinic logo, traced to vector on a plum background, for the 44 and 52 px header.
- `public/assets/mascot.svg`: original vector interpretation of the clinic’s sign character, subject to owner approval.
- `public/assets/favicon.svg`: the same traced logo with tighter padding, for the browser tab.

Keep changes to facts, links, and structured data consistent across all four language-specific pages. The phone link uses international format. Google Maps receives only the clinic’s public address when a visitor follows the directions link. There are no embedded maps, trackers, forms, cookies, or third-party resource requests on page load.

## Publication status

The site is published to GitHub Pages at https://dentistelam.ca/ by `.github/workflows/pages.yml` on every push to `main`. The workflow publishes only `public/`, never the repository root. The custom domain is set in the repository's Pages settings (a `CNAME` file is ignored by workflow deployments), and the domain's DNS points to GitHub Pages. The private `.local/` folder is excluded from Git and must stay outside published output.

Every page declares its absolute canonical URL and its French and English alternates; `sitemap.xml` and `robots.txt` use the same URLs. Keep them in step when adding or renaming a page. Still open: confirm owner approval of the text and logo, supply the actual office email (missing details are intentionally omitted), add sharing metadata, and review security headers (GitHub Pages cannot set custom headers).

## Typography and error pages

DM Serif Display provides the regular and italic display type; Manrope provides the variable-weight body type and bold wordmark. Both ship with SIL Open Font License files. Only the first-viewport faces are preloaded. Fallback sizes and vertical metrics are matched to the local fonts; all text sizes respect the browser default.

The team pages remain deliberately short until approved staff details are available. The home page links to them once in navigation.

The bilingual `404.html` uses root-relative assets and home links so a nested missing URL still works. GitHub Pages serves it automatically with HTTP status 404. Python's basic preview server shows its own error response for missing URLs; open `/404.html` directly to inspect the design locally.
