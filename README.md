# Navigatore Gravel – map data

Offline map data for the Navigatore Gravel app (Android, personal project): vector map with road surface and
road network for turn analysis. The files are published as **GitHub Releases** of this repository; the app
downloads only the area the user picks.

This repository contains **data only**. No code, no personal data.

## Source, licence and attribution

All files are derived from **OpenStreetMap** data – © OpenStreetMap contributors.
They are made available under the [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/)
(see `LICENSE.md` and https://www.openstreetmap.org/copyright). OSM extracts: Geofabrik, 2026-11-15/16.

Terrain elevation and routing data are **not** published here.

## Files

- `<country>.pmtiles` – vector map (PMTiles v3, zoom 6–14), built with [Planetiler](https://github.com/onthegomap/planetiler)
  from the country extract; roads carry a surface class derived from the OSM tags `surface`, `tracktype`, `smoothness`.
- `N<lat>E<lon>.roads` – road network of one 0.5° × 0.5° square (south-west corner in the name), SQLite:
  `edge` (one piece of road between two junctions: OSM node ids `a`/`b`, kind, surface class, name, access,
  oneway, length, geometry as zigzag varint deltas of lat/lon × 1e6), `edge_cell` (grid index, 1/200°),
  `poi` (drinking water, bicycle repair, food, toilets, shelters), `name`, `meta` (format and field codes).
  A road crossing the edge of a square is in both squares with the same id.

## Releases

| Release | Content |
|---|---|
| `area-2026-11` | Italy, Switzerland, France, Germany, Austria: 5 maps (one per country, 4.4 GB) and 821 road squares (4.4 GB) |
| `test-karlsruhe` | Test of the download method: one map file (Regierungsbezirk Karlsruhe, OSM data of 2026-11-08) |
