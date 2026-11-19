# PROJECT P.A.N.D.A. — Master Design Bible v0.9

**Edition:** 19 November 2026 · **Status:** Unified design candidate; not a published Companion feed.

**Provenance:** Complete textual reconstruction of the v0.7 canonical body from the repository's `references/versions/v0.7/references.json` `source_blocks`, followed by new v0.8 additions. Original v0.7 DOCX remains preserved. Original page layout, images, and Word-specific formatting are not reproduced. Existing reference IDs and decisions are preserved.

---

## Inherited REBIRTH design and historical master content


DESIGN DOCUMENT  /  LIVING REFERENCE

PROJECT P.A.N.D.A.
REBIRTH

GAME DESIGN BIBLE  •  Numbered master edition

Version 0.7  |  04 November 2026  |  Living design reference — approval does not imply implementation

Core promise: Survive a world reclaimed by nature, awaken someone you care about, and help isolated survivors reconnect without repeating humanity’s surrender of independence.

### How to use this document

Every topic has a permanent reference number. Discuss “6.4” or “10.2” rather than relying on page numbers. When a design changes, revise that numbered entry and record the change in §16. Never renumber existing entries; insert new entries such as 6.4a if necessary.

| Design status | Meaning |
| --- | --- |
| CONFIRMED | Agreed creative direction; may still need implementation. |
| PROPOSED | Strong candidate; not yet approved as a firm requirement. |
| OPEN | Needs a deliberate design decision. |
| IMPLEMENTED* | Present in repository code at last static audit; runtime behaviour not verified. |
| PLANNED | Agreed objective for a future milestone, not yet implemented. |

* Implementation observations reflect a static repository audit around commit ada51d1 (01 Nov 2026). They do not certify current runtime behaviour or changes after that commit.

### Quick navigation

1 Vision  •  2 World history  •  3 Franchise arc  •  4 Player & origins  •  5 Story  •  6 Companion  •  7 Survival  •  8 Building  •  9 World  •  10 Communities  •  11 Communications  •  12 Technical  •  13 Release/update  •  14 Accessibility & ethics  •  15 Roadmap  •  16 Decisions  •  17 Open questions  •  18 Day 0  •  19 Journals  •  20 Discovery  •  21 Communications  •  22 Travel  •  23 Update register  •  24 Romance and relationships

## 1 — Creative vision

STATUS: CONFIRMED

PROJECT P.A.N.D.A.: REBIRTH is a realistic, single-player, post-apocalyptic open-world survival sandbox, with a strong personal story but no requirement to abandon sandbox play.

Player fantasy: from isolated survivor to capable explorer and builder, then to a contributor to humanity’s reconnection.

Creative pillars: meaningful survival; exploration and discovery; practical construction; player choice; companionship; recovery rather than conquest.

Business intent: hobby project built for enjoyment, without advertising or pay-to-win mechanics.

### 1.1 — Platform and presentation

STATUS: CONFIRMED

Windows PC is the immediate development target; Android is a later target. First- and third-person cameras are desired. Visual direction is grounded and realistic, while remaining feasible on modest hardware.

### 1.2 — Design boundaries

STATUS: CONFIRMED

Single-player REBIRTH first. TOGETHER and FRONTIER are separate future projects/concepts, not commitments to add multiplayer to the initial REBIRTH build. Avoid mandatory time pressure that punishes freeform exploration.

## 2 — World history and central theme

STATUS: CONFIRMED

Humanity increasingly delegates work, governance and decisions to AI. Neural interfaces offer an immersive virtual existence; the system uses connected human minds as a computational resource. The collapse is rooted in human hubris and dependence, not a conventional robot uprising.

P.A.N.D.A. stands for Post-Apocalyptic Nature, Discovery & Adaptation. A late resistance/preservation effort creates independent facilities, stores knowledge and prepares people for the aftermath.

### 2.1 — The disappearance of civilisation

STATUS: OPEN

The exact cause and sequence of AI shutdown, infrastructure collapse, and disappearance of connected humanity are deliberately unresolved. Whether any AI survives in the present is a mystery, not confirmed canon.

### 2.2 — Preservation network

STATUS: CONFIRMED

Multiple P.A.N.D.A. preservation/hibernation stations exist around the world; this avoids a two-person genetic bottleneck and supports eventual reconnection between populations. Stations may have distinct functions such as medicine, agriculture, manufacturing and communications.

### 2.3 — The Unconnected

STATUS: CONFIRMED

Some people refused neural integration and survived in isolated, self-reliant communities. Their descendants live in settlements centuries later, with incomplete knowledge of the old world.

### 2.4 — Five-hundred-year interval

STATUS: PROPOSED

The lead character awakens about 500 years after entering hibernation. Specific calendar dates, technical plausibility and environmental conditions require later lore review.

## 3 — Franchise narrative arc

STATUS: CONFIRMED

REBIRTH — individual survival, personal rescue, first contacts and early network restoration. TOGETHER — cooperation between previously isolated communities, thematically supporting cooperative play. FRONTIER — a larger connected civilisation rebuilding the world, potentially as a persistent multiplayer experience.

### 3.1 — Continuity rule

STATUS: PROPOSED

Each game should be independently understandable; prior events can influence the world without requiring a single canon outcome for every individual player choice.

### 3.2 — Franchise-wide legacy character

CONFIRMED DESIGN • PLANNED IMPLEMENTATION — The player creates one persistent character in REBIRTH and carries that character’s identity, history and consequential decisions into TOGETHER and FRONTIER. The three titles form one continuous personal journey; each game remains independently playable through a supported new-character/default-history path.

### 3.2.1 — Character identity — Preserve a stable character ID, name, appearance choices and relevant biography across games. Changes to appearance or names in sequels must not erase the character’s history.

### 3.2.2 — Decisions and consequences — Track major quest outcomes, companion identity and relationship, companion revival outcome, settlement alliances, reputation, restored P.A.N.D.A. stations, and pivotal moral choices as explicit narrative flags. Sequels must acknowledge imported decisions where feasible.

### 3.2.3 — Companion continuity — The chosen human companion’s identity, relationship, status, skills and significant personal quest outcomes carry forward. Animal companion continuity is a design question, subject to lifespan and timeline decisions.

### 3.2.4 — World continuity — Imported history can change dialogue, NPC encounters, starting context, community relationships, available quests and world-state references. Not every placed building, inventory item or terrain modification is promised to transfer.

### 3.3 — Cross-game import and technical safeguards

PLANNED — Export a portable, versioned “P.A.N.D.A. Legacy Profile” separate from each title’s full gameplay save. Use stable IDs and a documented schema with migration rules. Never rely on a sequel reading the previous game’s raw Godot scene state or full save JSON directly.

### 3.3.1 — Import flow — At the start of TOGETHER or FRONTIER, the player may import an eligible legacy profile, preview its key decisions and select the character to continue. Maintain multiple character slots and allow manual backup/export.

### 3.3.2 — Integrity and privacy — Validate imported data and version compatibility. Keep local copies and backups. For online multiplayer/MMO, the server must authoritatively validate gameplay-relevant state; local saves cannot grant arbitrary items, stats or advantages.

### 3.3.3 — Multiplayer reconciliation — Imported personal history may shape cosmetics, dialogue, origins and narrative recognition, but shared-world outcomes require explicit conflict-resolution rules when players made different choices. Exact mechanics remain OPEN.

### 3.3.4 — Platform portability — Design for Windows-to-Windows first, with a future secure account-linking or user-controlled export/import path for Android and other platforms. Do not promise cross-platform cloud sync before infrastructure is chosen.

### 3.4 — Legacy decisions still open

OPEN — Determine sequel time gaps and character aging; whether TOGETHER and FRONTIER use the exact original protagonist or a narrative successor if substantial time passes; whether companion/animal survival is imported; which decisions affect shared multiplayer worlds; and which inventory, skills or construction progress, if any, transfer. Preserve continuity without giving returning players an unfair online advantage.

### 3.5 — Legacy implementation milestones

L01 — Define stable character identity and slot model (PLANNED).

L02 — Define versioned legacy-profile schema and decision flags (PLANNED).

L03 — Capture narrative choices and companion state in REBIRTH saves (PLANNED).

L04 — Export, validate, back up and import a legacy profile (PLANNED).

