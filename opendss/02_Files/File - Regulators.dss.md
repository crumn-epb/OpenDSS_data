---
note_type: opendss_file
source_path: "data/OpenDSS/templates/Regulators.dss"
declares_objects:
  - "regcontrol"
included_by_master: true
include_stage: "network_topology"
related_files:
  []
status: "draft"
---

# File - Regulators.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `Regulators.dss`
- Purpose: Voltage regulator controls
- Declares: `regcontrol`
- Included by master: `true`
- Include stage: `network_topology`
- Include index: `14` of `24`


## Auto Snippets
```dss
New RegControl.<REG_NAME> transformer=<XFMR_NAME> winding=<WNO>
~ vreg=<VREG_VOLT> band=<BAND_VOLT> ptratio=<PT_RATIO> ctprim=<CT_PRIM_A>
~ r=<LDC_R> x=<LDC_X> maxtapchange=<MAX_TAP_STEP>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Voltage regulator controls

## Declared Objects
- [[Object - RegControl]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `network_topology`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New RegControl.<REG_NAME> transformer=<XFMR_NAME> winding=<WNO>
~ vreg=<VREG_VOLT> band=<BAND_VOLT> ptratio=<PT_RATIO> ctprim=<CT_PRIM_A>
~ r=<LDC_R> x=<LDC_X> maxtapchange=<MAX_TAP_STEP>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/Regulators.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

