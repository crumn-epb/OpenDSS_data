---
note_type: opendss_object
object_class: "growthshape"
declared_in_files:
  - "GrowthShape.dss"
related_objects:
  - "load"
  - "loadshape"
related_files:
  - "GrowthShape.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/GrowthShape.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=GrowthShape"
status: "draft"
---

# Object - GrowthShape

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `growthshape`
- Declared in: `GrowthShape.dss`
- Parsed attrs: `mult`, `npts`, `year`
- Description: A multi-year scaling profile used to represent long-term load or DER growth.
- Grid role: Encodes planning-year demand/DER evolution for long-horizon study scenarios.

## Auto Snippets
```dss
New GrowthShape.<GROWTH_NAME> npts=<NYEARS>
~ year=[<YEAR_1> <YEAR_2> ...] mult=[<M1> <M2> ...]
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A multi-year scaling profile used to represent long-term load or DER growth.

## Role in Grid
Encodes planning-year demand/DER evolution for long-horizon study scenarios.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `mult` | Multiplier vector for profile/shape values. | array | Context |
| `npts` | Number of points in profile/curve. | integer | Required |
| `year` | Year axis values for growth profile. | array<int> | Context |

## Skeleton
```dss
New GrowthShape.<GROWTH_NAME> npts=<NYEARS>
~ year=[<YEAR_1> <YEAR_2> ...] mult=[<M1> <M2> ...]
```

## Example
```dss
New GrowthShape.obj1 npts=1
~ year=[1 1 ...] mult=[1 1 ...]
```

## Related
**Related Objects**
- [[Object - Load]]
- [[Object - LoadShape]]

**Related Files**
- [[File - GrowthShape.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/GrowthShape.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `GrowthShape`
<!-- CURATED:END -->