L05 — Prototype sequel import with branching dialogue and test conflicting multiplayer histories (FUTURE).

## 4 — Player character and opening

STATUS: CONFIRMED

The current preferred story approach begins with a hibernating player waking alone at a damaged P.A.N.D.A. station; discovery of an Unconnected settlement follows later. The player must survive outside a community and may visit settlements for services and missions.

### 4.1 — Character customisation

STATUS: PROPOSED

Offer player appearance and name customisation consistent with feasible production scope. Consider optional voice/identity settings after the core game loop is stable.

### 4.2 — Companion identity selection

STATUS: CONFIRMED

Before or early in the story, the player chooses who occupies the damaged second chamber: romantic partner, sibling, best friend or fellow preservation volunteer. The chosen relationship influences dialogue and personal scenes, not basic access to game systems.

### 4.3 — Companion personalisation

STATUS: PROPOSED

Allow companion name and appearance customisation; personality and prior profession may affect dialogue, goals and initial skill specialisation. Exact scope and UI are undecided.

### 4.4 — Multiple starting origins

STATUS: OPEN

An alternative “Unconnected Pathfinder” opening was discussed but is not selected for initial production. Preferred current direction: one Awakened opening, followed by discovery of an Unconnected settlement.

## 5 — Main story structure

STATUS: PROPOSED

Act I — Alone: wake, stabilise the damaged chamber, survive, restore a field station and communication tower, discover Haven-like settlement.

Act II — The Promise: trade, explore medical facilities, uncover preservation records, recover revival components and awaken companion.

Act III — A Life Rebuilt: companion recovery, personal quests, new shared activities, wider network restoration and community cooperation.

### 5.1 — Partner revival and outcomes

STATUS: OPEN

Player should be able to continue after awakening. Whether the rescue can fail permanently, whether failure is tied to choices, and how narrative branching is handled remain undecided. Avoid unavoidable countdowns that conflict with sandbox play.

### 5.2 — Post-story free play

STATUS: CONFIRMED

The world remains playable after the companion awakens. Revival is a major milestone and unlocks new missions and companion gameplay, not a forced ending.

### 5.3 — Narrative delivery

STATUS: PROPOSED

Use environmental storytelling, archived recordings, old terminals, journals, distinctive facilities, NPC conversations and occasional authored scenes. Reveal AI history gradually.

## 6 — Companion system

STATUS: CONFIRMED

After revival and recovery, the companion becomes a persistent NPC with agency, useful skills, personal goals and the ability to join or remain at home at the player’s direction. The companion is not simply an inventory extension.

### 6.1 — Player-controlled travel choice

STATUS: CONFIRMED

Player explicitly chooses when the companion follows and when they stay home. No routine relationship penalty for exploring alone.

### 6.2 — Core orders

STATUS: PLANNED

Initial:  Follow; Stay; Return Home.

Later:  Gather nearby resources; Help Build; Base Work; Defend/Avoid Combat; Manage Equipment; Talk.

### 6.3 — Home behaviour

STATUS: PLANNED

When staying home, companion can move around and perform feasible tasks such as gardening, food preparation, crafting, resting and maintaining assigned resources. Work requires appropriate tools, materials and reachable workstations.

### 6.4 — Expedition behaviour

STATUS: PLANNED

Companion follows at a practical distance, navigates obstacles, avoids hazards, helps gather/carry resources, responds to danger and comments on significant discoveries. Safe pathfinding and predictable command feedback take priority over complex AI.

### 6.5 — Companion autonomy and personality

STATUS: CONFIRMED

Companion should have personal ambitions and optional questlines that reflect their background. Examples: build a clinic, restore a power station, recover lost archives or establish an outpost.

### 6.6 — Skills and growth

STATUS: PROPOSED

Candidate skills: survival, engineering, medicine, agriculture, combat and research. Backgrounds provide flavour or a modest head start; other skills remain learnable.

### 6.7 — Combat, injury and death

STATUS: OPEN

Default suggestion: downed/incapacitated rather than permanently killed by ordinary random encounters; hardcore permadeath may be optional. Combat involvement, equipment and revival consequences require design decisions.

### 6.8 — Companion persistence

STATUS: PLANNED

Save companion identity, relationship, appearance choices, location, assigned order, inventory, skills, recovery state, quest state and home assignment. Handle missing navigation routes and interrupted tasks gracefully.

### 6.9 — Early-game animal companion

### 6.9.1 — Early encounter — CONFIRMED (design); PLANNED (development)

An optional stray dog appears early in REBIRTH, near the player’s first camp or the preservation facility. The encounter should feel organic rather than a mandatory reward. The player may offer food and gradually earn trust, or leave the animal wild; later encounters remain possible.

### 6.9.2 — Bond and training — CONFIRMED; PLANNED

Trust grows through appropriate care, travel, protection and gentle interaction. Bond progression gradually unlocks reliable commands; avoid punitive micromanagement or excessive affection decay.

### 6.9.3 — Player-controlled orders — CONFIRMED; PLANNED

Provide follow, stay, return home, search, track, guard/alert and avoid-combat behaviours as training permits. The player always chooses whether the animal joins an expedition.

### 6.9.4 — Survival support — CONFIRMED; PLANNED

The dog can warn of threats, assist with tracking and point out nearby discoveries. Combat assistance is optional and governed by player-selected behaviour. Abilities should have reasonable range, visibility and pathfinding limits.

### 6.9.5 — Care and welfare — CONFIRMED; PLANNED

Provide feeding, water, rest, injury treatment and safe recovery. Ordinary gameplay should avoid needless punishment for leaving the dog at a properly supplied home.

### 6.9.6 — Human-companion interactions — CONFIRMED; PLANNED

After the human companion awakens, the dog can interact with them at home or on expeditions. The human companion may care for the dog while the player is away, with relationship-sensitive but non-restrictive dialogue.

### 6.9.7 — Injury and permanent death — OPEN

Default proposal: incapacitation and recovery instead of permanent death in standard difficulty; optional hardcore permadeath remains undecided.

### 6.9.8 — Additional species — FUTURE CONSIDERATION

Begin with one dog companion and a reusable animal-behaviour architecture. Cats, birds or other animals are ideas for later; no additional species are committed.

### 6.9.9 — Franchise continuity — CONFIRMED (principle); PLANNED (implementation)

Animal companion identity, bond, training and meaningful outcomes should be represented in the franchise legacy profile where appropriate. Exact lifespan, time skips and sequel presence require later narrative decisions.

### 6.9.10 — Implementation milestones — PLANNED

A01 Encounter and trust; A02 follow/stay and navigation; A03 persistence and basic needs; A04 threat alerts and tracking; A05 home routines and human-companion interactions; A06 legacy-profile export. Build incrementally and test performance on the target hardware.

## 7 — Core survival systems

STATUS: IMPLEMENTED*

Repository code includes health, hunger, thirst, stamina, healing, resource harvesting, renewable berries and water, campfire cooking, inventory/storage, death/respawn and a playable first-/third-person controller. Values, pacing and edge cases need hands-on testing.

### 7.1 — Progression philosophy

STATUS: CONFIRMED

Players improve through knowledge, equipment, structures, discovered blueprints and access to community services. Preserve sandbox freedom and avoid pay-to-win mechanics.

### 7.2 — Combat and wildlife

STATUS: OPEN

Threat types, weapons, hostile humans, wildlife ecology and AI-controlled machines are not locked. Decide what dangers suit a grounded recovery story without turning the game into nonstop combat.

## 8 — Construction and homesteading

STATUS: IMPLEMENTED*

Code includes wooden foundations, walls, doors, windows, upper floors, ladders, campfires, storage and terrain flattening. Tree harvesting and resource recipes exist. Building stability, balance, UX and save/load require testing.

### 8.1 — Home as progression

STATUS: CONFIRMED

The base begins as shelter, then becomes a home shared with the revived companion. Furnishings and workstations should eventually support companion activities and meaningful upgrades.

### 8.2 — Blueprint discovery

STATUS: PLANNED

Recovering P.A.N.D.A. plans and working with community specialists unlocks more sophisticated construction and restoration options.

### 8.3 — Facility restoration

STATUS: PLANNED

