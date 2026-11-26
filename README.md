# A13Xg Industries — App Documentation

Central home for public app documentation from **A13Xg Industries**: privacy policies, terms of use, support pages, and the shared `app-ads.txt`. Served with GitHub Pages at the domain root:

**https://a13xg.github.io/**

## Apps

| App | Privacy | Terms | Support |
|---|---|---|---|
| Magnet Swarm | [privacy](https://a13xg.github.io/magnet-swarm/privacy/) | [terms](https://a13xg.github.io/magnet-swarm/terms/) | [support](https://a13xg.github.io/magnet-swarm/support/) |

## Adding a new app

1. Copy `_template/` to a new folder named after the app's slug (e.g. `my-new-app/`).
2. Replace every `{{APP_NAME}}`, `{{APP_SLUG}}` and `{{EFFECTIVE_DATE}}` placeholder, and edit the data sections to match what the app actually collects.
3. Add the app to `index.md` and to the table above.
4. Commit and push. GitHub Pages republishes in about a minute.

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
