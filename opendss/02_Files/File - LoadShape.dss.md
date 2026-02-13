---
note_type: opendss_file
source_path: "data/OpenDSS/templates/LoadShape.dss"
declares_objects:
  - "loadshape"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - LoadShape.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `LoadShape.dss`
- Purpose: Active/reactive demand multipliers
- Declares: `loadshape`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `5` of `24`


## Auto Snippets
```dss
New LoadShape.<LS_NAME> npts=<NPTS> interval=<HOURS>
~ mult=(file=<P_MULT_CSV_PATH>) qmult=(file=<Q_MULT_CSV_PATH>)
```

```dss
New LoadShape.<LS_INLINE> npts=24 interval=1
~ mult=(1.00 0.95 0.90 ...)
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Active/reactive demand multipliers

## Declared Objects
- [[Object - LoadShape]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New LoadShape.<LS_NAME> npts=<NPTS> interval=<HOURS>
~ mult=(file=<P_MULT_CSV_PATH>) qmult=(file=<Q_MULT_CSV_PATH>)
```

```dss
New LoadShape.<LS_INLINE> npts=24 interval=1
~ mult=(1.00 0.95 0.90 ...)
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/LoadShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

