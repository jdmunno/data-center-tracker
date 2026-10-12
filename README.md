# US AI Data Center Tracker — data

This repository holds the data behind the tracker at
https://energyriskengineering.com/data-center-tracker

- `data.json` — everything the page shows:
  - `updated` — date of the last refresh (shown on the page)
  - `projects` — one row per campus: status, power, cooling, water, cost, next milestone, risks, sources
  - `nri` — FEMA National Risk Index (Dec 2025) county ratings for each project's county
  - `news` — recent developments with a risk-engineering angle
  - `permits` — dated permit and local-rule record per campus (air/water permits, zoning, moratoria, utility commission rulings, pipelines, transmission, incentives, litigation), each checked against its cited source; `open: true` means the outcome can still change; `scope` is Site, Local area (county ring: host county and nearby towns) or State; `source_kind` is Original (the deciding body's own record) or Reported (press/company account). The page flags an open item as stale when its next_date has passed, or when it has been pending six months with no update.

The page loads `data.json` each time someone opens it, so updating this file updates the site.
No other file needs to change. If the file can't be loaded, the page falls back to the copy built into it.

- `softr-page-code.html` — the code pasted into the Softr Custom Code block (one time). It reads `data.json` from this repo.
