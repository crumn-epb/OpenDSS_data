---
note_type: opendss_object
object_class: energymeter
declared_in_files:
  - Master.dss
  - MetersMonitors.dss
related_objects:
  - line
  - monitor
related_files:
  - Master.dss
  - MetersMonitors.dss
related_commands:
  - New
source_refs:
  - data/OpenDSS/templates/Master.dss
  - data/OpenDSS/templates/MetersMonitors.dss
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=EnergyMeter"
status: draft
---

# Object - EnergyMeter

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `energymeter`
- Declared in: `Master.dss`, `MetersMonitors.dss`
- Parsed attrs: `element`, `terminal`
- Description: A metering element that accumulates feeder/zone energy, losses, and demand quantities.
- Grid role: Acts as accounting instrumentation for feeder losses, energy delivery, and zone performance.

## Auto Snippets
```dss
New EnergyMeter.<name> element=<Line.name> terminal=<1>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A metering element that accumulates feeder/zone energy, losses, and demand quantities.

## Role in Grid
Acts as accounting instrumentation for feeder losses, energy delivery, and zone performance.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `element` | Target element reference used by monitor/meter/control. | object reference | Context |
| `terminal` | Terminal index for monitor/meter/sensor/control. | integer | Context |

## Skeleton
```dss
New EnergyMeter.<name> element=<Line.name> terminal=<1>
```

## Example
```dss
New EnergyMeter.obj1 element=obj1 terminal=1
```

## Related
**Related Objects**
- [[Object - Line]]
- [[Object - Monitor]]

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
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `EnergyMeter`
<!-- CURATED:END -->

