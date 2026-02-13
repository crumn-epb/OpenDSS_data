---
note_type: opendss_file
source_path: "data/OpenDSS/templates/XYCurve.dss"
declares_objects:
  - "xycurve"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - XYCurve.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `XYCurve.dss`
- Purpose: Generic piecewise curves
- Declares: `xycurve`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `9` of `24`


## Auto Snippets
```dss
New XYCurve.<CURVE_NAME> npts=<NPTS>
~ xarray=[<X1> <X2> ...] yarray=[<Y1> <Y2> ...]
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Generic piecewise curves

## Declared Objects
- [[Object - XYCurve]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New XYCurve.<CURVE_NAME> npts=<NPTS>
~ xarray=[<X1> <X2> ...] yarray=[<Y1> <Y2> ...]
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/XYCurve.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

