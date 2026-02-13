---
note_type: opendss_file
source_path: "data/OpenDSS/templates/InvControls.dss"
declares_objects:
  - "invcontrol"
included_by_master: true
include_stage: "der_and_inverter_controls"
related_files:
  []
status: "draft"
---

# File - InvControls.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `InvControls.dss`
- Purpose: Inverter fleet control logic
- Declares: `invcontrol`
- Included by master: `true`
- Include stage: `der_and_inverter_controls`
- Include index: `21` of `24`


## Auto Snippets
```dss
New InvControl.<INVCTRL_NAME> DERList=[<PVSystem.PV1>, <Storage.BESS1>]
~ mode=<VOLTVAR|VOLTWATT|DYNAMICREACCURR|WATTPF>
~ vvc_curve1=<XYCURVE_NAME> voltage_curvex_ref=<rated|avg>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Inverter fleet control logic

## Declared Objects
- [[Object - InvControl]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `der_and_inverter_controls`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New InvControl.<INVCTRL_NAME> DERList=[<PVSystem.PV1>, <Storage.BESS1>]
~ mode=<VOLTVAR|VOLTWATT|DYNAMICREACCURR|WATTPF>
~ vvc_curve1=<XYCURVE_NAME> voltage_curvex_ref=<rated|avg>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/InvControls.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

