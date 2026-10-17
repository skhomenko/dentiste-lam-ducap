# Dentiste Lam-Ducap

A small, bilingual website for Diane Du Cap and Tuan Lam’s dental clinic in Châteauguay, Québec. Built for existing patients to find the current address and call the clinic.

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
- `public/assets/fonts/`: self-hosted Latin WOFF2 fonts, licenses and provenance.
- `public/assets/styles.css`: shared responsive styles, keyboard focus, and print layout.
- `public/assets/brand-mark.svg`: simplified, plum-backed character for the 44 and 52 px header, subject to owner approval.
- `public/assets/mascot.svg`: original vector interpretation of the clinic’s sign character, subject to owner approval.
- `public/assets/favicon.svg`: small character mark, subject to owner approval.

Keep changes to facts, links, and structured data consistent across all four language-specific pages. The phone link uses international format. Google Maps receives only the clinic’s public address when a visitor follows the directions link. There are no embedded maps, trackers, forms, cookies, or third-party resource requests on page load.

## Publication status

Not launched. A review preview for the clinic owners is published to GitHub Pages at https://skhomenko.github.io/dentiste-lam-ducap/ by `.github/workflows/pages.yml` on every push to `main`. The workflow publishes only `public/`, marks every page `noindex`, and prefixes the 404 page's root-relative paths for the project subpath. The final host is not chosen yet; remove the preview when it is. Any future static host must publish **only `public/`**, never the repository root. The private `.local/` folder is excluded from Git and must stay outside published output.

Before launch, obtain approval for the text and character artwork, confirm the public practice name, address and phone number, and supply any desired opening hours and actual office email. Missing details are intentionally omitted. After choosing the real domain, add absolute canonical/language-alternate URLs, sharing metadata and a sitemap, and review the selected host’s HTTPS and security header configuration.

## Typography and error pages

DM Serif Display provides the regular and italic display type; Manrope provides the variable-weight body type and bold wordmark. Both ship with SIL Open Font License files. Only the first-viewport faces are preloaded. Fallback sizes and vertical metrics are matched to the local fonts; all text sizes respect the browser default.

The team pages remain deliberately short until approved staff details are available. The home page links to them once in navigation.

The bilingual `404.html` uses root-relative assets and home links so a nested missing URL still works. Configure the chosen host to serve it with HTTP status 404. Python's basic preview server shows its own error response for missing URLs; open `/404.html` directly to inspect the design locally. Production 404 routing must be checked when hosting is selected.
