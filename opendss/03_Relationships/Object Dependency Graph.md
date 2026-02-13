---
note_type: opendss_relationship
relationship_type: "object_dependency_graph"
source_refs:
  - "data/OpenDSS/templates/Master.dss"
status: "draft"
---

# Object Dependency Graph

<!-- AUTO-GENERATED:START -->
```mermaid
graph LR
  CNData --> Line
  CNData --> LineGeometry
  CapControl --> Capacitor
  CapControl --> Line
  CapControl --> Transformer
  Capacitor --> CapControl
  Circuit --> Capacitor
  Circuit --> Generator
  Circuit --> Line
  Circuit --> Load
  Circuit --> PVSystem
  Circuit --> Storage
  Circuit --> Transformer
  EnergyMeter --> Line
  EnergyMeter --> Monitor
  Fuse --> Line
  Fuse --> Recloser
  Fuse --> Relay
  Fuse --> TCC_Curve
  Generator --> LoadShape
  Generator --> Monitor
  GrowthShape --> Load
  GrowthShape --> LoadShape
  InvControl --> PVSystem
  InvControl --> Storage
  InvControl --> XYCurve
  Line --> CNData
  Line --> LineCode
  Line --> LineGeometry
  Line --> TSData
  Line --> WireData
  LineCode --> Line
  LineGeometry --> CNData
  LineGeometry --> Line
  LineGeometry --> TSData
  LineGeometry --> WireData
  Load --> GrowthShape
  Load --> LoadShape
  Load --> Monitor
  LoadShape --> Generator
  LoadShape --> Load
  LoadShape --> PVSystem
  LoadShape --> Storage
  Monitor --> EnergyMeter
  Monitor --> Generator
  Monitor --> Line
  Monitor --> Load
  Monitor --> PVSystem
  Monitor --> Sensor
  Monitor --> Transformer
  PVSystem --> InvControl
  PVSystem --> LoadShape
  PVSystem --> Monitor
  PVSystem --> XYCurve
  PriceShape --> Storage
  PriceShape --> TShape
  Recloser --> Fuse
  Recloser --> Line
  Recloser --> Relay
  Recloser --> TCC_Curve
  RegControl --> Transformer
  Relay --> Fuse
  Relay --> Line
  Relay --> Recloser
  Relay --> TCC_Curve
  Relay --> Transformer
  Sensor --> Line
  Sensor --> Monitor
  Sensor --> Transformer
  Storage --> InvControl
  Storage --> LoadShape
  Storage --> PriceShape
  Storage --> TShape
  TCC_Curve --> Fuse
  TCC_Curve --> Recloser
  TCC_Curve --> Relay
  TSData --> Line
  TSData --> LineGeometry
  TShape --> PriceShape
  TShape --> Storage
  Transformer --> CapControl
  Transformer --> Monitor
  Transformer --> RegControl
  WireData --> Line
  WireData --> LineGeometry
```
<!-- AUTO-GENERATED:END -->

<!-- CURATED:START -->
- Directed edges represent likely reference/dependency relationships in templates.
<!-- CURATED:END -->