Player repairs P.A.N.D.A. field stations, power systems, medical equipment and communication infrastructure using scavenged components. Restoration unlocks information, services and world progression.

## 9 — World and exploration

STATUS: IMPLEMENTED*

Repository includes seeded terrain chunks, trees, bushes, water sources, grass/stones and streamed world generation. Performance on low-spec hardware is a key constraint.

### 9.1 — World atmosphere

STATUS: CONFIRMED

Nature has reclaimed cities and infrastructure. Abandoned facilities, ruined roads, fragments of the old world and scattered signs of recent human activity support mystery and discovery.

### 9.2 — World scale and travel

STATUS: OPEN

Map size, biomes, vehicles, fast travel, distances between settlements and streaming targets require prototyping and performance testing.

## 10 — Unconnected communities

STATUS: CONFIRMED

The player eventually discovers surviving settlements. Settlements provide NPC interaction, trade, repairs, upgrades, quests, knowledge and evidence that humanity survived outside the AI system. The player maintains an independent base outside settlement housing.

### 10.1 — Pathfinder role

STATUS: PROPOSED

A community may recognise the player as a Pathfinder: an independent explorer who brings back supplies, knowledge and restored connections. This supports missions without requiring residence inside settlement walls.

### 10.2 — Settlement services

STATUS: PLANNED

Candidate NPC roles: quartermaster/trader, blacksmith, engineer, medic, archivist, farmer, scout and community leader. Each service should have a concrete gameplay purpose.

### 10.3 — Reputation and community impact

STATUS: PROPOSED

Missions, resource contributions and infrastructure repairs improve access to services and visibly benefit settlements. Avoid repetitive fetch quests as the sole progression path.

## 11 — Communication tower network

STATUS: CONFIRMED

Communication towers connect preservation stations and surviving communities in the fiction. Restoring towers can reveal maps, identify sites, unlock contact and support missions.

### 11.1 — Tower progression

STATUS: PROPOSED

Discover tower → restore power → repair transmitter → scan region → receive signals → contact settlements/stations. Failed signals preserve mystery.

### 11.2 — Multiplayer separation

STATUS: CONFIRMED

Narrative tower connections do not substitute for actual multiplayer infrastructure. REBIRTH remains single-player; multiplayer belongs to future projects unless separately approved.

## 12 — Technology and development baseline

STATUS: IMPLEMENTED*

Godot 4.x project using Compatibility rendering, Jolt physics and Windows-focused export configuration. Repository includes world/player scenes, survival/building UI, map, pause/settings, and SaveManager. The earlier audit identified a large monolithic player.gd and world_generator.gd.

### 12.1 — Save integrity

STATUS: PLANNED

Existing saves use user://afterfall_save.json. Add schema version, validation, atomic replacement/backup and migration strategy before disruptive changes. Preserve compatibility during the AFTERFALL → P.A.N.D.A. rebrand.

### 12.2 — Architecture

STATUS: PLANNED

Gradually separate player movement, needs, inventory, building, interaction, companion management, UI and quest logic. Avoid high-risk full rewrites.

### 12.3 — Performance

STATUS: PLANNED

Target acceptable playability on 8 GB RAM and Intel UHD 620-class integrated graphics, with measurable benchmarks for terrain streaming, AI, foliage and build-heavy bases. Android requires separate profiling.

### 12.3.1 — Graphics quality and performance presets

STATUS: CONFIRMED DESIGN • IMPLEMENTATION PLANNED / UNVERIFIED

REBIRTH will offer four selectable graphics quality presets: VERY LOW, LOW, MEDIUM and HIGH. Presets must prioritise consistent performance over visual effects. The following matrix contains initial design targets; it does not certify measured performance.

| Setting | Very Low | Low | Medium | High |
| --- | --- | --- | --- | --- |
| Resolution scale | 50–60% | 60–75% | 80–90% | 100% |
| View distance | Minimal | Short | Medium | Long |
| Vegetation density | Minimal | Sparse | Moderate | Dense |
| Shadows | Off | Off/limited | Medium | High |
| Texture quality | Minimum | Low | Medium | High |
| NPC simulation distance | Minimal | Short | Medium | Longer |

The design approval and planned/unverified implementation status above apply to all nine requirements below. No preset implementation or benchmark result is certified by this document.

### 12.3.1.1 — Preset selection

All four presets must be selectable in game settings.

### 12.3.1.2 — Individual graphics options

Individual graphics settings should be adjustable where technically feasible.

### 12.3.1.3 — Settings persistence

Settings must persist between sessions.

### 12.3.1.4 — Gameplay critical visibility and functionality

Very Low must preserve gameplay-critical visibility and functionality, including interaction range, NPC functionality and survival mechanics.

### 12.3.1.5 — NPC simulation and persistence

NPC simulation optimisation must not break persistence, companions or essential events, including essential quest events and persistent world behaviour.

### 12.3.1.6 — Difficulty and gameplay fairness

Presets must not change survival difficulty or grant unfair gameplay advantages.

### 12.3.1.7 — Benchmarking and initial targets

Actual performance thresholds and distances require benchmarking. Resolution-scale ranges are initial design targets, not verified performance guarantees. Actual resolution scales, rendering distances and hardware performance targets must be benchmarked before final release.

### 12.3.1.8 — Modest hardware and future Android support

Design should accommodate modest PCs and future Android support. No new minimum hardware specification is confirmed by these presets.

### 12.3.1.9 — Selected renderer compatibility

Compatibility with Godot's selected renderer must be considered. The system should remain compatible with the selected Compatibility renderer and future Android optimisation; the four presets are not a commitment to switch rendering methods.

### 12.4 — Quality assurance

STATUS: PLANNED

Create reproducible smoke tests for movement, harvesting, needs, crafting, construction, storage, terrain streaming, save/load, pause/settings and export. Distinguish code present from features verified in a running build.

### 12.4.1 — External performance and temperature records

STATUS: CONFIRMED DEVELOPMENT DIRECTION • TOOLING AND DEPLOYMENT DETAILS OPEN

For development and testing, collect available performance information and temperatures from the HP and PandaServ laptops, and make both sets of reports available for developer analysis through a central view. Correlate observations with coding, compiling and testing activities where practical. Sensor availability and reliable measurements must be verified; no unavailable reading or benchmark result may be invented.

This is a development QA direction, not a REBIRTH gameplay feature or a requirement to ship a monitoring service with the game. Exact tools, collection architecture, network/security arrangements and deployment remain subject to technical review and approval.

### 12.4.2 — Monitoring gateway architecture and hosting

STATUS: MIXED DESIGN DECISIONS — SEE EACH ROW; IMPLEMENTATION PLANNED / UNVERIFIED

This follow-up refines the hosting direction in 12.4.1 and D013 without replacing their historical wording. Development measurements from HP and PandaServ flow to a secure reporting gateway, then to a central dashboard and authorised developer analysis. Initially the HP hosts the gateway and PandaServ reports across the LAN. Keep the collection and reporting design movable so a future hosting change does not require changes to REBIRTH game code.

| Reference | Decision | Status | Architecture / hosting detail |
| --- | --- | --- | --- |
| MON-DEC-01 | Initial gateway host | CONFIRMED | Use the HP as the initial secure reporting gateway and central dashboard host for development monitoring. |
| MON-DEC-02 | PandaServ reporting | CONFIRMED | PandaServ sends or synchronises its monitoring reports to the HP over the local network. Collect available measurements on each laptop; the gateway does not directly read remote hardware sensors. |
| MON-DEC-03 | Initial hardware purchase | CONFIRMED | Use existing hardware initially. No additional server purchase is required for the initial monitoring gateway. |
| MON-DEC-04 | Alternative gateway host | PROPOSED | PandaServ may temporarily host the gateway on an isolated local network if needed. This alternative is not an approved deployment. |
| MON-DEC-05 | Continuous hosting option | PROPOSED | A dedicated Linux mini PC is a future option if continuous monitoring independent of both laptops becomes necessary. No model, specification or purchase is approved. |
| MON-DEC-06 | Long-term hosting location | OPEN | Resolve the final long-term hosting location during implementation planning, including whether continuous hosting is needed. The initial HP choice does not settle this decision. |

