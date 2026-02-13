---
note_type: opendss_object
object_class: "priceshape"
declared_in_files:
  - "PriceShape.dss"
related_objects:
  - "storage"
  - "tshape"
related_files:
  - "PriceShape.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/PriceShape.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=PriceShape"
status: "draft"
---

# Object - PriceShape

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `priceshape`
- Declared in: `PriceShape.dss`
- Parsed attrs: `file`, `interval`, `npts`, `price`
- Description: A time-series price profile used in economics-aware operation studies.
- Grid role: Represents market/economic signals used to evaluate schedule or dispatch sensitivity.

## Auto Snippets
```dss
New PriceShape.<PRICE_NAME> npts=<NPTS> interval=<HOURS>
~ price=(file=<PRICE_CSV_PATH>)
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A time-series price profile used in economics-aware operation studies.

## Role in Grid
Represents market/economic signals used to evaluate schedule or dispatch sensitivity.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `file` | External file path for profile/curve values. | path | Context |
| `interval` | Time step between profile points. | hours (or class-specific) | Context |
| `npts` | Number of points in profile/curve. | integer | Required |
| `price` | Price values associated with PriceShape. | array | Context |

## Skeleton
```dss
New PriceShape.<PRICE_NAME> npts=<NPTS> interval=<HOURS>
~ price=(file=<PRICE_CSV_PATH>)
```

## Example
```dss
New PriceShape.obj1 npts=24 interval=1
~ price=(file=./shape.csv)
```

## Related
**Related Objects**
- [[Object - Storage]]
- [[Object - TShape]]

**Related Files**
- [[File - PriceShape.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/PriceShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `PriceShape`
<!-- CURATED:END -->

