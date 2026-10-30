# 内容模型 / Content model

This is the sole editorial source. Do not copy narrative Markdown into individual website repositories.

| Record | Location | Shared fields | Translated fields |
|---|---|---|---|
| Route | routes/SLUG/index.LANG.md | id, status, collection, person, geometry, sources | title, subtitle, body |
| Chapter | routes/SLUG/chapters/NN-SLUG.LANG.md | id, route, order, place_id, coordinates, sources | title, place, date, body |
| Person | people/ID.LANG.md | id, sources | title, body |
| Place | places/ID.LANG.md | id, coordinates, sources | title, body |
| Reference | sources/ID.LANG.md | id, url, publisher, rights | title, body |
| Station introduction | stations/ID.LANG.md | id, repository, domain, status | title, tagline, body |

LANG is zh or en. Both translations must exist with the same stable ID. Coordinates are [longitude, latitude]. Shared spatial metadata must match between translations. Citations must point to an existing paired reference. Chapters must be numbered consecutively from 1.

The route `collection` is one of the theme IDs: move, war, road, seek or quest. It determines the primary story destination. The website builder produces a static story path for each published route. The initial complete example is xuanzang in seek. A candidate should remain `status: draft` until both language records and the route material are ready.

Geography is a separate GeoJSON FeatureCollection of LineString features, with `stage` such as outbound or return. State the spatial precision explicitly in the route record. Do not equate a historic schematic with a modern walking route. Add present-day walking records only after separate access and field verification.

## Review checklist

- What supports each claim, place and period?
- Which coordinates are only modern regional references?
- Are disagreements and omitted route sections explained?
- Do both language versions convey the same scope and uncertainty?
- Are external material rights distinguished from the original authored prose?

## Running checks

With journeys beside this repository, run `node ../journeys/scripts/check-content.mjs .`. To review all destinations, run `npm run build:all` and `npm run preview` in journeys.
