# Pond Geometry Calculator

A single-file, offline HTML tool that gives a quick head start on sizing an excavated pond before designing it in Civil 3D.

## What it does

- Plan shapes: circle, square, rectangle (length:width ratio) or a custom outline drawn on a sketch canvas
- Side slopes as 1V:xH or % grade
- Solves for any one of volume, top area or minimum depth from the other two
- Freeboard, with usable vs maximum (to lowest rim / spill point) storage
- Interactive 3D preview (drag to rotate, scroll to zoom, shift-drag to pan)
- DXF export (AutoCAD R12, metres, local coordinates) of top rim, approximate base toe and design waterline as 3D polylines

**Optional features** are switched on with the tick boxes at the top of the page. A feature that is unticked is hidden and has no effect on the results. The tick-box choices are remembered in the browser.

- Ground & base gradients: existing-ground and pond-base gradients (longitudinal and crossfall), in 1 in x or %

**Limitations:** concept sizing only. Planar ground and base, numerical grid integration, no outfall, berm, ground-condition, sediment or operational allowances. Verify levels, stability and volumes in CAD.

## How to use

1. Open `index.html` in a browser (or the GitHub Pages site). No install or internet connection is needed.
2. Tick any optional features you need.
3. Pick a plan shape and set the side slope and freeboard.
4. Under *Known quantities*, select the quantity to calculate and enter the other two.
5. Check the 3D preview, then use **Export DXF** to bring the outlines into Civil 3D.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole tool: page, styles and script in one offline file |
| `CHANGELOG.md` | Version history |
| `.github/` | Issue and pull request templates |

## Changelog

See [CHANGELOG.md](CHANGELOG.md).
