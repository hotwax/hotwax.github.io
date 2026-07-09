# hotwax.github.io

Source for [hotwax.github.io](https://hotwax.github.io) — a catalog of HotWax Commerce open source projects, organized into **App Side** and **Server Side**.

The site is built with [Jekyll](https://jekyllrb.com/) via GitHub Pages using the Slate theme. The repository list on the homepage is **fetched dynamically** from the GitHub API (`/orgs/hotwax/repos`) in the browser, so new repositories appear automatically — no site changes needed when a repo is created, renamed, or archived.

## How categorization works

Repos are grouped by their primary language (logic in [`index.html`](index.html)):

- **Server Side** — Groovy, Java, FreeMarker
- **App Side** — Vue, TypeScript, JavaScript (Ionic apps)
- **Other** — everything else (docs, themes, etc.)

Archived repos are hidden and forks are labeled.

## Private repositories

Visitors see public repos by default. Signing in with a GitHub personal access token (stored only in the browser's localStorage, sent only to api.github.com) also lists the private repos that user can access, marked with a `private` badge.
