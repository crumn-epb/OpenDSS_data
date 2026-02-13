---
note_type: opendss_file
source_path: "data/OpenDSS/templates/GrowthShape.dss"
declares_objects:
  - "growthshape"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - GrowthShape.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `GrowthShape.dss`
- Purpose: Multi-year growth multipliers
- Declares: `growthshape`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `8` of `24`


## Auto Snippets
```dss
New GrowthShape.<GROWTH_NAME> npts=<NYEARS>
~ year=[<YEAR_1> <YEAR_2> ...] mult=[<M1> <M2> ...]
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Multi-year growth multipliers

## Declared Objects
- [[Object - GrowthShape]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New GrowthShape.<GROWTH_NAME> npts=<NYEARS>
~ year=[<YEAR_1> <YEAR_2> ...] mult=[<M1> <M2> ...]
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/GrowthShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

