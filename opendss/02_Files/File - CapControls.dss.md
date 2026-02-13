---
note_type: opendss_file
source_path: "data/OpenDSS/templates/CapControls.dss"
declares_objects:
  - "capcontrol"
included_by_master: true
include_stage: "load_and_reactive_devices"
related_files:
  []
status: "draft"
---

# File - CapControls.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `CapControls.dss`
- Purpose: Automatic capacitor switching controls
- Declares: `capcontrol`
- Included by master: `true`
- Include stage: `load_and_reactive_devices`
- Include index: `17` of `24`


## Auto Snippets
```dss
New CapControl.<CAPCTRL_NAME> capacitor=<CAP_NAME>
~ element=<Line|Transformer.NAME> terminal=<TERM> type=<current>
~ onsetting=<ON_VALUE> offsetting=<OFF_VALUE> delay=<SEC>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Automatic capacitor switching controls

## Declared Objects
- [[Object - CapControl]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `load_and_reactive_devices`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New CapControl.<CAPCTRL_NAME> capacitor=<CAP_NAME>
~ element=<Line|Transformer.NAME> terminal=<TERM> type=<current>
~ onsetting=<ON_VALUE> offsetting=<OFF_VALUE> delay=<SEC>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/CapControls.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

