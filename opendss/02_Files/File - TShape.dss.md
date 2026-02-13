---
note_type: opendss_file
source_path: "data/OpenDSS/templates/TShape.dss"
declares_objects:
  - "tshape"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - TShape.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `TShape.dss`
- Purpose: Temperature profiles
- Declares: `tshape`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `6` of `24`


## Auto Snippets
```dss
New TShape.<TSHAPE_NAME> npts=<NPTS> interval=<HOURS>
~ temp=(file=<TEMP_CSV_PATH>)
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Temperature profiles

## Declared Objects
- [[Object - TShape]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New TShape.<TSHAPE_NAME> npts=<NPTS> interval=<HOURS>
~ temp=(file=<TEMP_CSV_PATH>)
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/TShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

