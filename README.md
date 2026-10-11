# US AI Data Center Tracker — data

This repository holds the data behind the tracker at
https://energyriskengineering.com/data-center-tracker

- `data.json` — everything the page shows:
  - `updated` — date of the last refresh (shown on the page)
  - `projects` — one row per campus: status, power, cooling, water, cost, next milestone, risks, sources
  - `nri` — FEMA National Risk Index (Dec 2025) county ratings for each project's county
  - `news` — recent developments with a risk-engineering angle

The page loads `data.json` each time someone opens it, so updating this file updates the site.
No other file needs to change. If the file can't be loaded, the page falls back to the copy built into it.