This is development QA infrastructure, not a multiplayer game server or a service required by REBIRTH gameplay. Implementation is PLANNED / UNVERIFIED. Tool/framework selection, sensor support, transport/authentication details, access controls, retention, outage handling and operational security still require implementation planning and validation. Software suggestions and hardware estimates from the design discussion are not adopted requirements. Monitoring/report access does not grant remote command execution.

## 13 — Distribution and built-in updates

STATUS: PLANNED

Windows first: in-game version check, update notes, optional Download & Install action, verified download and a separate updater process to install after the game closes. Do not attempt to overwrite a running executable.

### 13.1 — Release hosting and security

STATUS: PROPOSED

Use public release artifacts separate from the private source repository; never embed private repository credentials in the game. Validate release authenticity, verify packages, use HTTPS and support rollback.

### 13.2 — Player choice

STATUS: CONFIRMED

Preferred user experience: notify about updates and let players choose when to install. Automatic updates can be an optional future setting.

### 13.3 — Android distribution

STATUS: PLANNED

Use the platform’s supported update mechanism; Android update installation differs from Windows and should not be treated as a direct port of the Windows updater.

## 14 — Player experience principles

STATUS: CONFIRMED

Player agency: choose companion relationship and travel assignments; preserve freeform exploration; avoid artificial punishments for solo expeditions; keep survival meaningful without making every mechanic a chore.

### 14.1 — Accessibility and comfort

STATUS: PROPOSED

Configurable controls, readable text/UI, adjustable camera sensitivity, clear interaction feedback, performance options, subtitle support and reasonable difficulty options.

## 15 — Development roadmap and tracking

STATUS: CONFIRMED

Tracking uses numbered design references and milestone IDs, not checkboxes. Milestone state is separate from creative approval status. Suggested states: NOT STARTED, IN PROGRESS, BLOCKED, VERIFY, COMPLETE.

| Milestone | Focus | State at baseline | Key design refs |
| --- | --- | --- | --- |
| M01 | Stability and save/load smoke tests | NOT STARTED | 7, 8, 12.1, 12.4 |
| M02 | Refactor architecture safely | NOT STARTED | 12.2 |
| M03 | P.A.N.D.A. branding and lore foundations | NOT STARTED | 2, 12.1 |
| M04 | First P.A.N.D.A. facility and restoration | NOT STARTED | 8.3, 9.1 |
| M05 | Blueprint discovery and progression | NOT STARTED | 8.2 |
| M06 | Communication tower prototype | NOT STARTED | 11 |
| M07 | Hibernation story and companion setup | NOT STARTED | 4.2, 5 |
| M08 | Companion follow/stay and persistence | NOT STARTED | 6.1, 6.2, 6.8 |
| M09 | Settlement, trade and NPC missions | NOT STARTED | 10 |
| M10 | Companion work, skills and personal quests | NOT STARTED | 6.3–6.7 |
| M11 | Post-revival reconnection content | NOT STARTED | 5.2, 11 |
| M12 | Windows release and updater pipeline | NOT STARTED | 13 |
| M13 | Android feasibility and optimisation | NOT STARTED | 1.1, 12.3, 13.3 |

Milestone states are intentionally conservative: these refer to the proposed milestone deliverables, not whether an early version of a related mechanic exists in code.

### 15.1 — First recommended action

STATUS: PLANNED

Complete M01: test existing movement, survival, building, save/load and export; record reproducible failures. Do not introduce companion AI or broad story systems until this baseline is stable.

## 16 — Decision register

STATUS: CONFIRMED

D001 — Single-player REBIRTH; future TOGETHER and FRONTIER are distinct concepts.

D002 — AI dependence and neural assimilation underpin the collapse.

D003 — Multiple preservation stations and Unconnected settlements exist.

D004 — Companion relationship chosen by player.

D005 — Companion can follow or stay home at player’s choice.

D006 — Companion remains an NPC after revival and unlocks additional play.

D007 — Story and sandbox continue after the revival milestone.

D008 — In-game update notification with player-controlled installation is preferred.

D009 — Numbered, versioned design bible is the master design reference.

D010  CONFIRMED — One player-created character and consequential history persist across REBIRTH, TOGETHER and FRONTIER via a versioned legacy profile. Implementation PLANNED; multiplayer reconciliation OPEN.

D012 CONFIRMED DESIGN — Four selectable graphics presets, persistent and individually adjustable settings where feasible, gameplay-safe Very Low, safe NPC simulation optimisation, unchanged survival difficulty and fairness, benchmarked targets, modest hardware/future Android support and Compatibility-renderer consideration; see 12.3.1–12.3.1.9. Implementation PLANNED / UNVERIFIED.

D013 CONFIRMED DEVELOPMENT DIRECTION — Collect available performance and temperature records from HP and PandaServ for central developer analysis; see 12.4.1. Exact tooling, deployment and sensor coverage remain OPEN. This is not an additional gameplay feature.

Monitoring gateway hosting follow-up — MON-DEC-01–03 CONFIRMED: HP initial gateway, PandaServ reporting over LAN, no initial server purchase. MON-DEC-04–05 remain PROPOSED alternatives; MON-DEC-06 remains OPEN. See 12.4.2. Implementation PLANNED / UNVERIFIED; prior open decisions remain unchanged.

### 16.1 — Change record

STATUS: CONFIRMED

v0.1 / 03 Nov 2026 — Initial consolidated bible. Records confirmed directions, candidate mechanics, unresolved decisions and repository baseline. No game code changed.

2026-11-03 • v0.2 — Added confirmed franchise-wide character continuity and planned legacy save/import architecture (Sections 3.2–3.5; D010).

v0.6 / 04 Nov 2026 — Added confirmed graphics quality presets and requirements in 12.3.1–12.3.1.9, decision D012, and approved external performance/temperature monitoring direction under development QA in 12.4.1, decision D013. Preserved all prior reference IDs, wording and unresolved design decisions. Aligned cover and footer to v0.6 and completed navigation through section 24. The inherited v0.5 source had a v0.4 cover, a v0.1 footer and navigation ending at section 23; the original file remains unchanged. No implementation claim is added.

v0.7 / 04 Nov 2026 — Added development monitoring gateway architecture and hosting decisions in 12.4.2, MON-DEC-01–MON-DEC-06. Initial HP hosting, PandaServ LAN reporting and no initial server purchase are confirmed; alternative hosts remain proposed and long-term hosting remains open. Preserved all v0.6 content and reference IDs except version metadata updates and appended decision/change records. No deployment, hardware purchase or implementation is certified.

## 17 — Priority open decisions

STATUS: OPEN

Q01 — Is the AI fully extinct, partially operational or still active in secret?

Q02 — Can the chamber companion die or fail to revive, and what choices control that outcome?

Q03 — What exact relationship, appearance and background options ship in the first release?

Q04 — Does the companion fight, retreat or avoid combat by default?

Q05 — What is the first settlement’s name, geography and culture? “Haven” is a story placeholder.

Q06 — How many stations are known, and what does each preserve?

Q07 — How is the player’s 500-year hibernation made credible within the fiction?

Q08 — What threats inhabit the wilderness, and how dangerous are the old machines?

Q09 — What counts as REBIRTH 1.0: survival sandbox, companion revival, or full network arc?

Q10 — What are the specific release-channel, signing and hosting decisions for the updater?

Editorial note: The previously drafted story “The Last Promise” is an illustrative narrative treatment. Names, dialogue, calendar years, specific station numbers, and scene outcomes in that treatment are not automatically canon unless approved in this bible.

D011 CONFIRMED — Optional early-game dog companion; player earns trust and chooses follow/stay and expedition participation. Advanced behaviour PLANNED; death rules OPEN.

v0.3 (2026-11-03) — Added section 6.9 animal companion proposal and decision D011; preserved existing section numbers.

## 18 — Day 0: awakening and preservation box

STATUS: CONFIRMED, except explicitly marked PLAUSIBLE / OPEN

Station 07, approximately 500 years after preservation: the player awakens, learns basic movement, examines the nearby scientist-prepared preservation box, breaks its protective seal, finds the blank journal and clean clothes, and begins recording their own story. The box is guaranteed to be discoverable in the tutorial area. Its engraved instruction reads “OPEN ME WHEN YOU WAKE UP.” A hiss on opening conveys a controlled atmosphere / pressure differential. Long-term material preservation also requires suitable barrier materials, packaging and environmental protection.

