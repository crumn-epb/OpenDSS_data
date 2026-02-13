---
note_type: opendss_object
object_class: "invcontrol"
declared_in_files:
  - "InvControls.dss"
  - "Master.dss"
related_objects:
  - "pvsystem"
  - "storage"
  - "xycurve"
related_files:
  - "InvControls.dss"
  - "Master.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/InvControls.dss"
  - "data/OpenDSS/templates/Master.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=InvControl"
status: "draft"
---

# Object - InvControl

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `invcontrol`
- Declared in: `InvControls.dss`, `Master.dss`
- Parsed attrs: `derlist`, `mode`, `voltage_curvex_ref`, `vvc_curve1`
- Description: A controller that coordinates inverter-based DER behavior (volt-var, volt-watt, etc.).
- Grid role: Enforces fleet-level inverter response so DERs support voltage and operational constraints.

## Auto Snippets
```dss
New InvControl.<INVCTRL_NAME> DERList=[<PVSystem.PV1>, <Storage.BESS1>]
~ mode=<VOLTVAR|VOLTWATT|DYNAMICREACCURR|WATTPF>
~ vvc_curve1=<XYCURVE_NAME> voltage_curvex_ref=<rated|avg>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A controller that coordinates inverter-based DER behavior (volt-var, volt-watt, etc.).

## Role in Grid
Enforces fleet-level inverter response so DERs support voltage and operational constraints.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `derlist` | DER fleet list controlled by this InvControl. | array<object reference> | Required |
| `mode` | Inverter control mode. | VOLTVAR|VOLTWATT|DYNAMICREACCURR|WATTPF | Required |
| `voltage_curvex_ref` | Voltage-axis reference for curve evaluation. | rated|avg | Context |
| `vvc_curve1` | Volt-var curve used when mode enables volt-var behavior. | XYCurve reference | Context |

## Skeleton
```dss
New InvControl.<INVCTRL_NAME> DERList=[<PVSystem.PV1>, <Storage.BESS1>]
~ mode=<VOLTVAR|VOLTWATT|DYNAMICREACCURR|WATTPF>
~ vvc_curve1=<XYCURVE_NAME> voltage_curvex_ref=<rated|avg>
```

## Example
```dss
New InvControl.obj1 DERList=[1, 1]
~ mode=VOLTVAR
~ vvc_curve1=obj1 voltage_curvex_ref=rated
```

## Related
**Related Objects**
- [[Object - PVSystem]]
- [[Object - Storage]]
- [[Object - XYCurve]]

**Related Files**
- [[File - InvControls.dss]]
- [[File - Master.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/InvControls.dss`
- `data/OpenDSS/templates/Master.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `InvControl`
<!-- CURATED:END -->

