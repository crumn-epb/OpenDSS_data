---
note_type: opendss_file
source_path: "data/OpenDSS/templates/TCC_Curve.dss"
declares_objects:
  - "tcc_curve"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - TCC_Curve.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `TCC_Curve.dss`
- Purpose: Time-current characteristic curves
- Declares: `tcc_curve`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `10` of `24`


## Auto Snippets
```dss
New TCC_Curve.<TCC_NAME> npts=<NPTS>
~ c_array=[<CURRENT_MULT_1> <CURRENT_MULT_2> ...]
~ t_array=[<TIME_SEC_1> <TIME_SEC_2> ...]
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Time-current characteristic curves

## Declared Objects
- [[Object - TCC_Curve]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New TCC_Curve.<TCC_NAME> npts=<NPTS>
~ c_array=[<CURRENT_MULT_1> <CURRENT_MULT_2> ...]
~ t_array=[<TIME_SEC_1> <TIME_SEC_2> ...]
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/TCC_Curve.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

