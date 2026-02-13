---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Generators.dss"
declares_objects:
  - "generator"
included_by_master: true
include_stage: "der_and_inverter_controls"
related_files:
  []
status: "draft"
---

# File - Generators.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Generators.dss`
- Purpose: Synchronous/modeled distributed generation
- Declares: `generator`
- Included by master: `true`
- Include stage: `der_and_inverter_controls`
- Include index: `18` of `24`


## Auto Snippets
```dss
New Generator.<GEN_NAME> bus1=<BUS> phases=<NPH> kv=<KV>
~ kw=<KW> kvar=<KVAR> model=<MODEL_ID> vpu=<VPU_SET> enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Synchronous/modeled distributed generation

## Declared Objects
- [[Object - Generator]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `der_and_inverter_controls`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Generator.<GEN_NAME> bus1=<BUS> phases=<NPH> kv=<KV>
~ kw=<KW> kvar=<KVAR> model=<MODEL_ID> vpu=<VPU_SET> enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Generators.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

