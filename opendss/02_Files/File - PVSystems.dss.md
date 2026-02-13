---
note_type: opendss_file
source_path: "data/OpenDSS/templates/PVSystems.dss"
declares_objects:
  - "pvsystem"
included_by_master: true
include_stage: "der_and_inverter_controls"
related_files:
  []
status: "draft"
---

# File - PVSystems.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `PVSystems.dss`
- Purpose: PV inverter resources
- Declares: `pvsystem`
- Included by master: `true`
- Include stage: `der_and_inverter_controls`
- Include index: `19` of `24`


## Auto Snippets
```dss
New PVSystem.<PV_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta> kv=<KV>
~ pmpp=<PMPP_KW> kva=<KVA_RATING> irradiance=<PU_IRR>
~ temperature=<DEGC> daily=<IRR_SHAPE> yearly=<IRR_SHAPE> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
PV inverter resources

## Declared Objects
- [[Object - PVSystem]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `der_and_inverter_controls`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New PVSystem.<PV_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta> kv=<KV>
~ pmpp=<PMPP_KW> kva=<KVA_RATING> irradiance=<PU_IRR>
~ temperature=<DEGC> daily=<IRR_SHAPE> yearly=<IRR_SHAPE> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/PVSystems.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

