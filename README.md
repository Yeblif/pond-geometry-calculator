# Pond Geometry Calculator

A single-file, offline HTML tool for concept sizing of excavated ponds. Open `index.html` in any browser — no install, no internet needed.

## Features

- Plan shapes: circle, square, rectangle (length:width ratio) or a custom outline drawn on a sketch canvas
- Side slopes as 1V:xH or % grade
- Solve for any one of volume, top area or minimum depth from the other two
- Freeboard, with usable vs maximum (to lowest rim / spill point) storage
- Optional existing-ground and pond-base gradients (longitudinal and crossfall), in 1 in x or %
- Interactive 3D preview (drag to rotate, scroll to zoom, shift-drag to pan)
- DXF export (AutoCAD R12, metres, local coordinates) of top rim, approximate base toe and design waterline

## Limitations

Concept sizing only. Planar ground and base, numerical grid integration, no outfall, berm, ground-condition, sediment or operational allowances. Verify levels, stability and volumes in CAD.

## Version history

Each version is a commit — see the git log. v5 was never saved separately.

| Version | Change |
|---|---|
| v1 | Basic shapes, side slope, solve volume/area/depth, 3D preview |
| v2 | Freeboard, usable vs total capacity |
| v3 | Custom drawn outline |
| v4 | Ground and base gradients, spill level |
| v6 | Collapsible gradient panels, minimum depth, global grade format, DXF export |

## Known issues

- Ground and base gradients reported as not calculating correctly; steep grades (e.g. 1 in 0.5) look extreme in the 3D preview.
