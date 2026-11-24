# Anubandh SO Dashboard — Vadodara Region

A web-based operational performance dashboard for **India Post (Vadodara Region)** designed to track Sub Office (SO) targets, achievements, and revenue metrics.

## Overview

The **Anubandh SO Dashboard** presents unit-level and divisional/sub-divisional performance data for post offices across the Vadodara Region, pulling operational data from Google Sheets with periodic background synchronization.

## Key Features

- **Live Operational Sync:** Automated background refresh cycle (every 60 seconds) with a manual **Retry Now** option and last-updated status indicator.
- **Part A — Unit Level Data:**
  - Sequential cascading filters: **Division** → **Subdivision** → **Post Office (SO Name)**.
  - Displays active scope, matching unit count, and target vs. achievement performance for the selected scope.
  - Supports exporting filtered/unit data to Excel (`.xlsx`).
- **Part B — Division & Subdivision Wise Performance:**
  - Subordinate Office (SO) performance ranking sorted by **Weighted Achievement %**.
  - Filterable by **Division** and **Subdivision**.
  - Tabular view covering **Total Revenue GTD**, **Parcel Revenue**, **International Mails**, and **Domestic Mails**.
  - Supports exporting raw data to Excel (`.xlsx`).
- **Interface Controls:** Theme toggle and a **Mobile View** toggle for responsive/compact inspection.

## Data & Integration

- **Data Source:** Fetches live operational records from Google Sheets.
- **Deployment:** Hosted via GitHub Pages at `https://rbuvdr-wq.github.io/VadodaraAnubandhSOV1/`.

## Notes & Troubleshooting

- Because live figures are fetched dynamically from Google Sheets, a **Sync issue. Retrying next cycle...** notice may appear temporarily if the sheet source is unreachable, rate-limited, or blocked by network/CORS policies; use **Retry Now** or wait for the next 60-second cycle.
