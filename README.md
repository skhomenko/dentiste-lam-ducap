# Dentiste Lam-Ducap

A small, bilingual website for Diane Du Cap and Tuan Lam’s dental clinic in Châteauguay, Québec. Built for existing patients to find the current address and call the clinic.

## Local preview

From the repository root:

```sh
python3 -m http.server 4173 --bind 127.0.0.1 --directory public
```

Open http://127.0.0.1:4173. French is `index.html`; English is `index-en.html`.

No dependencies, build step, JavaScript runtime, or external fonts are needed. All essential navigation uses ordinary links. The only script is non-executable JSON-LD describing the clinic.

## Files

- `public/index.html`: French page.
- `public/index-en.html`: equivalent English page.
- `public/equipe.html` and `public/team.html`: French and English team pages.
- `public/assets/styles.css`: shared responsive styles, keyboard focus, and print layout.
- `public/assets/mascot.svg`: original vector interpretation of the clinic’s sign character, subject to owner approval.
- `public/assets/favicon.svg`: small character mark, subject to owner approval.

Keep changes to facts, links, and structured data consistent across both pages. The phone link uses international format. Google Maps receives only the clinic’s public address when a visitor follows the directions link. There are no embedded maps, trackers, forms, cookies, or third-party resource requests on page load.

## Publication status

Local review version only; not deployed. Any future static host must publish **only `public/`**, never the repository root. The private `.local/` folder is excluded from Git and must stay outside published output.

Before launch, obtain approval for the text and character artwork, confirm the public practice name, address and phone number, and supply any desired opening hours and actual office email. Missing details are intentionally omitted. After choosing the real domain, add absolute canonical/language-alternate URLs, sharing metadata and a sitemap, and review the selected host’s HTTPS and security header configuration.
