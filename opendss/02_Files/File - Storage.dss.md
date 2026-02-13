---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Storage.dss"
declares_objects:
  - "storage"
included_by_master: true
include_stage: "der_and_inverter_controls"
related_files:
  []
status: "draft"
---

# File - Storage.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Storage.dss`
- Purpose: Battery or other storage devices
- Declares: `storage`
- Included by master: `true`
- Include stage: `der_and_inverter_controls`
- Include index: `20` of `24`


## Auto Snippets
```dss
New Storage.<STOR_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta> kv=<KV>
~ kWrated=<KW_RATED> kWhrated=<KWH_RATED> %stored=<SOC_INIT_PCT>
~ %reserve=<RESERVE_PCT> %effcharge=<EFF_CHG_PCT> %effdischarge=<EFF_DIS_PCT>
~ dispmode=<DEFAULT> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Battery or other storage devices

## Declared Objects
- [[Object - Storage]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `der_and_inverter_controls`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Storage.<STOR_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta> kv=<KV>
~ kWrated=<KW_RATED> kWhrated=<KWH_RATED> %stored=<SOC_INIT_PCT>
~ %reserve=<RESERVE_PCT> %effcharge=<EFF_CHG_PCT> %effdischarge=<EFF_DIS_PCT>
~ dispmode=<DEFAULT> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Storage.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

