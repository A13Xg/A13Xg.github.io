# A13Xg Industries — App Documentation

Central home for public app documentation from **A13Xg Industries**: privacy policies, terms of use, support pages, and the shared `app-ads.txt`. Served with GitHub Pages at the domain root:

**https://a13xg.github.io/**

## Apps

| App | Privacy | Terms | Support |
|---|---|---|---|
| Magnet Swarm | [privacy](https://a13xg.github.io/magnet-swarm/privacy/) | [terms](https://a13xg.github.io/magnet-swarm/terms/) | [support](https://a13xg.github.io/magnet-swarm/support/) |

## Site structure

- **`/`** is the main index. It lists every app and service, built automatically from pages with `layout: app`.
- **`/<slug>/`** is an app or service home with a short intro and a table of contents of its documents.
- **`/<slug>/<doc>/`** is one document.

Each app's pages are scoped to that app. Their header shows only the app's name and links to its own documents. They never link to the main index or to other apps. Scoping comes from the first URL segment (`_includes/section.html`), so a new app needs no configuration beyond its folder.

| Path | Purpose |
|---|---|
| `_layouts/home.html` | Main index |
| `_layouts/app.html` | App/service home + table of contents |
| `_layouts/doc.html` | Single document (default for every page) |
| `_includes/header.html` | Scoped header and document nav |
| `assets/site.css` | Styles (light and dark) |

Document front matter: `title` (page heading), `head_title` (browser tab, include the app name), `nav_title` (short header label), `order` (position in nav/TOC), `summary` (TOC blurb), `permalink`.

## Adding a new app or service

1. Copy `_template/` to a folder named after the slug (e.g. `my-new-app/`). Move each `privacy.md`/`terms.md`/`support.md` into `<doc>/index.md` if you like, since the permalink decides the URL either way.
2. Replace every `{{APP_NAME}}`, `{{APP_SLUG}}`, `{{EFFECTIVE_DATE}}`, `{{ONE_LINE_DESCRIPTION}}` and `{{SHORT_INTRO}}` placeholder, and edit the data sections to match what the app actually collects. Delete any document that doesn't apply, or add new ones with the same front matter.
3. Add the app to the table above.
4. Commit and push. GitHub Pages republishes in about a minute. The main index picks the app up automatically.

Use the resulting URLs in App Store Connect:
- **Privacy Policy URL** → `https://a13xg.github.io/<slug>/privacy/`
- **Support URL** → `https://a13xg.github.io/<slug>/support/`
- **Marketing URL** → `https://a13xg.github.io/<slug>/`

## app-ads.txt

`app-ads.txt` lists the ad sellers authorized to sell ad space in these apps, following the IAB Tech Lab spec. Ad networks only look for it at the domain root (`https://a13xg.github.io/app-ads.txt`), which is why this repo must stay named `A13Xg.github.io`. Every app whose store listing points to a developer website on `a13xg.github.io` shares this one file. If a new app uses a different ad network or publisher ID, add one line per seller.

Current entries:
- Google AdMob, publisher `pub-2324560181270946` (Magnet Swarm)

## Legacy URLs

Magnet Swarm v1.0 shipped with `https://a13xg.github.io/App-Documentation/...` links. Those paths are served by the redirect stubs in `App-Documentation/`, which point to the pages here. The old A13Xg/App-Documentation repo has been deleted. Remove `App-Documentation/` once no live store listing uses those links.
