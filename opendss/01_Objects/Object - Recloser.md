---
note_type: opendss_object
object_class: "recloser"
declared_in_files:
  - "Master.dss"
  - "Protection.dss"
related_objects:
  - "fuse"
  - "line"
  - "relay"
  - "tcc_curve"
related_files:
  - "Master.dss"
  - "Protection.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/Protection.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Recloser"
status: "draft"
---

# Object - Recloser

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `recloser`
- Declared in: `Master.dss`, `Protection.dss`
- Parsed attrs: `groundcurve`, `groundtrip`, `monitoredobj`, `monitoredterm`, `phasecurve`, `phasetrip`, `shots`, `switchedobj`, `switchedterm`
- Description: A protection and switching device that can trip and reclose according to curves/settings.
- Grid role: Improves reliability by clearing temporary faults and restoring service automatically.

## Auto Snippets
```dss
New Recloser.<name> monitoredobj=<Line.name> monitoredterm=<1>
~ switchedobj=<Line.name> switchedterm=<1> phasecurve=<TCC_NAME>
~ groundcurve=<TCC_NAME> phaseTrip=<A> groundTrip=<A> shots=<N>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A protection and switching device that can trip and reclose according to curves/settings.

## Role in Grid
Improves reliability by clearing temporary faults and restoring service automatically.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `groundcurve` | Ground-element TCC curve reference. | TCC_Curve reference | Optional |
| `groundtrip` | Ground trip pickup setting. | A | Optional |
| `monitoredobj` | Element monitored by protection/control. | object reference | Required |
| `monitoredterm` | Terminal index used for monitored quantities. | integer | Context |
| `phasecurve` | Phase-overcurrent TCC curve reference. | TCC_Curve reference | Optional |
| `phasetrip` | Phase trip pickup setting. | A | Optional |
| `shots` | Maximum reclose shots before lockout. | integer | Optional |
| `switchedobj` | Element operated by protection/control. | object reference | Required |
| `switchedterm` | Terminal index on switched element. | integer | Context |

## Skeleton
```dss
New Recloser.<name> monitoredobj=<Line.name> monitoredterm=<1>
~ switchedobj=<Line.name> switchedterm=<1> phasecurve=<TCC_NAME>
~ groundcurve=<TCC_NAME> phaseTrip=<A> groundTrip=<A> shots=<N>
```

## Example
```dss
New Recloser.obj1 monitoredobj=obj1 monitoredterm=1
~ switchedobj=obj1 switchedterm=1 phasecurve=obj1
~ groundcurve=obj1 phaseTrip=1 groundTrip=1 shots=1
```

## Related
**Related Objects**
- [[Object - Fuse]]
- [[Object - Line]]
- [[Object - Relay]]
- [[Object - TCC_Curve]]

**Related Files**
- [[File - Master.dss]]
- [[File - Protection.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/Protection.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Recloser`
<!-- CURATED:END -->

