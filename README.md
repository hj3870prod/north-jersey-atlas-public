# North Jersey County Atlas

A single zoomable map of nine New Jersey counties — the northern eight plus
Middlesex — showing all 251 municipalities at exact boundaries, over the
NJ Transit commuter rail, PATH and light rail network.

**Live map:** https://hj3870prod.github.io/north-jersey-atlas-public/

Montclair, West Orange, Bloomfield and Clifton are outlined in red: three Essex
County towns and one Passaic County town that read as one continuous area on the
ground but sit under two county governments.

## Using it

- **Zoom** 1× to 16× with the `+` / `−` / `Reset` buttons, or ctrl/⌘ with the
  scroll wheel. Drag to pan, double-click to zoom in.
- **Jump to** buttons frame Essex, Union, Middlesex or the four towns.
- Town and station names appear as you zoom in — 193 town names at the full
  extent, 335 at high zoom, plus every one of the 172 station names.
- **Hover** any town for its county, type and land area; any station for the
  systems serving it.

## What's in this repository

Just the built page. `index.html` is self-contained — all boundary and rail data
is inlined, so it has no build step and no server requirements beyond static
hosting. The build scripts that generate it live in a separate repository.

## Data and licensing

The page code is MIT licensed (see `LICENSE`). The data is licensed separately:

- **Boundaries** — U.S. Census Bureau cartographic boundary files, 2023 vintage
  (county and county subdivision, 1:500,000). A U.S. Government work, public
  domain. In New Jersey every county subdivision is a municipality, so the town
  shapes are exact, not schematic. Areas are ALAND: land only, water excluded.
- **Rail lines and stations** — © OpenStreetMap contributors, licensed
  [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/). Attribution is
  required, and it appears in the page footer. Because the page embeds
  coordinates rather than only a rendered image, that embedded data is a
  derivative database and carries ODbL's share-alike terms.

- **House prices** — [Zillow Home Value Index](https://www.zillow.com/research/data/)
  (ZHVI), the typical value for homes in the 35th–65th percentile, as a 12-month
  median. Free to use with attribution; the credit is in the page footer. Zillow
  publishes nothing for 54 of these 251 towns — mostly rural townships — and those
  fall back to the Census figure rather than being estimated.
- **Income, rent, population, tenure** — U.S. Census Bureau, American Community
  Survey 2024 5-year estimates, joined on GEOID so every municipality is covered.
  Being 5-year estimates they describe 2020–2024, not this month.

Station symbols show which systems serve a stop, not which trains actually stop
there — off-peak and weekend patterns differ.
