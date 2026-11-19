# Pond Geometry Calculator

A single-file, offline HTML tool that gives a quick head start on sizing an excavated pond before designing it in Civil 3D.

## What it does

- Plan shapes: circle, square, rectangle (length along X : width along Y) or a custom outline drawn on a sketch canvas (up on the sketch is +Y)
- Side slopes as 1V:xH or % grade
- Solves for any one of volume, top area or minimum depth from the other two
- Freeboard, with usable vs maximum (to lowest rim / spill point) storage
- Datum level: all levels are reported as real levels (datum + relative level)
- Save and load projects as `.json` files (all inputs, feature choices and outlines; versioned so older files keep loading)
- Interactive 3D preview (drag to rotate, scroll to zoom, shift-drag to pan)
- DXF export (AutoCAD R12, metres) of the outlines as 3D polylines at real levels, one layer per element

**Optional features** are switched on with the tick boxes at the top of the page. A feature that is unticked is hidden and has no effect on the results. The tick-box choices are remembered in the browser and saved with projects.

| Feature | What it adds |
|---|---|
| Ground & base gradients | Site-wide existing-ground gradients and per-pond base gradients (longitudinal and crossfall), in 1 in x or %. "Base matches ground" keeps the excavation depth constant |
| Permanent water level | Outlet invert as depth above the base or as a level; permanent (treatment) and attenuation volumes; "Attenuation" volume basis |
| Safety bench & access ramp | A level bench cut into the sides below the water level, and a ramp (width, gradient, position) running in from the rim to the base. Both change the storage |
| Stage-storage table | Depth, level, wetted area and cumulative volume from the lowest point to spill at a chosen interval; copy or download as CSV |
| Natural shapes & smoothing | A "Natural" plan shape (irregular ellipse with a seed number and a minimum inward bend radius) and a smoothing button for custom outlines |
| Import polyline (DXF / CSV) | Closed LWPOLYLINE / POLYLINE from an ASCII DXF, or pasted X,Y coordinates, as a pond outline or site boundary. Drawing coordinates are kept on export |
| Maintenance track & verges | Track at top of bank with inner/outer verges, crossfall, outer tie-in slope and a minimum centreline radius; reports land take and track length |
| Site boundary check | Rectangle or imported boundary, shrunk by the track offsets; fits / doesn't fit, spare or missing area and volume, largest pond that fits, and a button to use the allowed area as the outline |
| Treatment + attenuation ponds | A second pond with its own inputs (tabs), laid out end to end or side by side with a gap and a shared track; treatment volume as a % of the attenuation volume; level drop between the ponds |
| SuDS guidance checks | Warnings against common UK guidance (side slope, freeboard, depths, bench, treatment volume). Values are in one table in the script and marked "to confirm" until checked against CIRIA C753 |

**Limitations:** concept sizing only. Planar ground and base, numerical grid integration, sampled contours, no outfall, berm, ground-condition, sediment or operational allowances. Verify levels, stability and volumes in CAD.

## How to use

1. Open `index.html` in a browser (or the GitHub Pages site). No install or internet connection is needed.
2. Tick any optional features you need.
3. Pick a plan shape and set the side slope, datum and freeboard.
4. Under *Known quantities*, select the quantity to calculate and enter the other two.
5. Check the 3D preview, then use **Export DXF** to bring the outlines into Civil 3D, and **Save** to keep the project.

### DXF layers

| Layer | Contents |
|---|---|
| `POND_TOP_RIM` | Top of bank at existing ground level |
| `POND_WATERLINE_APPROX` | Design water level contour |
| `POND_BASE_TOE_APPROX` | Where the side slopes meet the base |
| `POND_PERMANENT_WATERLINE_APPROX` | Permanent water level contour (when used) |
| `POND_BENCH_APPROX`, `POND_ACCESS_RAMP_APPROX` | Bench edges and ramp outline (when used) |
| `TRACK_INNER_EDGE`, `TRACK_CENTRELINE`, `TRACK_OUTER_EDGE`, `VERGE_OUTER_EDGE`, `LAND_TAKE_EDGE` | Maintenance track (when used) |
| `SITE_BOUNDARY` | Site boundary (when used) |

With two ponds the pond layers are prefixed `POND1_` and `POND2_`. XY is local (site origin at 0,0) unless an outline or boundary was imported from a drawing, in which case the original drawing coordinates are used. The polylines can be converted to feature lines in Civil 3D.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole tool: page, styles and script in one offline file |
| `CHANGELOG.md` | Version history |
| `.github/` | Issue and pull request templates |

## Changelog

See [CHANGELOG.md](CHANGELOG.md).
