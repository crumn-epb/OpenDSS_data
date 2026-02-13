---
note_type: opendss_object
object_class: "storage"
declared_in_files:
  - "Master.dss"
  - "Storage.dss"
related_objects:
  - "invcontrol"
  - "loadshape"
  - "priceshape"
  - "tshape"
related_files:
  - "Master.dss"
  - "Storage.dss"
related_commands:
  - "New"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
  - "data/OpenDSS/templates/Storage.dss"
  - "context/EE653 OpenDSS Tutorial and Cases.pdf :: keyword=Storage"
status: "draft"
---

# Object - Storage

<!-- AUTO-GENERATED:START -->
## Auto Summary
- Class: `storage`
- Declared in: `Master.dss`, `Storage.dss`
- Parsed attrs: `%effcharge`, `%effdischarge`, `%reserve`, `%stored`, `bus1`, `conn`, `dispmode`, `enabled`, `kv`, `kwhrated`, `kwrated`, `phases`
- Description: An energy storage DER element with power/energy limits and dispatch mode settings.
- Grid role: Shifts energy across time and provides fast active/reactive support where needed.

## Auto Snippets
```dss
New Storage.<name> bus1=<BUS> phases=<NPH> kv=<KV> conn=<wye>
~ kWrated=<KW_RATED> kWhrated=<KWH_RATED> %stored=<SOC_INIT>
~ %effcharge=<EFF_CHG> %effdischarge=<EFF_DISCHG>
~ dispmode=<DEFAULT|follow|external>
```
<!-- AUTO-GENERATED:END -->


<!-- CURATED:START -->
## Definition
An energy storage DER element with power/energy limits and dispatch mode settings.

## Role in Grid
Shifts energy across time and provides fast active/reactive support where needed.

## Core Attributes
| Attribute | Meaning | Type/Unit | Required |
|---|---|---|---|
| `%effcharge` | Charge efficiency setting for storage charging. | percent | Optional |
| `%effdischarge` | Discharge efficiency setting for storage discharging. | percent | Optional |
| `%reserve` | Minimum reserved state-of-charge for storage. | percent | Optional |
| `%stored` | Initial state-of-charge before simulation starts. | percent | Context |
| `bus1` | Primary terminal bus connection (supports phase suffixes). | bus token | Required |
| `conn` | Connection type for element terminals. | wye|delta | Context |
| `dispmode` | Storage dispatch strategy. | default|follow|external|... | Optional |
| `enabled` | Enable/disable this element. | True/False | Optional |
| `kv` | Nominal voltage level for element connection. | kV | Context |
| `kwhrated` | Usable energy capacity. | kWh | Context |
| `kwrated` | Charge/discharge active power capability. | kW | Context |
| `phases` | Phase count for connected element. | integer | Context |

## Skeleton
```dss
New Storage.<name> bus1=<BUS> phases=<NPH> kv=<KV> conn=<wye>
~ kWrated=<KW_RATED> kWhrated=<KWH_RATED> %stored=<SOC_INIT>
~ %effcharge=<EFF_CHG> %effdischarge=<EFF_DISCHG>
~ dispmode=<DEFAULT|follow|external>
```

## Example
```dss
New Storage.obj1 bus1=BUS1.1.2.3 phases=3 kv=12.47 conn=1
~ kWrated=500 kWhrated=500 %stored=1
~ %effcharge=1 %effdischarge=1
~ dispmode=DEFAULT
```

## Related
**Related Objects**
- [[Object - InvControl]]
- [[Object - LoadShape]]
- [[Object - PriceShape]]
- [[Object - TShape]]

**Related Files**
- [[File - Master.dss]]
- [[File - Storage.dss]]

## Pitfalls and Validation
- Keep names and units consistent with referenced files.
- Re-run a snapshot solve after edits to verify convergence.
- Confirm references to curves/controllers resolve.

## Source Refs
- `data/OpenDSS/templates/Master.dss`
- `data/OpenDSS/templates/Storage.dss`
- `context/EE653 OpenDSS Tutorial and Cases.pdf` keyword: `Storage`
<!-- CURATED:END -->

