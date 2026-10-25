# Kingdom information website

This repository hosts the public information website and privacy notice for
Kingdom, Matthew King's private desktop and command-line workflow tools. The
site supplies the app information and privacy links used by Kingdom's Google
OAuth configuration.

- [Website](https://kingdom-systems.github.io/)
- [Privacy notice](https://kingdom-systems.github.io/privacy.html)

The application source remains in the private Kingdom repository. This public
repository contains only the information site and its documentation. The site
provides no account sign-in or Google data processing.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | App information, Google integration and contact link. |
| `privacy.html` | Privacy notice covering the private tools' Google data use. |
| `styles.css` | Shared presentation for both pages. |
| `.nojekyll` | Disables Jekyll processing for these static files. |
| `README.md` | Repository purpose and maintenance instructions. |

## Preview locally

There is no build step or application dependency to install. Open `index.html`
in a browser to review the pages and follow the privacy link.

For an HTTP preview, run this command from the repository root with
[uv](https://docs.astral.sh/uv/) installed:

```sh
uv run --no-project python -m http.server --bind 127.0.0.1 8000
```

Visit <http://127.0.0.1:8000/> and <http://127.0.0.1:8000/privacy.html>.
Press `Ctrl+C` to stop the preview server.

## Update and publish

1. Edit the relevant HTML or stylesheet and preview the result locally.
2. Check both pages, their navigation, styling, contact link and privacy wording.
3. Review the diff, commit the intended changes and push them to `main`.
4. Check the GitHub Pages deployment in the repository's **Actions** tab, then
   confirm the live pages show the intended content.

GitHub Pages publishes the root of `main` at
<https://kingdom-systems.github.io/> with HTTPS enforced. No custom build command
or additional hosting service is required.

Keep credentials, tokens, account data and private application files out of this
public repository. Keep the privacy notice accurate when the private tools' data
use changes. Changes to Google OAuth branding, consent or account permissions are
managed separately from website updates.
