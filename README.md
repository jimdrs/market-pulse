# Market Pulse

A daily intelligence site on OOH, real-world media and international marketing, for the marketing team.

It is a static site with no server or build step:

| File | What it is |
|---|---|
| `index.html` | The whole app: layout, logic and the English/French switch |
| `news.json` | The data: daily editions, tenders, cities, companies, campaigns and OOH numbers |
| `fr.json` | The French text |
| `img/` | Illustrative stock photos (Unsplash, credited in the app) |
| `.nojekyll`, `robots.txt` | Make GitHub Pages serve the files as they are, and keep the site out of search engines |

## How it is published

The site is served by GitHub Pages from the `main` branch. A scheduled Claude task refreshes `news.json` and `fr.json` every morning (06:43 London time) and commits them here; Pages republishes automatically. The same content also stays in the claude.ai version of the app.

Pages sites on a personal account are public: anyone with the link can open it. The content is public news with sources and no personal details, and `robots.txt` plus a `noindex` tag keep it out of search engines.

## Updating by hand

To refresh the content yourself, replace `news.json` and `fr.json` in the repository through **Add file → Upload files**. Never edit `index.html` unless you mean to change the app itself.
