# Finest Way UK

The website for the best luxury travel agency — [finestway.uk](https://finestway.uk/)

A plain static website: just HTML, CSS and JavaScript. There is **no build step**.

## Structure

```
index.html        Home page
404.html          Not-found page
css/styles.css    Compiled Bootstrap 5 + Grayscale theme (vendored)
js/scripts.js     Navbar shrink/scrollspy + footer year
assets/img/       Photos used on the page
assets/favicon.ico
CNAME             Custom domain for GitHub Pages (finestway.uk)
```

Bootstrap's JavaScript, Font Awesome icons and Google Fonts are loaded from CDNs
(see the `<head>` of `index.html`), so nothing needs to be installed.

## Run it locally

Because the page loads `css/` and `js/` via relative paths, open it through a
local web server (opening the file directly with `file://` also works for most
of the page).

Pick whichever you have installed:

```powershell
# Python 3
python -m http.server 8000

# Node.js
npx serve .
```

Then visit <http://localhost:8000/>.

> Note: the "About" photo is a `.heic` file, which some browsers (e.g. Chrome on
> Windows) cannot display. This matches the current live site. Replace
> `assets/img/mldvs.heic` with a `.jpg`/`.webp` and update the `src` in
> `index.html` if you want it to render everywhere.

## Deploy

The site is served by GitHub Pages on the custom domain in `CNAME`. In the repo
settings, set **Pages → Build and deployment → Source** to **Deploy from a
branch**, branch `main`, folder `/ (root)`. Pushing to `main` publishes the
files as-is — no Actions workflow required.
