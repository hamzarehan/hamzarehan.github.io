# hamzarehan.github.io

Personal site for Hamza Rehan's apps and tools — plain static HTML served by GitHub Pages from `main` (root). No build step.

## Structure

| Path | What it is |
| --- | --- |
| `/` | Home: product showcase, selected apps, principles, about, contact |
| `/apps/` | All apps, filterable by Islamic / Tools |
| `/pilgrim-companion/` | Pilgrim Companion product page |
| `/visual-shield/` | Visual Shield product page, `support.html`, `privacy.html` |
| `/contact/` | Contact topics (pre-filled email subjects) |
| `/gift/`, `/tip/` | Appreciation page; `/tip/` redirects old links to `/gift/` |
| `/privacy-policy.html`, `/terms-of-use.html`, `/support.html`, `/delete-account.html` | Pilgrim Companion legal/support pages |
| `assets/css/site.css` | Shared styles (light + dark) |
| `assets/img/` | App icons (256 px), screenshots (540 px JPEG), favicon |

## URLs that must not move

These are entered in App Store Connect, Google Play Console, Google OAuth and the browser-extension stores. Keep them at the same paths:

- `/privacy-policy.html`, `/terms-of-use.html`, `/support.html`, `/delete-account.html`
- `/visual-shield/`, `/visual-shield/support.html`, `/visual-shield/privacy.html`
- The `google-site-verification` meta tag in `/index.html`

## Adding a new app

1. Copy `pilgrim-companion/` to `/<app-slug>/` and replace the content, icon and screenshots. Use `/visual-shield/` as the model for a tool or extension.
2. Add the icon to `assets/img/<app-slug>.png` (256 × 256) and screenshots as ~540 px wide JPEGs.
3. Add a card to the right grid on `/index.html` and to `#app-grid` on `/apps/index.html` (`data-cat="islamic"` or `data-cat="tools"`). Use `pill live` or `pill dev` for the status.
4. Put the app's privacy policy and support page under `/<app-slug>/` and link them from its page.
5. Add the app to the footer **Apps** / **Resources** / **Legal** lists on every page, and its URLs to `sitemap.xml`.

## Appreciation page

Keep `/gift/index.html` as the appreciation page and `/tip/index.html` as its legacy
redirect. The redirect preserves the `?app=` context used by app links. The English quotation is a labelled excerpt from Jamiʿ at-Tirmidhi
2035, linked to its source and graded Hasan (Darussalam).

The `.transfer-details` block is visible and uses the existing bank details copied
from the live `/gift/` page on 15 October 2026. Keep account values and copy-button
data aligned across both pages; do not replace them with placeholders.

## Local preview

Serve this directory with a static HTTP server. Pages use root-relative asset paths,
so opening HTML directly through `file://` does not provide a complete preview.
The site needs no framework, dependency installation, or production build.
