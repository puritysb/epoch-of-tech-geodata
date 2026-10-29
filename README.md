# Epoch of Tech — open geographic data

Public release of the geographic databases used by **Epoch of Tech**, a turn-based
strategy game about the history of information technology, from the 1970s mainframe
era to the age of AI. This repository exists so that the OpenStreetMap-derived
databases inside the game are publicly available under the
[Open Database License 1.0](https://opendatacommons.org/licenses/odbl/1-0/), as ODbL
requires for a publicly used produced work.

Map data © OpenStreetMap contributors. See [ATTRIBUTION.md](ATTRIBUTION.md) for every
source and licence.

Page: https://github.com/puritysb/epoch-of-tech-geodata · built 2026-10-30 from game commit `d5c9a7dd3ac3`.

## Contents

| What | Where | Size |
|---|---|---|
| 281 vector databases (JSON, gzip JSON) for 35 regions | [`data/`](data/) | 59.8 MiB |
| 9541 terrain meshes and rasters (Godot `.res`, PNG, WebP) | Release asset `epoch-of-tech-geodata-rasters-2026-10-29.tar.gz` | 420.8 MiB |
| 104 Creative Commons photographs, exactly as shipped in the game | [`media/`](media/) · [credits](media/CREDITS.md) | 8.0 MiB |
| Paths, sizes and SHA-256 of every file | [`MANIFEST.json`](MANIFEST.json) | |

Regions: austin, bangalore, daedeok, dresden, edinburgh, geneva, guangzhou, gumi, helsinki, hsinchu, hyderabad_hitec, london, mesh_cache, montreal, munich, new_york, osaka, research_triangle, route_128, sao_paulo, seattle, seoul_metro, shenzhen, silicon_fen, silicon_valley, singapore, stockholm, sydney, tel_aviv, tokyo, toronto, world, zhangjiang, zhongguancun, zurich.

Coordinates are in the game's map projection; the region files carry their origin
and scale. `.res` meshes are Godot 4 compressed resources produced from the same DEM
and OSM water inputs.

## How it was made

Roads, coastlines, land use and building outlines were extracted from OpenStreetMap
(Geofabrik extracts and the Overpass API), clipped to each region window, simplified
and quantised for the game. Korean city surroundings add MOLIT building footprints.
Elevation comes from Terrain Tiles; land cover from Copernicus. No other changes to
the source facts were made beyond clipping, simplification, reprojection and
classification into the game's land-use categories.

## Licence

OpenStreetMap-derived databases: ODbL 1.0, contents DbCL 1.0. Other sources keep their
own terms listed in [ATTRIBUTION.md](ATTRIBUTION.md). Photographs in `media/` keep their own
Creative Commons licences listed in [media/CREDITS.md](media/CREDITS.md); they are published here
DRM-free so that the copies distributed through game stores never restrict anyone's rights
under those licences. The game itself, its code and
its artwork are not part of this release.
