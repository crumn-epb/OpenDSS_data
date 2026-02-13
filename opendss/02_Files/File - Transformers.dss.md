---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Transformers.dss"
declares_objects:
  - "transformer"
included_by_master: true
include_stage: "network_topology"
related_files:
  []
status: "draft"
---

# File - Transformers.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Transformers.dss`
- Purpose: Power transformer definitions
- Declares: `transformer`
- Included by master: `true`
- Include stage: `network_topology`
- Include index: `13` of `24`


## Auto Snippets
```dss
New Transformer.<XFMR_NAME> phases=<NPH> windings=<NW>
~ buses=[<BUS_W1>, <BUS_W2>] conns=[<wye>, <wye>]
~ kvs=[<KV_W1>, <KV_W2>] kvas=[<KVA_W1>, <KVA_W2>]
~ xhl=<XHL_PCT> %rs=[<R_W1_PCT>, <R_W2_PCT>] enabled=<True>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Power transformer definitions

## Declared Objects
- [[Object - Transformer]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `network_topology`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New Transformer.<XFMR_NAME> phases=<NPH> windings=<NW>
~ buses=[<BUS_W1>, <BUS_W2>] conns=[<wye>, <wye>]
~ kvs=[<KV_W1>, <KV_W2>] kvas=[<KVA_W1>, <KVA_W2>]
~ xhl=<XHL_PCT> %rs=[<R_W1_PCT>, <R_W2_PCT>] enabled=<True>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Transformers.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