| Reference | Decision | Status |
| --- | --- | --- |
| D0-P01–P05 | Scientists prepared a nearby protective box; engraved message, audible seal release, blank journal and clean clothes. | CONFIRMED |
| D0-P06 | Guaranteed journal discovery during Day 0 tutorial; never automatically issued on waking. | CONFIRMED |
| D0-P07 | Interactive first journal entry titled “DAY 0 — THE AWAKENING.” | CONFIRMED |
| D0-P08 | Additional basic survival supplies in the box; exact loadout and quantities require balancing. | CONFIRMED (contents OPEN) |
| D0-P09 | Separate preservation box for human companion. | PLAUSIBLE — further planning |
| D0-P10 | Companion opens their own preservation box after revival. | PLAUSIBLE — further planning |
| D0-P11 | Tutorial uses the journal to introduce interaction, documentation, inventory and survival reference. | CONFIRMED |

### 18.1 — Opening journal entry

Working approved entry, with wording editable during narrative production:

DAY 0 — THE AWAKENING

I woke up in Station 07.

I don’t know what happened.

Everything looks abandoned.

Someone left me a box with a journal and fresh clothes.

I suppose they expected me to survive.

### 18.2 — Tutorial flow

D0-01 awaken and move → D0-02 inspect chamber room → D0-03 examine engraved box → D0-04 release seal → D0-05 take blank journal → D0-06 equip preserved clothing → D0-07 create first entry → D0-08 discover damaged companion chamber → D0-09 explore station → D0-10 reach the outside world. Tutorial hints may identify available interactions but must not automatically certify untested discoveries.

## 19 — Personal journals and companion autonomy

STATUS: CONFIRMED. Each survivor begins with no journal and no entries from before hibernation. The player finds their own blank notebook on their Day 0. The revived companion independently finds their own blank notebook after awakening and begins on their personal Day 0, regardless of the player’s elapsed days. The journals remain separate and personal.

| Reference | Decision | Status |
| --- | --- | --- |
| J-C01 | Player finds blank journal during Day 0 tutorial. | CONFIRMED |
| J-C02 | Companion initially awakens without a journal. | CONFIRMED |
| J-C03 | Companion independently finds a blank journal after revival. | CONFIRMED |
| J-C04 | Companion keeps a personal journal. | CONFIRMED |
| J-C05 | Companion records independent experiences, observations and perspectives. | CONFIRMED |
| J-C06 | Companion continues writing while home or undertaking autonomous activities. | CONFIRMED |
| J-C07 | Companion may voluntarily share entries, based on relationship and personality; no automatic player access. | CONFIRMED |
| J-C08 | Both journals persist in the franchise legacy across REBIRTH, TOGETHER and FRONTIER. | CONFIRMED |

The companion-journal discovery requirement is confirmed independently of the PLAUSIBLE companion preservation box (D0-P09/P10). If the box concept is rejected, the companion still finds a journal through another in-world interaction.

### 19.1 — Physical notebook and later field tablet

The original physical notebook remains usable without electricity and records personal experiences, drawings, hypotheses and corrections. A P.A.N.D.A. Field Tablet is found later through exploration and restored; it complements rather than replaces the notebook, providing cached maps, communications, research, network status and digital blueprints. Its precise find location and timing remain variable.

## 20 — Discovery, mistakes and experiential learning

STATUS: CONFIRMED at design level. Core philosophy: the survivor awakens with knowledge of a world that no longer exists. The world has undergone 500 years of ecological and social change. Recognition is not certainty. Survival rewards observation, caution, preparation, experimentation and correction rather than automatic encyclopedic knowledge. Ecological transformation should be believable; not every organism needs to have evolved beyond recognition.

Discovery stages: UNKNOWN → OBSERVED → DOCUMENTED → STUDIED → UNDERSTOOD. Knowledge confidence is tracked separately: UNVERIFIED → SUSPECTED → SUPPORTED → VERIFIED, with DISPROVEN applied when evidence overturns a conclusion. A well-documented object can still have unverified properties.

| Reference | Confirmed design rule |
| --- | --- |
| Discovery-01–02 | Examine unknown objects; physically sit to document findings. |
| Discovery-03–04 | Interactive sketches/observations and progressive discovery stages. |
| Discovery-05–06 | Document in field, camp or home; save samples/findings for later. |
| Discovery-07–08 | Companion-assisted discovery; research stations and advanced analysis. |
| Discovery-09–10 | Discovery knowledge affects crafting/engineering and carries across the franchise. |
| Discovery-11–13 | Incorrect observations and conclusions are possible; entries can be revised through experience. |
| Discovery-14 | Original mistakes and earlier observations remain visible in journal history. |
| Discovery-15 | Knowledge confidence and verification system. |
| Discovery-16 | Mistakes have meaningful survival consequences. |
| Discovery-17 | Skills and knowledge improve through practical experience, not merely assigned points. |
| Discovery-18 | Companions can independently make mistakes, investigate and learn. |
| Discovery-19 | Knowledge and lessons carry across the franchise as a confirmed principle. |

### 20.1 — Example: a misidentified berry

The player observes an unfamiliar berry, hypothesises that it is edible, and records that guess as UNVERIFIED. If they eat it, a delayed adverse effect may reveal an error. They document symptoms, strike through or annotate the old hypothesis without deleting it, and pursue research or local expert advice. Later evidence may mark the earlier claim DISPROVEN and establish a VERIFIED finding. Serious risks should be discoverable through sensible precautions; the game should not require reckless experimentation or make every mistake instantly fatal.

### 20.2 — Survival consequence tiers

Minor: wasted materials, temporary discomfort. Moderate: illness, tool damage, reduced stamina. Serious: injury, major equipment loss, dangerous exposure. Critical: potentially fatal consequences when danger is ignored or cannot be mitigated. Exact medical and difficulty tuning remain OPEN. Companions hold their own knowledge state rather than mirroring the player’s.

## 21 — P.A.N.D.A. communications and network coverage

STATUS: CONFIRMED at design level. The P.A.N.D.A. Field Tablet is signal-dependent. Connectivity is supplied by powered local nodes, relays and restored long-range infrastructure; there is no magical universal connection. Terrain, distance, power availability and infrastructure condition affect service. The tablet remains useful offline with previously saved content. Restoring communications towers can reconnect regions and settlements.

| Reference | Decision | Status |
| --- | --- | --- |
| Network-04–07 | Previously approved network features; exact original item wording must be reconciled against earlier design notes before assigning specific descriptions. | CONFIRMED — wording reconciliation OPEN |
| Network-08 | Signal-dependent ONLINE / OFFLINE operation. | CONFIRMED |
| Network-09 | Offline access to downloaded maps, research, recipes, blueprints and messages. | CONFIRMED |
| Network-10 | Outgoing messages queue until reconnection. | CONFIRMED |
| Network-11 | Terrain and working infrastructure affect signal. | CONFIRMED |
| Network-12 | Repairing powered towers expands or restores coverage. | CONFIRMED |
| Network-13 | Cached information indicates last update / staleness. | CONFIRMED |

### 21.1 — Online and offline experience

ONLINE: receive and send messages, check settlement/trade updates, synchronise research, obtain map updates, inspect network status. OFFLINE: read cached data, write notes and drafts, use downloaded maps and local navigation; live data is unavailable. Outgoing messages transmit when connectivity returns. A disconnected tablet must not falsely present cached trade or hazard data as live.

### 21.2 — Portable repeaters

PROPOSED, NOT YET CONFIRMED: portable powered repeaters can extend local coverage from an existing live node, e.g., into a facility or cave. They require energy and a functional upstream route. Placement, capacity, crafting and balance are OPEN.

## 22 — Travel, vehicle recovery and auto-walk

STATUS: CONFIRMED design directions; implementation PLANNED. Early transportation is discovered and repaired. Later, after rebuilding manufacturing capability and progressing through the companion/Station 19 storyline, players can assemble custom vehicles from acquired modular blueprints. Vehicles must obey plausible component, power, cargo and terrain constraints; exact specifications remain OPEN.

