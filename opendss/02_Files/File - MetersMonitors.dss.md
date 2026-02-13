---
note_type: opendss_file
source_path: "data/OpenDSS/templates/MetersMonitors.dss"
declares_objects:
  - "energymeter"
  - "monitor"
  - "sensor"
included_by_master: true
include_stage: "protection_and_monitoring"
related_files:
  []
status: "draft"
---

# File - MetersMonitors.dss

<!-- AUTO-GENERATED:START -->
## Auto Summary
- File: `MetersMonitors.dss`
- Purpose: Measurement and logging objects
- Declares: `energymeter`, `monitor`, `sensor`
- Included by master: `true`
- Include stage: `protection_and_monitoring`
- Include index: `23` of `24`


## Auto Snippets
```dss
New EnergyMeter.<MTR_NAME> element=<Line.NAME> terminal=<1>
```

```dss
New Monitor.<MON_NAME> element=<Line|Transformer|Load|PVSystem.NAME>
~ terminal=<TERM> mode=<0..12> ppolar=<Yes|No>
```

```dss
New Sensor.<SENSOR_NAME> element=<Line|Transformer.NAME> terminal=<TERM>
~ kVbase=<KV_BASE> clear=<Yes|No>
```

<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Purpose
Measurement and logging objects

## Declared Objects
- [[Object - EnergyMeter]]
- [[Object - Monitor]]
- [[Object - Sensor]]

## Include and Ordering Role
- Included by `Master.dss`: `true`
- Include stage: `protection_and_monitoring`
- Master file reference: [[File - Master.dss]]

## Skeleton Snippets
```dss
New EnergyMeter.<MTR_NAME> element=<Line.NAME> terminal=<1>
```

```dss
New Monitor.<MON_NAME> element=<Line|Transformer|Load|PVSystem.NAME>
~ terminal=<TERM> mode=<0..12> ppolar=<Yes|No>
```

```dss
New Sensor.<SENSOR_NAME> element=<Line|Transformer.NAME> terminal=<TERM>
~ kVbase=<KV_BASE> clear=<Yes|No>
```

## Links
- [[Object-File Matrix]]
- [[Object Dependency Graph]]
- [[File - Master.dss]]

## Source Refs
- `data/OpenDSS/templates/MetersMonitors.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Define A Circuit`
<!-- CURATED:END -->

