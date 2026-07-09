# hotwax.github.io

Source for [hotwax.github.io](https://hotwax.github.io) — a catalog of HotWax Commerce open source projects, organized into **App Side** (Ionic/Vue PWAs and UI libraries) and **Server Side** (Moqui/OFBiz backend services and integrations).

The site is built with [Jekyll](https://jekyllrb.com/) via GitHub Pages using the Slate theme. The repository list on the homepage is **fetched dynamically** from the GitHub API (`/orgs/hotwax/repos`) in the browser, so new repositories appear automatically — no site changes needed when a repo is created, renamed, or archived.

## How categorization works

Logic lives in [`index.html`](index.html):

1. The `OVERRIDES` map pins specific repos to a category (`app`, `server`, or `other`). Use this for repos the language heuristic would misplace — e.g. Shopify/NetSuite integrations written in JavaScript belong to Server Side.
2. Any repo not in the map falls back to its primary language: Groovy/Java/FreeMarker/Dockerfile → Server Side; Vue/TypeScript/JavaScript → App Side; everything else → Documentation & Tooling.

To recategorize a repo, add or edit its entry in `OVERRIDES` and push to `main` — GitHub Pages rebuilds automatically.
