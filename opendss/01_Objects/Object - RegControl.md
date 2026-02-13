---
note_type: opendss_object
object_class: "regcontrol"
declared_in_files:
  - "Master.dss"
  - "Regulators.dss"
related_objects:
  - "transformer"
related_files:
  - "Master.dss"
  - "Regulators.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/Regulators.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=RegControl"
status: "draft"
---

# Object - RegControl

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `regcontrol`
- Declared in: `Master.dss`, `Regulators.dss`
- Parsed attrs: `band`, `ctprim`, `maxtapchange`, `ptratio`, `r`, `transformer`, `vreg`, `winding`, `x`
- Description: A voltage regulator controller attached to transformer windings and tap positions.
- Grid role: Maintains downstream voltage bands by commanding transformer tap adjustments.

## Auto Snippets
```dss
New RegControl.<REG_NAME> transformer=<XFMR_NAME> winding=<WNO>
~ vreg=<VREG> band=<BAND> ptratio=<PT_RATIO> ctprim=<CT_PRIM>
~ r=<LINE_DROP_R> x=<LINE_DROP_X>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A voltage regulator controller attached to transformer windings and tap positions.

## Role in Grid
Maintains downstream voltage bands by commanding transformer tap adjustments.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `band` | Voltage bandwidth around `vreg` before tap action. | volts | Context |
| `ctprim` | CT primary current rating for line-drop compensation. | A | Context |
| `maxtapchange` | Maximum tap steps per regulator action. | integer | Optional |
| `ptratio` | PT ratio used to scale sensed voltage. | ratio | Context |
| `r` | Line-drop compensation R setting. | volts (control units) | Optional |
| `transformer` | Transformer object referenced by controller. | object reference | Required |
| `vreg` | Target regulated voltage at control point. | volts | Required |
| `winding` | Transformer winding number used by control. | integer | Required |
| `x` | Line-drop compensation X setting. | volts (control units) | Optional |

## Skeleton
```dss
New RegControl.<REG_NAME> transformer=<XFMR_NAME> winding=<WNO>
~ vreg=<VREG> band=<BAND> ptratio=<PT_RATIO> ctprim=<CT_PRIM>
~ r=<LINE_DROP_R> x=<LINE_DROP_X>
```

## Example
```dss
New RegControl.obj1 transformer=obj1 winding=1
~ vreg=1 band=1 ptratio=1 ctprim=1
~ r=1 x=1
```

## Related
**Related Objects**
- [[Object - Transformer]]

**Related Files**
- [[File - Master.dss]]
- [[File - Regulators.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/Regulators.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `RegControl`
<!-- CURATED:END -->

