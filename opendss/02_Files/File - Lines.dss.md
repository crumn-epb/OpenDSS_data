---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Lines.dss"
declares_objects:
  - "line"
included_by_master: true
include_stage: "network_topology"
related_files:
  []
status: "draft"
---

# File - Lines.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Lines.dss`
- Purpose: Network branches (non-switch lines)
- Declares: `line`
- Included by master: `true`
- Include stage: `network_topology`
- Include index: `11` of `24`


## Auto Snippets
```dss
New Line.<LINE_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ length=<LEN> units=<UNITS> linecode=<LC_NAME>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> enabled=<True>
```

```dss
New Line.<LINE_GEO_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ length=<LEN> units=<UNITS> geometry=<GEO_NAME> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Network branches (non-switch lines)

## Declared Objects
- [[Object - Line]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `network_topology`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Line.<LINE_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ length=<LEN> units=<UNITS> linecode=<LC_NAME>
~ normamps=<NORM_AMPS> emergamps=<EMERG_AMPS> enabled=<True>
```

```dss
New Line.<LINE_GEO_NAME> bus1=<FROM_BUS> bus2=<TO_BUS> phases=<NPH>
~ length=<LEN> units=<UNITS> geometry=<GEO_NAME> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Lines.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

