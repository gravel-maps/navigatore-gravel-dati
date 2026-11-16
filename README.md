# Navigatore Gravel – map data

Offline map data for the Navigatore Gravel app (Android, personal project): vector map with road surface,
road network for turn analysis, terrain elevation and BRouter routing data. The files are published as
**GitHub Releases** of this repository; the app downloads only the area the user picks.

This repository contains **data only**. No code, no personal data.

## Sources, licences and attribution

- **OpenStreetMap** – © OpenStreetMap contributors. The map (`.pmtiles`) and road (`.roads`) files are
  derived from OpenStreetMap data and are made available under the
  [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).
  See https://www.openstreetmap.org/copyright
- **Copernicus DEM** (terrain, `.dem` files, when present) – produced using Copernicus WorldDEM-30
  © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the
  European Union and ESA; all rights reserved. The organisations in charge of the Copernicus programme
  are not liable for any use of these data.
- **BRouter** routing data (`.rd5`, when present) – generated from OpenStreetMap data (ODbL) for the
  [BRouter](https://github.com/abrensch/brouter) routing engine (MIT licence).

## Releases

| Release | Content |
|---|---|
| `test-karlsruhe` | Test of the download method: one map file (Regierungsbezirk Karlsruhe, OSM data of 2026-11-08) |
