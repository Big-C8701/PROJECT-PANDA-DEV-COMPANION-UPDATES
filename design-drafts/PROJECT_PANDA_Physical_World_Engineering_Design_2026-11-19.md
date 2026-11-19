# PROJECT P.A.N.D.A. — Physical World, Engineering & Construction Design
**Design checkpoint:** 19 November 2026
**Status:** APPROVED DESIGN DIRECTION — implementation not started; environmental simulation still open.
**Scope:** Reusable P.A.N.D.A. CORE subsystems, with REBIRTH as initial gameplay application.
**Publication:** Standalone design addendum; does not modify existing v0.9 Companion catalogue or overwrite the Master Design Bible.

## Confirmed choices
1. **Terrain manipulation — C, hybrid realistic terrain.** Smooth-looking, editable volumetric terrain with recoverable measured volumes of soil, clay, gravel, stone and ore. Digging and filling permanently modify the world. Chunk-based storage, adaptive resolution and aggregated bulk materials.
2. **Material processing — D, progressive realism.** Consistent material laws from manual survival through craftsmanship, mechanization, industrial engineering and intelligent automation. Knowledge, tools and available facilities govern access and precision; no arbitrary recipe unlocks. Processing tracks composition, purity, condition, history, byproducts and waste.
3. **Construction — C, hybrid freeform.** Manual component placement, optional snapping/alignment and blueprint-driven building use the same physical rules. Foundations, supports, connections, loads, damage, salvage and partial construction persist. NPCs and machinery may assist without bypassing material requirements.
4. **Component fabrication — C, hybrid fabrication.** Standard parts can be modified, cut, joined or replaced with custom-fabricated parts. Conserve material mass, account for offcuts and machining losses. Fabrication methods and achievable precision depend on materials, equipment and skills. Designs are reusable.
5. **Machinery — C, open-ended functional engineering.** Functional behaviour emerges from assemblies of supported mechanical, electrical, hydraulic/pneumatic and control components rather than hard-coded machine recipes. Power, torque, load, friction, heat, wear, connections and faults matter. Design, test, diagnose and iterate; larger production lines connect machines.
6. **Vehicle engineering — D, progressive.** Repair existing vehicles, modify them, assemble modular vehicles, then fabricate original components and vehicles as knowledge and facilities develop. Not a rigid technology gate. Vehicles are component assemblies sharing CORE material and engineering systems; terrain, payload, wear and damage affect performance.
7. **Vehicle operation — C, adaptive realism.** Assisted, manual and specialized control operate the same underlying vehicle physics. Assistance coordinates existing mechanisms and cannot conjure missing components or exceed physical limits. Custom vehicles support configurable controls; NPC driving and self-driving technology are separate.
8. **Physical interaction — C, hybrid.** Players can directly pick up, carry, drag, rotate, position and connect objects, or use contextual and precision-assisted actions. All interaction methods use the same object properties and outcomes. Inventory respects mass, volume and storage; large loads need transport or lifting equipment.

## Cross-system rules
- The same material identity and relevant properties persist through excavation, inventory, storage, salvage, fabrication, construction and recycling.
- No resource duplication through cutting, mining, salvage or manufacturing; losses and byproducts are tracked at an appropriate simulation resolution.
- A building, machine or vehicle remains an assembly of functional components, with inspectable condition and meaningful failure modes.
- Skills are individual and bounded. Player and NPC competence, knowledge, tools and available measurements influence diagnosis, construction and operation.
- Support both direct play and optional assistance; assistance must not bypass physical constraints.
- Save and reload terrain edits, incomplete buildings, object positions, component state, machines, vehicles and reusable blueprints.
- Performance is a design constraint, especially on Android: chunk-based terrain, sleeping objects, assembly grouping, localized solvers, and scalable simulation detail.
- Open-ended engineering is bounded by supported physical models and interactions; this is not a promise of molecular-level simulation.

## Representative gameplay loop
Survey terrain → excavate soil/stone/ore → collect and transport actual material → salvage structures → refine or manufacture components → build a workshop → construct functional machinery → repair or fabricate a vehicle → automate transport and production → persist all world changes.

## Proposed first proof of concept
Dig a smooth trench; recover a measured amount of soil; carry/transport and redeposit it; save and reload the changed terrain. Then validate a simple salvaged component and constructed assembly before advancing to machinery and vehicles.

## Open design questions / not yet approved
- Environmental simulation choice A/B/C/D (weather, water, fire, erosion, ecosystems) remains **unselected**.
- Numerical balancing, exact simulation algorithms, hardware targets and implementation milestones require testing.
- Aircraft, advanced industrial factories and autonomous fleets are longer-term possibilities, not committed first-release features.

## Publication boundary
This addendum records tonight's approved design choices. It does not assert that the features exist in REBIRTH or CORE, and does not change the installed Companion's v0.9 update feed.
