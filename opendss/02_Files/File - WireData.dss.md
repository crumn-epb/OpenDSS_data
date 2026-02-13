---
note_type: opendss_file
source_path: "data/OpenDSS/templates/WireData.dss"
declares_objects:
  - "wiredata"
included_by_master: true
include_stage: "parameter_libraries"
related_files:
  []
status: "draft"
---

# File - WireData.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `WireData.dss`
- Purpose: Overhead conductor definitions
- Declares: `wiredata`
- Included by master: `true`
- Include stage: `parameter_libraries`
- Include index: `2` of `24`


## Auto Snippets
```dss
New WireData.<WIRE_NAME> rac=<RAC_PER_LEN> gmrac=<GMR_LEN> diam=<DIAM_LEN>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> units=<mi|kft|km|m|ft>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Overhead conductor definitions

## Declared Objects
- [[Object - WireData]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `parameter_libraries`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New WireData.<WIRE_NAME> rac=<RAC_PER_LEN> gmrac=<GMR_LEN> diam=<DIAM_LEN>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> units=<mi|kft|km|m|ft>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/WireData.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

