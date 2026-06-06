# east-toronto-streetmap

An accessible interactive streetmap of east Toronto — keyboard- and
screen-reader-navigable, with a dual-mode (Cartesian via pointer,
polar via keyboard) interaction model. One of a family of accessible
map demos; see also
[terminal-map](https://github.com/bobdodd/terminal-map) and
[accessible-maps](https://github.com/bobdodd/accessible-maps).

A runnable version is hosted at
<https://a11ybob.com/maps/east-toronto-streetmap>.

## Running it

Open `index.htm` in a browser, or serve the folder over any static
HTTP server. There is no build step.

## Structure

This repository deliberately includes the full data pipeline behind the
rendered map, not just the finished demo:

- `index.htm` — entry point
- `js/` — the demo's source: geometry, rendering (`MapDrawing.js`),
  feature models (`Road.js`, `Building.js`, …), and the per-layer map
  data (`MapData*.js`)
- `map/` — GeoJSON layers (roads, buildings, water, amenities, …)
- `shapefiles/` — shapefile exports of the same layers
- `map.osm` — the raw OpenStreetMap extract the layers come from
- `styles.css`, `boundary.png`, `bam.svg` — presentation assets

## Licence

The **code** (`index.htm`, `js/`, `styles.css`) is licensed
GPL-3.0-or-later — see [LICENSE](LICENSE).

The **map data** (`map.osm`, `shapefiles/`, `map/`) is derived from
OpenStreetMap, © OpenStreetMap contributors, under the Open Database
License (ODbL) v1.0. See [NOTICE](NOTICE) for details.
