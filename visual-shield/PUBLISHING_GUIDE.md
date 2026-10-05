# Publish Visual Shield with GitHub Pages

## Official URLs

Use these after GitHub Pages has successfully deployed:

- Official website / homepage: `https://hamzarehan.github.io/visual-shield/`
- Support URL: `https://hamzarehan.github.io/visual-shield/support.html`
- Privacy policy URL: `https://hamzarehan.github.io/visual-shield/privacy.html`
- Support email: `hamzarehan83@gmail.com`

The existing `https://hamzarehan.github.io/` account site remains unchanged. Visual Shield is published from its `/visual-shield/` subfolder.

## Before publishing

1. Confirm the GitHub repository is public, or that your GitHub plan supports Pages for this repository.
2. Commit and push the `docs/` directory to the `main` branch.
3. Confirm that `hamzarehan83@gmail.com` is the support email you want to publish publicly.

## Enable GitHub Pages

1. Open `https://github.com/hamzarehan/hamzarehan.github.io`.
2. Select **Settings**.
3. In the left sidebar, select **Pages** under **Code and automation**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**.
6. Select **Save**.
7. Wait for the Pages deployment to finish. GitHub will show the published URL on the same page.
8. Open all three URLs listed above and confirm the homepage, support page, and privacy page load over HTTPS.

## Chrome Web Store fields

Enter:

- Homepage URL: `https://hamzarehan.github.io/visual-shield/`
- Support URL: `https://hamzarehan.github.io/visual-shield/support.html`
- Mature content: **No**
- Item support: **On**

If the dashboard separately asks for a privacy-policy URL, use:

`https://hamzarehan.github.io/visual-shield/privacy.html`

## Google Search Console ownership

For the Chrome Web Store “official URL” association, Google may require ownership verification. GitHub Pages project sites do not let you verify ownership of the whole `github.io` domain through DNS because you do not own that domain. Try the URL-prefix property for the exact project URL if the dashboard accepts it. If Chrome requires domain-level ownership, connect a custom domain that you own to GitHub Pages, add the provided DNS records, and verify that domain in Google Search Console.

The homepage and support links can still be used as public listing URLs even if website ownership association is not enabled.

## Add the Chrome Web Store link after approval

After the extension is published:

1. Copy its public Chrome Web Store URL.
2. Open `docs/index.html`.
3. Replace the “Chrome Web Store — coming soon” link target (`href="#availability"`) with the store URL.
4. Change its label to “Add to Chrome”.
5. Commit and push the update.

## Updating the website

Edit files under `docs/`, then commit and push to `main`. GitHub Pages will redeploy automatically. Deployment status is available under the repository's **Actions** tab or **Settings → Pages**.
