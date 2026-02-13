---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Loads.dss"
declares_objects:
  - "load"
included_by_master: true
include_stage: "load_and_reactive_devices"
related_files:
  []
status: "draft"
---

# File - Loads.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Loads.dss`
- Purpose: Customer demand models
- Declares: `load`
- Included by master: `true`
- Include stage: `load_and_reactive_devices`
- Include index: `15` of `24`


## Auto Snippets
```dss
New Load.<LOAD_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kw=<KW> kvar=<KVAR> model=<MODEL_ID>
~ daily=<LS_NAME> yearly=<LS_NAME> status=<variable|fixed> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Customer demand models

## Declared Objects
- [[Object - Load]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `load_and_reactive_devices`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Load.<LOAD_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kw=<KW> kvar=<KVAR> model=<MODEL_ID>
~ daily=<LS_NAME> yearly=<LS_NAME> status=<variable|fixed> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Loads.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