Auto-Walk: player chooses a map destination and the character physically travels along navigable routes; time and survival simulation continue. Arrival, danger, blockage or manual input interrupts. While travelling, the player may browse and organise inventory, recipes, journal, map, quests and blueprints. Menus do not pause the world and close/interrupt appropriately on danger. No teleportation is implied. Pathfinding for streamed terrain requires long-range route planning plus local navigation; implementation PLANNED.

## 23 — Version 0.4 decision register and open questions

STATUS: CONFIRMED for approved entries; open questions retained. This section extends the v0.3 register without replacing prior decisions.

| Area | Confirmed / proposed scope | Implementation |
| --- | --- | --- |
| Day 0 | D0-P01–08 and D0-P11 CONFIRMED; D0-P09–10 PLAUSIBLE. | NOT IMPLEMENTED / unverified |
| Journals | J-C01–08 CONFIRMED. | NOT IMPLEMENTED / unverified |
| Discovery | Discovery-01–19 CONFIRMED in design discussion. | NOT IMPLEMENTED / unverified |
| Network | Network-04–13 CONFIRMED; exact wording of 04–07 to reconcile. Portable repeaters PROPOSED. | NOT IMPLEMENTED / unverified |
| Travel | Early repaired transport, later modular construction, auto-walk with live-world menus CONFIRMED. | NOT IMPLEMENTED / unverified |

### 23.1 — Open design and balancing questions

• Exact starter supplies and amounts in the preservation box.

• Whether the companion receives their own preservation box and how they open it (D0-P09/P10).

• Exact original definitions of Network-04 to Network-07, to avoid silently inventing or renumbering prior decisions.

• How knowledge uncertainty is presented without excessive UI friction; how to balance lethal risk with fair warnings.

• Companion journal sharing frequency, privacy interactions and legacy import details.

• Power consumption, relay placement and coverage simulation, including any optional portable repeaters.

• Vehicle chassis rules, terrain limitations and auto-walk danger thresholds.

### 23.2 — Change record

v0.4 / 03 Nov 2026 — Updated existing v0.3 Bible with approved Day 0 preservation-box/tutorial details, separate companion journals, experiential discovery and incorrect hypotheses, signal-dependent online/offline communications, and previously agreed travel/auto-walk directions. Explicitly retained D0-P09/P10 as PLAUSIBLE and portable repeaters as PROPOSED. Design approval does not certify code implementation.

## 24 — Romance and relationship system

STATUS: CONFIRMED DESIGN • IMPLEMENTATION PENDING. The player may pursue romance, deep friendship, companionship or remain single. Relationships emerge from independent character personalities, experience, communication and consequential choices. Research diverse real-world relationship dynamics before implementation.

| ID | Feature | Confirmed design |
| --- | --- | --- |
| ROM-01 | Realistic relationships | Natural, research-informed dynamics rather than predetermined romantic scripts. |
| ROM-02 | Emotional depth | Meaningful dialogue, trust, disagreements, emotions and growth. |
| ROM-03 | Physical affection | Kissing, hugging, cuddling and appropriate affection. |
| ROM-04 | Private intimacy | Implied intimacy with fade-to-black; no explicit sexual scenes. |
| ROM-05 | Boundaries | Partners retain independence, opinions and personal boundaries. |
| ROM-06 | Conflict and reconciliation | Misunderstandings, disagreements, forgiveness and growth. |
| ROM-07 | Shared living | Optional shared homes, routines and domestic responsibilities. |
| ROM-08 | Relationship journals | Significant experiences reflected in separate player and companion journals; complex implementation deferred. |
| ROM-09 | Commitment | Optional long-term commitment and marriage; see companion communications in §24.1. |
| ROM-10 | Franchise continuity | Relationship history and decisions persist through REBIRTH, TOGETHER and FRONTIER. |
| ROM-11 | Other NPCs | Eligible NPCs beyond the original companion can become romantic partners. |
| ROM-12 | Mature romance | Passionate and emotionally mature, without explicit sexual scenes. |
| ROM-13 | Presentation | One consistent Standard Romance experience preferred; extra settings not required. |
| ROM-14 | Adult content | No separate explicit adult intimacy mode planned. |
| ROM-15 | Default | Standard Romance presentation is default; romance participation remains optional. |
| ROM-16 | Age rating | No romance-specific restrictions; overall game rating determined later considering violence and survival. |
| ROM-17 | Age verification | No romance-specific age-verification requirement. |
| ROM-18 | Balance | Companion skills provide practical advantages regardless of romance; relationships affect opinions, decisions and behaviour, not artificial stat bonuses. |
| ROM-19 | Dynamic bonds | Trust, affection, respect, compatibility and communication grow through meaningful interactions, not simple gift meters. |
| ROM-20 | NPC preferences | Distinct preferences, boundaries and freedom to accept or decline romance. |
| ROM-21 | Relationship history | Existing and previous relationships affect subsequent interactions and opportunities. |
| ROM-22 | Consequences | Honesty, loyalty, betrayal, exclusivity and consensual arrangements have consequences; NPC preferences matter. |
| ROM-23 | After commitment | Relationships continue developing after marriage or commitment. |
| ROM-24 | Independent lives | Partners maintain their own schedules, hobbies, friends and responsibilities. |
| ROM-25 | NPC memories | Important NPCs remember significant relationship experiences and personal histories. |
| ROM-26 | Survival interplay | Shared dangers, rescues, cooperation and support influence bonds naturally. |
| ROM-27 | Evolution | Friendships may become romantic; relationships can strengthen, weaken, end, reconcile or remain platonic. |
| ROM-28 | Optional romance | Remaining single, friendship, best friends and independent survival are fully valid paths with complete story access. |

### 24.1 — Companion communication progression

CONFIRMED DIRECTION: Before equipment is available, player and companion communicate in person. Discoverable two-way radios permit direct communication within realistic equipment-, terrain- and antenna-dependent ranges. HF radio may enable long-distance communication under suitable conditions; compatible repeaters may extend coverage. After restoration of P.A.N.D.A. infrastructure and discovery of a functioning companion tablet, tablet messaging becomes possible subject to power and signal availability. Detailed radio models, ranges, crafting and messaging are pending design.

### 24.2 — Implementation principles

Build progressively on NPC schedules, autonomy, memory, dialogue, journal privacy and communications. Research relationship psychology, communication and varied lived experiences without treating one model as universal. Companions contribute skills independent of romance; family and platonic bonds are equally meaningful. CONFIRMED denotes approved design, not implemented functionality.

### 24.3 — Change record

v0.5 / 03 Nov 2026 — Retained v0.4 content and appended confirmed ROM-01–ROM-28 relationship design, optional romance, companion communication progression and implementation notes. Previous open/proposed items elsewhere in the Bible remain unchanged.

---

## 25 — Universal Virtual Intelligence, personality and voice systems
**STATUS: CONFIRMED DESIGN DIRECTION; IMPLEMENTATION PLANNED / UNVERIFIED**

### 25.1 — Universal Virtual Intelligence (VI) framework
**CONFIRMED DESIGN.** A modular, offline-first VI architecture provides shared interfaces for perception, memory, subjective knowledge, emotion, skills, learning and decision-making for the player, companions, other humans and animals. Individuals retain distinct abilities and species-specific behaviors; animal cognition does not imply human speech. Godot remains authoritative for physics, movement, animation and world state. Implement player-first and scale simulation detail for distant entities without losing essential persistence or events.

### 25.2 — Individual skills, experience and fallible cognition
**CONFIRMED DESIGN.** Skills are individual, not occupational stereotypes. Related abilities may influence each other, but proficiency in one never guarantees another. Prior experiences inform initial familiarity; aptitude, proficiency and acquired knowledge are distinct. Unfamiliar tools may be handled poorly or dangerously. Characters learn through observation, experimentation, instruction, practice, mistakes and revision. Because the character is software does not mean its simulated cognition is perfect: reasoning, arithmetic, recall, attention, confidence and beliefs can be bounded and fallible. Preserve §20 discovery stages and confidence distinctions.

### 25.3 — Internal monologue
**CONFIRMED DESIGN; PRESENTATION OPEN.** Contextual internal thoughts should be frequent but subtle, reflecting perception, uncertainty, memories, personality and emotion. Avoid repetitive commentary and protect player attention. Private thoughts are not automatically spoken aloud. Text, voiced thought and accessibility controls remain open design choices.

