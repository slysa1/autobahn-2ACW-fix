# Tasks

## In Progress

- [ ] Phase 1: Create KR Harmony Debug launcher playset (clone current KR playset, do not edit it in place)
- [ ] Phase 2A: Verify 2ACW fix is obsolete — remove from debug playset and re-test natural USA 2ACW

## To Do

### Phase 1 — Minimal Baseline

- [ ] Disable non-core mods from debug playset: Autobahn KR 2ACW Fix, Expanded Tank Designer, BM Supply Production Health, BM AI Divisions, BM AI Designs, BM Extended Projects, BM Namelists
- [ ] Run clean baseline boot + 7-14 day smoke test (research, tech tree, aircraft designer, navy UI)
- [ ] Archive baseline logs and compare against noisy current baseline

### Phase 2A — Retire/Update Local Patches

- [ ] Update KNR KR Runtime Fix descriptor: bump `supported_version` to `1.18.*`
- [ ] Reconfirm KNR runtime fix content still matches live breakpoints

### Phase 2B — Rebuild Autobahn<->KNR Compatch

- [ ] Diff x_plane_airframes.txt across current KR, Autobahn, KNR and rebuild valid merged version
- [ ] Diff countrytechtreeview.gui across current KR, Autobahn, KNR and rebuild valid merged version
- [ ] Check whether nuclear_projects.txt still needs an override (remove if it is just a stale KR copy)
- [ ] Package rebuilt compatch as clean local replacement

### Phase 2C — KNR Core Repairs

- [ ] Confirm has_navy_size scope fix still covers all 6 naval traits in live KNR trait file
- [ ] Update KNR runtime fix to current file layout (0.2.0 bump)
- [ ] Audit KR naval project definitions suppressed by KNR; restore missing ones

### Phase 2D — Autobahn Core Repairs

- [ ] Remove/guard invalid idea checks in plane_airframes.txt (BUL_army_restrictions, MPL_mandate, GER treaty ideas)
- [ ] Audit special_forces_doctrine.txt for invalid category references (ranger, aircraft category drift)
- [ ] Fix BOM on interface/r56_equip_air.gfx (UTF-8 BOM causing ﻿SpriteTypes parse error)
- [ ] Audit 00_plane_icons.txt and other graphics database files for invalid scope/tag spam

### Phase 3 — Secondary Mod Reintegration (BLOCKED on Phase 2)

- [ ] Batch 1: Cosmetic/audio mods (ship models, music packs)
- [ ] Batch 2: KR-side gameplay extensions (Project Gorgeous etc.)
- [ ] Batch 3: Low-surface Better Mechanics QoL modules
- [ ] Batch 4: High-risk Better Mechanics modules (SPH, AI Divisions, AI Designs, Extended Projects, Namelists)
- [ ] Batch 5: Expanded Tank Designer standalone decision

### Phase 4 — Final Stabilization

- [ ] Consolidate local patches; retire stale shims
- [ ] Update all descriptor metadata for surviving patches
- [ ] Document final stable load order
- [ ] Prepare upstream reports (KNR author, Autobahn author, compatch author, BM authors)

### Phase 5 — Validation

- [ ] Load validation (menu, new game, save/reload)
- [ ] UI validation (research, tech tree, aircraft/tank designer, navy UI, officer corps, special projects)
- [ ] 30-day observe run — no catastrophic log explosion
- [ ] USA 2ACW validation (natural start, no stall, no DMZ hang)
- [ ] Naval edge-case: USA pre-war split with KNR, admiral/task-force, no crash
- [ ] Designer/equipment: no invalid module setup spam

## Done

- [x] Identify winning file owners for all major error families
- [x] Confirm 2ACW fix is likely obsolete (Autobahn no longer carries old ACW scripted-effects override)
- [x] Confirm KNR runtime fix still targets real live seams (has_navy_size, armoured cruiser equipment/project)
- [x] Audit Autobahn<->KNR compatch — confirmed stale (x_plane_airframes.txt, countrytechtreeview.gui, nuclear_projects.txt)
- [x] Confirm has_navy_size in character scope (6 naval traits in KNR)
- [x] Record all mod error families and ownership in diagnostics/
- [x] Write ai_project_briefing.txt and kr_playset_recovery_roadmap.txt
