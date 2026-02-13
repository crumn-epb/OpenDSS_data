---
note_type: opendss_object
object_class: "xycurve"
declared_in_files:
  - "XYCurve.dss"
related_objects:
  []
related_files:
  - "XYCurve.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/XYCurve.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=XYCurve"
status: "draft"
---

# Object - XYCurve

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `xycurve`
- Declared in: `XYCurve.dss`
- Parsed attrs: `npts`, `xarray`, `yarray`
- Description: A reusable XY lookup curve object used by controls and device characteristics.
- Grid role: Provides control and device characteristic mappings for nonlinear response behaviors.

## Auto Snippets
```dss
New XYCurve.<CURVE_NAME> npts=<NPTS>
~ xarray=[<X1> <X2> ...] yarray=[<Y1> <Y2> ...]
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A reusable XY lookup curve object used by controls and device characteristics.

## Role in Grid
Provides control and device characteristic mappings for nonlinear response behaviors.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `npts` | Number of points in profile/curve. | integer | Required |
| `xarray` | Reactance array values (class-specific). | array | Context |
| `yarray` | Admittance/susceptance array values (class-specific). | array | Context |

## Skeleton
```dss
New XYCurve.<CURVE_NAME> npts=<NPTS>
~ xarray=[<X1> <X2> ...] yarray=[<Y1> <Y2> ...]
```

## Example
```dss
New XYCurve.obj1 npts=24
~ xarray=[1 1 ...] yarray=[1 1 ...]
```

## Related
**Related Objects**
- _(none mapped)_

**Related Files**
- [[File - XYCurve.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/XYCurve.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `XYCurve`
<!-- CURATED:END -->