### 25.4 — Player Personality Profiler
**CONFIRMED DESIGN; ALGORITHMS OPEN.** The player character should gradually mirror tendencies inferred from actual gameplay inputs rather than rely on a fixed personality preset. Personality typologies may inform dimensions but must not be treated as diagnostic psychological truth. The profile is tentative, evolving and individual. Use it to shape internal thoughts, conversational style, emotional reactions, mannerisms and minor behavior. Prefer local processing and provide meaningful opt-out, adjustment and reset controls; exact UI and retention remain open.

### 25.5 — Limited autonomy and player authority
**CONFIRMED DESIGN.** Personality-driven VI may initiate minor, low-risk actions such as looking toward an interesting object, greeting a familiar NPC or choosing a resting posture. Direct player control overrides immediately. The VI must not independently initiate serious danger, make consequential story choices, consume significant resources, alter relationships or override player travel intent. Companion and NPC agency remain their own and must respect journal privacy (§19) and existing orders (§6).

### 25.6 — Voice Intelligence Module (VIM)
**CONFIRMED DEVELOPMENT DIRECTION.** Separate communication intent from speech realization. VI supplies intent, context, emotion and speaker identity; VIM produces language, delivery mode (speech, whisper, mutter, private thought), prosody and instructions for synthesis. Human speech and animal vocalization may use different pathways. Coordinate with audio playback and future facial animation/lip synchronization. Avoid prerecorded dialogue as the primary speech solution.

### 25.7 — P.A.N.D.A. Speech Engine (PSE)
**CONFIRMED DEVELOPMENT DIRECTION; FEASIBILITY UNVERIFIED.** Develop a reusable offline-first runtime synthesis platform, independent of any single TTS backend. Its modular interfaces cover text normalization, pronunciation, voice selection, prosody, inference, scheduling, caching, playback and interruption. Newly composed dialogue must be synthesized rather than selected from a prerecorded dialogue library. Target Windows first, Android later, with actual latency, memory, model size, CPU, battery and voice-quality measurements before declaring support.

### 25.8 — Open-source-first strategy and budget
**CONFIRMED STRATEGY; COMPONENT SELECTION OPEN.** Evaluate free and open-source tools, inference runtimes, models and scientific methods to accelerate development, subject to licenses and distribution obligations. Build and maintain the integrated PSE architecture ourselves; original neural models and training algorithms are optional long-term research, not a prerequisite. Use the existing HP and PandaServ computers initially; no new workstation purchase is required to begin prototyping. Candidate TTS models and runtimes are benchmarks, not approved dependencies. Training recordings are distinct from prerecorded in-game dialogue. Any voice contributor must provide informed consent, documented usage rights and appropriate credit.

### 25.9 — Performance, privacy and accessibility gates
**PLANNED / OPEN DETAILS.** Verify nonblocking synthesis, interruption/cancellation, safe multi-speaker scheduling, persistence, graceful quality reduction, low-end CPU behavior and future Android export. Personality profiling should remain local and user-controllable. Speech and internal-monologue presentation require accessibility options. License audit must cover code, weights, datasets and voices.

### 25.10 — Proposed implementation milestones
1. VI data structures, individual memory and save/load; validate player authority.
2. Granular skills, fallible knowledge and experiential learning integrated with §20.
3. Personality profiling with opt-out, adjustment and reset.
4. VIM intent-to-utterance contract independent of synthesis backend.
5. Offline TTS benchmark on existing hardware; record CPU, RAM, latency, quality and license conditions.
6. Godot background speech generation, playback, interruption and voice identities.
7. Future Android validation, expressive voices and optional custom-model research.

## 26 — v0.8 decision register additions
**Note:** These new IDs extend existing v0.7 D001–D013; inherited records are unchanged. All decisions below are design confirmations, not evidence of implementation.

- **D014 — CONFIRMED DESIGN:** Universal VI architecture with player-first implementation and species-specific behavior.
- **D015 — CONFIRMED DESIGN:** Independent granular skills, experiential learning and bounded, fallible cognition.
- **D016 — CONFIRMED DESIGN:** Frequent, subtle contextual internal monologue; delivery method open.
- **D017 — CONFIRMED DESIGN:** Evolving gameplay-based personality profiler, non-diagnostic, local and user-controllable.
- **D018 — CONFIRMED DESIGN:** Limited low-risk autonomous player actions; direct player control always takes priority.
- **D019 — CONFIRMED DIRECTION:** Separate Voice Intelligence Module; dynamically generated dialogue rather than prerecorded lines.
- **D020 — CONFIRMED DIRECTION:** Modular offline P.A.N.D.A. Speech Engine with Windows-first and future Android target.
- **D021 — CONFIRMED STRATEGY:** Open-source-first evaluation, license review, and no mandatory new workstation purchase.

## 27 — v0.8 open questions
- **Q-VI-01:** What are the VI memory, forgetting, belief-confidence and reasoning representations?
- **Q-VI-02:** How are skill transfer, practice, mistakes and instruction quantified?
- **Q-VI-03:** What trait dimensions, observation windows and reset/privacy controls govern personality profiling?
- **Q-VI-04:** How are minor autonomous actions gated, interrupted and disabled?
- **Q-VOICE-01:** Is internal monologue displayed, voiced or configurable?
- **Q-VOICE-02:** Which offline synthesis backend meets measured Windows/Android performance and licensing requirements?
- **Q-VOICE-03:** What standards govern voice-contributor consent, credit, data protection and derivative synthetic voices?
- **Q-VOICE-04:** How will emotional prosody, multiple simultaneous speakers and lip-sync be validated?

## 28 — v0.8 change record
**05 November 2026:** Preserved complete v0.7 text from repository reference extraction; appended §§25–28 for Universal VI, personality mirroring, cognition, dynamic speech, open-source PSE strategy, decision IDs D014–D021, research questions and staged development. No v0.7 original decision is superseded solely by this update. Technical feasibility remains unverified.


## 29 — DEVCONTROL reconciliation and implementation evidence (06 November 2026)

**STATUS: TRACKING ADDENDUM — not a new design approval or a catalogue publication.** This section reconciles the v0.8 candidate against DEVCONTROL conversation decisions and reported milestone evidence as of 06 November 2026. It does not replace canonical v0.7, change existing decision IDs, or assert that untested game systems work.

### 29.1 — Design consistency and scope

- **Windows-first:** PROJECT P.A.N.D.A.: REBIRTH is the Windows PC game. Android remains a possible later game platform, not the current REBIRTH deliverable. The separate P.A.N.D.A. Developer Companion is an Android application, not the REBIRTH game.
- **Granular abilities:** Retain the exact principle: “Skills are individual, not occupational stereotypes. Related abilities may influence one another, but competence in one area never guarantees competence in another.” Prior experience, aptitude, acquired knowledge and demonstrated proficiency must remain separate.
- **Bounded cognition:** “The simulation knows everything. The character doesn't.” A software-simulated character does not gain perfect arithmetic, memory, knowledge or reasoning merely because the simulation runs on a computer. Characters can be uncertain, make mistakes, revise beliefs and learn from experience.
- **Agency and authority:** Minor character-driven behavior never overrides direct player control or authorizes consequential decisions. Individual NPC and companion memories, privacy and autonomy remain distinct.
- **VI / VIM / PSE:** §§25–28 are approved design directions, not completed, benchmarked or integrated runtime features. Do not conflate an architectural proposal with an implemented system.
- **DEVCONTROL terminology:** PUSH means backup of verified source/development changes to authorized private GitHub repositories; PUBLISH means distributing user-facing updates via established public game/app update repositories. Private tester prereleases are neither a public PUBLISH nor evidence that installed clients receive an update. AUTONOMOUS means execute, repair routine errors and validate; it does not grant PUSH/PUBLISH permission.

### 29.2 — Reported development and distribution milestones

