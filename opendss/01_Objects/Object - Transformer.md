---
note_type: opendss_object
object_class: "transformer"
declared_in_files:
  - "Master.dss"
  - "Transformers.dss"
related_objects:
  - "capcontrol"
  - "monitor"
  - "regcontrol"
related_files:
  - "Master.dss"
  - "Transformers.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/Transformers.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Transformer"
status: "draft"
---

# Object - Transformer

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `transformer`
- Declared in: `Master.dss`, `Transformers.dss`
- Parsed attrs: `%rs`, `buses`, `conns`, `enabled`, `kvas`, `kvs`, `phases`, `windings`, `xhl`
- Description: A multi-winding electromagnetic coupling element for voltage level conversion and isolation.
- Grid role: Links voltage levels and feeder sections while introducing series impedance and tap behavior.

## Auto Snippets
```dss
New Transformer.<XFMR_NAME> phases=<NPH> windings=<NW>
~ buses=[<BUS_W1>, <BUS_W2>] conns=[<wye>, <wye>]
~ kvs=[<KV_W1>, <KV_W2>] kvas=[<KVA_W1>, <KVA_W2>]
~ xhl=<XHL_PCT> %rs=[<R_W1_PCT>, <R_W2_PCT>]
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
A multi-winding electromagnetic coupling element for voltage level conversion and isolation.

## Role in Grid
Links voltage levels and feeder sections while introducing series impedance and tap behavior.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `%rs` | Per-winding resistance array for transformer model. | percent array | Context |
| `buses` | Bus list for multi-terminal devices (e.g., transformer windings). | array<bus token> | Context |
| `conns` | Connection type list per winding/terminal. | array<wye|delta> | Context |
| `enabled` | Enable/disable this element. | True/False | Optional |
| `kvas` | Per-winding transformer ratings. | array<kVA> | Context |
| `kvs` | Per-winding voltage ratings. | array<kV> | Context |
| `phases` | Phase count for connected element. | integer | Context |
| `windings` | Number of transformer windings. | integer | Required |
| `xhl` | Leakage reactance between high/low transformer windings. | percent | Context |

## Skeleton
```dss
New Transformer.<XFMR_NAME> phases=<NPH> windings=<NW>
~ buses=[<BUS_W1>, <BUS_W2>] conns=[<wye>, <wye>]
~ kvs=[<KV_W1>, <KV_W2>] kvas=[<KVA_W1>, <KVA_W2>]
~ xhl=<XHL_PCT> %rs=[<R_W1_PCT>, <R_W2_PCT>]
```

## Example
```dss
New Transformer.obj1 phases=3 windings=1
~ buses=[BUS1.1.2.3, BUS1.1.2.3] conns=[1, 1]
~ kvs=[12.47, 12.47] kvas=[12.47, 12.47]
~ xhl=1 %rs=[1, 1]
```

## Related
**Related Objects**
- [[Object - CapControl]]
- [[Object - Monitor]]
- [[Object - RegControl]]

**Related Files**
- [[File - Master.dss]]
- [[File - Transformers.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/Transformers.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Transformer`
<!-- CURATED:END -->

