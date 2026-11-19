# Changelog

All notable changes to this project are recorded here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added
- Optional feature tick boxes at the top of the page; unticked features are hidden and ignored by the calculation, and choices are remembered in the browser (#2)
- Changelog, issue templates and pull request template
- "Base matches ground gradients" tick box (#15)
- Datum level; real levels in the results and the DXF, one DXF layer per element (#4)
- Save / Load project as a versioned `.json` file (#3)
- Optional stage-storage table with copy and CSV download (#9)
- Optional permanent water level with permanent and attenuation volumes and an attenuation volume basis (#10)
- Optional safety bench and access ramp (#13)
- Optional import of closed polylines from DXF or pasted CSV, keeping drawing coordinates on export (#5)
- Optional natural (irregular) pond shape with seed and minimum bend radius, and outline smoothing (#6)
- Optional maintenance track and verges with minimum radius, land take and track length (#7)
- Optional site boundary check with allowed area, largest fitting pond and spare/missing volume (#8)
- Optional second pond (treatment + attenuation) with layout, linked volume and level drop (#11)
- Optional SuDS guidance checks (warnings; values to be confirmed against C753) (#12)
- Pond position and rotation in the site when the boundary or second-pond feature is on

### Fixed
- Rectangle length now runs along +X, matching the longitudinal (+X) gradient labels
- Custom sketch outlines are no longer mirrored (up on the sketch is +Y), including in the DXF
- Levels no longer display as "-0 m"

### Changed
- Ground & base gradients are now an optional feature (off by default) shown as a plain panel instead of collapsible dropdowns (#2)
- Script rewritten into readable, commented sections with a pond data model that can hold more than one pond; results are unchanged (#2)
- Section numbering made sequential (01–06)

## [v6]
### Added
- Collapsible gradient panels, minimum depth, global grade format, DXF export

## [v4]
### Added
- Ground and base gradients, spill level

## [v3]
### Added
- Custom drawn outline

## [v2]
### Added
- Freeboard, usable vs total capacity

## [v1]
### Added
- Basic shapes, side slope, solve volume/area/depth, 3D preview

v5 was never saved separately.
