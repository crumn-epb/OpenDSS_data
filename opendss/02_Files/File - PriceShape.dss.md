---
note_type: opendss_file
source_path: "data/OpenDSS/templates/PriceShape.dss"
declares_objects:
  - "priceshape"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - PriceShape.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `PriceShape.dss`
- Purpose: Energy price time series
- Declares: `priceshape`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `7` of `24`


## Auto Snippets
```dss
New PriceShape.<PRICE_NAME> npts=<NPTS> interval=<HOURS>
~ price=(file=<PRICE_CSV_PATH>)
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Energy price time series

## Declared Objects
- [[Object - PriceShape]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New PriceShape.<PRICE_NAME> npts=<NPTS> interval=<HOURS>
~ price=(file=<PRICE_CSV_PATH>)
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/PriceShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