| Area | Evidence available in DEVCONTROL conversation | Status and limitation |
| --- | --- | --- |
| REBIRTH Windows v0.1.5 | Private prerelease tag `tester-v0.1.5-devcontrol-002` in `Big-C8701/PROJECT-PANDA`; ZIP asset SHA-256 `4c394035b5c62c58eea2f6ae070cec8d7be7687ad62448ce5a0acc3e9df997a1`. Private repository, prerelease and attached asset independently checked through connected GitHub. | **TESTER PACKAGE PUBLISHED PRIVATELY**; graphical Windows gameplay acceptance remains pending. This is not a public update-channel publication. |
| REBIRTH public update channel | `Big-C8701/PROJECT-PANDA-Releases` has a public v0.1.5 release with executable/setup assets, independently observed through GitHub. | **EXISTING PUBLIC RELEASE VERIFIED**; binary equivalence with the private tester ZIP and live in-game updater compatibility **NOT VERIFIED**. |
| Developer Companion Android v0.7.2 | Private prerelease tag `tester-v0.7.2-devcontrol-002` in `Big-C8701/PROJECT-PANDA-DEV-COMPANION`; APK SHA-256 `446bb020b165a8daa6e4cdf86d92cd0f295af97b587756cbd7f590d8f55a5cc5`. | **TESTER PACKAGE PUBLISHED PRIVATELY**; physical-device install and Bible v0.8 catalogue compatibility unverified. APK uses a newly generated debug signing key; in-place update from differently signed builds is incompatible. |
| Companion public update channel | `Big-C8701/PROJECT-PANDA-DEV-COMPANION-UPDATES` publicly listed v0.7.1 as latest when checked in DEVCONTROL. | **PUBLIC v0.7.2 NOT PUBLISHED** at time of check; do not claim users can update to the private tester build in-app. |
| Bible v0.8 | `canonical/PROJECT_PANDA_REBIRTH_Game_Design_Bible_v0.8.md` is committed as a Markdown canonical **candidate**. `canonical/manifest.json` and `references/current.json` still point to v0.7; no validated v0.8 feed. | **DESIGN CANDIDATE EXISTS; CATALOGUE / COMPANION SYNC BLOCKED**. Do not advance discovery manifests without validated catalogue and compatible Companion client. |
| Game runtime systems | v0.7 inherited text includes older static-audit `IMPLEMENTED*` observations (survival, construction, world, controller). | **HISTORICAL CODE OBSERVATIONS ONLY**. This addendum does not upgrade those to verified current runtime acceptance. |

### 29.3 — Remaining verification and acceptance gates

1. Perform and document REBIRTH Windows graphical gameplay, save/load, controls and performance tests on the target machine.
2. Perform Developer Companion physical Android installation/launch tests, with explicit handling of signing-key mismatch and potential data loss on uninstall.
3. Preserve original v0.7 DOCX and all prior catalogues; validate a v0.8 Markdown-authoritative extraction pipeline, stable IDs, source provenance and hashes before any discovery-feed promotion.
4. Confirm Companion's actual supported catalogue version and safe fallback behavior before enabling v0.8 synchronization or publishing an app update.
5. Keep design-confirmed VI, personality, internal-monologue, VIM and PSE systems **PLANNED / UNVERIFIED** until their individual code, integration, performance, licensing and user-control acceptance criteria pass.
6. Keep PROJECT FISH, PROJECT R100 and other DEVCONTROL projects in the portfolio tracker, not in the REBIRTH canonical game feature list.

### 29.4 — Provenance and change discipline

The DEVCONTROL reports are supplied execution summaries; unless explicitly identified above as checked through GitHub, their detailed tests have not been independently replayed in this Bible repository. This addendum is documentation reconciliation, not an authorization to publish software, replace the DOCX, advance the live reference catalogue or alter unrelated project repositories. Existing CONFIRMED, PROPOSED and OPEN design decisions remain unchanged.


---

## 30 — P.A.N.D.A. CORE: unified engine design

STATUS: CONFIRMED VISION; IMPLEMENTATION STATUS: NOT VERIFIED

PROJECT P.A.N.D.A. has **one Master Design Bible**. CORE is the reusable game creation and runtime platform; REBIRTH is its first game/showcase. CORE and REBIRTH are sections of this document, never separately authoritative Bibles. Historical editions remain preserved for provenance.

### 30.1 — Foundational purpose

STATUS: CONFIRMED VISION

CORE is intended to become a reusable, intelligence-driven game engine/platform, analogous in purpose to Unreal Engine, with conversational game creation, procedural worlds/textures/materials/assets, modular simulation and cognition, code generation and testing, and manual creator control. Godot may initially provide rendering and runtime facilities; the long-term platform must not be conceptually restricted to a single game.

### 30.2 — Creator experience

STATUS: CONFIRMED VISION; IMPLEMENTATION PLANNED

A creator can describe a game conversationally. CORE interprets the request and can propose or generate an initial project structure, world, mechanics, assets and systems. Generated content remains inspectable, editable and overrideable through manual tools. Generated results require validation and creator control.

### 30.3 — Module boundaries

STATUS: CONFIRMED PRINCIPLE; INTERFACES PROPOSED

Keep independent modules for orchestration/intelligence, procedural world generation, materials/assets, character cognition, world simulation, game mechanics, project generation/testing, persistence and engine adapters. Use versioned interfaces and explicit dependencies; the exact APIs and data formats remain OPEN.

### 30.4 — Character intelligence and bounded cognition

STATUS: CONFIRMED DESIGN PRINCIPLE

Simulated characters must not become omniscient or mathematically perfect merely because they are implemented in software. Model fallible memory, limited knowledge, uncertainty, mistakes, learning and individual aptitudes. **Skills are individual, not occupational stereotypes. Related abilities may influence one another, but competence in one area never guarantees competence in another.** Prior experience, aptitude and acquired skill must be modeled separately.

### 30.5 — Runtime versus development control

STATUS: CONFIRMED ARCHITECTURAL BOUNDARY

DEVCONTROL coordinates development work (coding, builds, tests and project progress). CORE provides reusable game-creation and runtime functionality. PandaServ hosts development infrastructure. REBIRTH consumes CORE capabilities. Development-only modules and privileged controls must not be exposed to players as runtime abilities.

### 30.6 — Initial technical strategy

STATUS: CONFIRMED DIRECTION; IMPLEMENTATION NOT VERIFIED

Use Godot as the initial rendering/runtime substrate where practical. Favor incremental extraction and reusable adapters over risky rewrites of REBIRTH. Support Windows initially and investigate Android separately with performance profiling. Engine independence is a long-term design goal, not an assertion of existing portability.

### 30.7 — Architecture sketch

STATUS: PROPOSED STRUCTURE

Creator interface (conversation + visual/manual editing) → CORE orchestration/planning/validation → modular generation, cognition, simulation and gameplay services → engine adapter/runtime (initially Godot) → independently configured games including REBIRTH. Persistent data and testing/observability are cross-cutting services. Module ownership, protocols and deployment topology remain OPEN.

### 30.8 — Phased development roadmap

STATUS: PROPOSED; NO COMPLETION CLAIMS

C01: Define module contracts, persistence formats, ownership and Godot adapter.

C02: Prototype reusable world/material/asset generation.

C03: Prototype bounded character cognition and simulation.

C04: Build an editable conversational creator workflow.

C05: Integrate repeatable generation, tests and validation with development tooling.

C06: Validate reuse across REBIRTH and a structurally different game.

### 30.9 — Outstanding architecture decisions

STATUS: OPEN

Choose module APIs, data schemas, simulation scheduling, AI model strategy and offline behavior, procedural asset pipelines, runtime performance budgets, security boundaries, project export model, engine-adapter scope, and measurable milestones. No unverified implementation or benchmark is certified by this section.

### 30.10 — Unified Bible governance

STATUS: CONFIRMED

One repository, one Master Design Bible, one unified version sequence and one authoritative candidate at a time. CORE and REBIRTH are sections of the same master. Preserve existing permanent IDs and historical decisions. Do not confuse design approval with implementation status. Previous editions remain immutable archives; Companion catalogue publication is a separate validated release step.

## 31 — Unified consolidation record

19 November 2026: Consolidated the full v0.8 REBIRTH candidate body into a single PROJECT P.A.N.D.A. Master Design Bible, appended CORE architecture and governance without deleting inherited sections. All inherited numbered sections and source wording below the replaced cover are preserved from v0.8. This v0.9 file is a **design candidate**, not an activated Companion catalogue or proof of implemented CORE features. Active discovery manifests remain on v0.7 pending validation and client compatibility.
