---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Capacitors.dss"
declares_objects:
  - "capacitor"
included_by_master: true
include_stage: "load_and_reactive_devices"
related_files:
  []
status: "draft"
---

# File - Capacitors.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Capacitors.dss`
- Purpose: Shunt capacitor banks
- Declares: `capacitor`
- Included by master: `true`
- Include stage: `load_and_reactive_devices`
- Include index: `16` of `24`


## Auto Snippets
```dss
New Capacitor.<CAP_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kvar=<KVAR> numsteps=<NSTEPS> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Shunt capacitor banks

## Declared Objects
- [[Object - Capacitor]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `load_and_reactive_devices`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Capacitor.<CAP_NAME> bus1=<BUS> phases=<NPH> conn=<wye|delta>
~ kv=<KV> kvar=<KVAR> numsteps=<NSTEPS> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Capacitors.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

