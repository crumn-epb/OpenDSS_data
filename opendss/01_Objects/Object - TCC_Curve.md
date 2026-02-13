---
note_type: opendss_object
object_class: "tcc_curve"
declared_in_files:
  - "TCC_Curve.dss"
related_objects:
  - "fuse"
  - "recloser"
  - "relay"
related_files:
  - "TCC_Curve.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/TCC_Curve.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=TCC_Curve"
status: "draft"
---

# Object - TCC_Curve

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `tcc_curve`
- Declared in: `TCC_Curve.dss`
- Parsed attrs: `c_array`, `npts`, `t_array`
- Description: A time-current characteristic curve definition used by protective devices.
- Grid role: Defines the protection timing selectivity that coordinates fault-clearing devices.

## Auto Snippets
```dss
New TCC_Curve.<TCC_NAME> npts=<NPTS>
~ c_array=[<CURRENT_MULT_1> <CURRENT_MULT_2> ...]
~ t_array=[<TIME_SEC_1> <TIME_SEC_2> ...]
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A time-current characteristic curve definition used by protective devices.

## Role in Grid
Defines the protection timing selectivity that coordinates fault-clearing devices.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `c_array` | Current axis values for TCC or related curve definitions. | array | Context |
| `npts` | Number of points in profile/curve. | integer | Required |
| `t_array` | Time axis values for TCC or related curves. | array | Context |

## Skeleton
```dss
New TCC_Curve.<TCC_NAME> npts=<NPTS>
~ c_array=[<CURRENT_MULT_1> <CURRENT_MULT_2> ...]
~ t_array=[<TIME_SEC_1> <TIME_SEC_2> ...]
```

## Example
```dss
New TCC_Curve.obj1 npts=24
~ c_array=[1 1 ...]
~ t_array=[1 1 ...]
```

## Related
**Related Objects**
- [[Object - Fuse]]
- [[Object - Recloser]]
- [[Object - Relay]]

**Related Files**
- [[File - TCC_Curve.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/TCC_Curve.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `TCC_Curve`
<!-- CURATED:END -->

