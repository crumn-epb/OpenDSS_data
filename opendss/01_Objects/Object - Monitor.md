---
note_type: opendss_object
object_class: "monitor"
declared_in_files:
  - "Master.dss"
  - "MetersMonitors.dss"
related_objects:
  - "energymeter"
  - "generator"
  - "line"
  - "load"
  - "pvsystem"
  - "sensor"
  - "transformer"
related_files:
  - "Master.dss"
  - "MetersMonitors.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/MetersMonitors.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Monitor"
status: "draft"
---

# Object - Monitor

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `monitor`
- Declared in: `Master.dss`, `MetersMonitors.dss`
- Parsed attrs: `element`, `mode`, `ppolar`, `terminal`
- Description: A recorder element that captures time-series electrical quantities from target elements.
- Grid role: Provides traceability and diagnostics for validating operating states and control actions.

## Auto Snippets
```dss
New Monitor.<name> element=<Line|Transformer|Load|PVSystem.name>
~ terminal=<TERM> mode=<0..12> ppolar=<Yes|No>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A recorder element that captures time-series electrical quantities from target elements.

## Role in Grid
Provides traceability and diagnostics for validating operating states and control actions.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `element` | Target element reference used by monitor/meter/control. | object reference | Context |
| `mode` | Monitor channel mode code (e.g., V/I, P/Q, taps). | integer code | Required |
| `ppolar` | Whether monitor reports powers in polar format. | Yes/No | Optional |
| `terminal` | Terminal index for monitor/meter/sensor/control. | integer | Context |

## Skeleton
```dss
New Monitor.<name> element=<Line|Transformer|Load|PVSystem.name>
~ terminal=<TERM> mode=<0..12> ppolar=<Yes|No>
```

## Example
```dss
New Monitor.obj1 element=Line
~ terminal=1 mode=1 ppolar=Yes
```

## Related
**Related Objects**
- [[Object - EnergyMeter]]
- [[Object - Generator]]
- [[Object - Line]]
- [[Object - Load]]
- [[Object - PVSystem]]
- [[Object - Sensor]]
- [[Object - Transformer]]

**Related Files**
- [[File - Master.dss]]
- [[File - MetersMonitors.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/MetersMonitors.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Monitor`
<!-- CURATED:END -->

