# farahnilofarfarid.com

A three-column academic website for GitHub Pages, in the style of Cargo's "Portfolio" template:

1. **Left column:** your photo, name, and menu (CV, Research, Teaching)
2. **Middle column:** a short description that stays the same on every page
3. **Right column:** the page you're on

## What to edit

| File | What it controls |
|---|---|
| `assets/img/photo.jpg` | Your photo. Replace it with yours, using the same name. Portrait orientation works best. |
| `assets/files/cv.pdf` | Your CV. Replace it with yours, using the same name. The CV page shows its pages as images, with a small download link. |
| `_config.yml` | Your name, the menu, the font, and the clock on/off switch |
| `_includes/about.md` | The description in the middle column. Links are written like `[here](mailto:you@example.com)`. |
| `index.md` | Home page, which shows your research (papers) |
| `teaching.md` | Teaching page |
| `assets/css/style.css` | Look and sizes. The variables at the top control photo size, column widths, text size, and colours. |

To add a page (e.g. "Talks"), copy `teaching.md` to `talks.md`, change its `title` and `permalink` to `/talks/`, then add it to `nav` in `_config.yml`.

`assets/js/` holds PDF.js (Mozilla, Apache 2.0 licence), which draws the CV pages. Don't edit it.

## Put it on GitHub

1. Create a **public** repository on GitHub (for example `farahnilofarfarid.github.io`).
2. Click **Add file → Upload files** and drag in **everything inside** this folder, including the `_layouts`, `_includes` and `assets` folders and the `CNAME` file. Then commit.
3. Open **Settings → Pages**. Under **Build and deployment**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.
4. On the same page, enter `farahnilofarfarid.com` under **Custom domain** and save.

## Point your domain at GitHub

Add these DNS records at the place where you bought the domain, and delete any existing `A` records for `@`:

| Type | Name / Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `YOUR-GITHUB-USERNAME.github.io` |

DNS changes can take up to a day to take effect. When **Settings → Pages** shows the domain check passing, tick **Enforce HTTPS**.

Each time you edit a file and commit, the site updates within a minute or two.
