# App Documentation

Public privacy policies, terms of use, and support pages for apps published by **A13Xg Industries**, served with GitHub Pages:

**https://a13xg.github.io/App-Documentation/**

## Apps

| App | Privacy | Terms | Support |
|---|---|---|---|
| Magnet Swarm | [privacy](https://a13xg.github.io/App-Documentation/magnet-swarm/privacy/) | [terms](https://a13xg.github.io/App-Documentation/magnet-swarm/terms/) | [support](https://a13xg.github.io/App-Documentation/magnet-swarm/support/) |

## Adding a new app

1. Copy `_template/` to a new folder named after the app's slug (e.g. `my-new-app/`).
2. Replace every `{{APP_NAME}}`, `{{APP_SLUG}}` and `{{EFFECTIVE_DATE}}` placeholder, and edit the data sections to match what the app actually collects.
3. Add the app to `index.md` and to the table above.
4. Commit and push. GitHub Pages republishes in about a minute.

Use the resulting URLs in App Store Connect:
- **Privacy Policy URL** → `https://a13xg.github.io/App-Documentation/<slug>/privacy/`
- **Support URL** → `https://a13xg.github.io/App-Documentation/<slug>/support/`
