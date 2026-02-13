---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Switches.dss"
declares_objects:
  - "line"
included_by_master: true
include_stage: "network_topology"
related_files:
  []
status: "draft"
---

# File - Switches.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Switches.dss`
- Purpose: Explicit switch elements and default status
- Declares: `line`
- Included by master: `true`
- Include stage: `network_topology`
- Include index: `12` of `24`


## Auto Snippets
```dss
New Line.<SW_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ switch=Yes r1=<SMALL_R> x1=<SMALL_X> r0=<SMALL_R0> x0=<SMALL_X0>
~ normamps=<NORM_AMPS> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Explicit switch elements and default status

## Declared Objects
- [[Object - Line]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `network_topology`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Line.<SW_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ switch=Yes r1=<SMALL_R> x1=<SMALL_X> r0=<SMALL_R0> x0=<SMALL_X0>
~ normamps=<NORM_AMPS> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Switches.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

