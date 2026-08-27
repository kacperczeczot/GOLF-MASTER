# Dziennik Zmian (Changelog)

Wszystkie istotne zmiany w projekcie są dokumentowane w tym pliku zgodnie ze standardem [Keep a Changelog](https://keepachangelog.com/pl/1.1.0/) oraz [Semantic Versioning](https://semver.org/lang/pl/).

---

## [0.1.2] - 2026-08-27

### Changed
- migrate repository layout to DevEx Monorepo architecture

### Miscellaneous
- remove redundant root MESSAGES.md and cleanup empty archiwum
- preserve historical prototypes and bridge scripts in data/archive
- remove self-referencing breadcrumb from root README.md
- fix all remaining broken relative links
- adapt README.md to project specific context, remove boilerplate
- align PR templates with .agents/rules standard and specific repo context
- enforce DevEx canonical breadcrumbs in all markdown files

---

## [0.1.1] - 2026-06-17

### Miscellaneous
- Add ESP32 wireless firmware alongside Arduino reference sketch.
- Migrate UI transport to BLE UART and archive legacy bridge stack.
- Fix startup reliability and restore active mobile BLE UI runtime.
- Add CAN idle shutdown timers and TWAI recovery; fix mobile modal headers.
- Implement roadmap P0–P3 for ESP32 reliability and web diagnostics.
- Fix false CAN HANG during sleep and simplify diagnostics UI.
- Fix garbled BLE CAN lines by correcting UART reassembly.
- Add PQ35 CAN snapshot and terminal logs from 2026-06-17 session.
- Send each CAN log line atomically over BLE UART.
- Add BLE transport validation logs from 2026-06-17 session.

---

## [0.1.0] - 2026-04-28

### Added
- align Python simulator flow with bridge logic
- add offline-first launch flow with simulation choice
- live-update modal when CAN frame data changes
- błysk kafelków przy ramkach CAN i symulacja z osi czasu

### Changed
- optimize CAN RX and clean up NM logic constants
- reorganize web modules and fix UI runtime errors
- centralize frame registry and relocate offline bundle
- replace inline decoder styles with CSS classes
- simplify and darken UI color palette
- unify frame color semantics across decoders
- keep frame card order stable by ID
- centralize frame border status styling in CSS
- consolidate header action button styles
- modular JS layout, modal value colors, offline bundle
- rename CAN reference txt files to snake_case

### Fixed
- fixed SCAN DTC
- fixed* SCAN DTC
- fixed** DTC
- fixed**** DTC + log fix
- Zmiana logiki usypiania OSEK na detekcję bitu 0x80 w Bajcie 2. Naprawiono błąd HANG przy spamowaniu przycisku pilota.
- Faza_4_Hybryda — logika OSEK jak hardware.ino (bit 0x80 w Bajcie 2)
- final zero-one NM logic based on gateway wake causes
- default state assumes sleeping bus for hang watchdog
- make cantools import resilient in frame info script
- remove stray brace causing decoder syntax error
- Safari/Chrome bundle load (innerHTML descriptor, comment header)
- clamp CAN DLC and normalize RX id

### Miscellaneous
- Add initial HTML structure for GOLF MASTER UI
- Add styles for GOLF MASTER v50.0
- Add CAN communication setup and error handling
- Implement WebSocket server to handle Arduino data
- Add initial implementation of WebSocket client
- Create txt.txt
- Delete web/data directory
- Create data
- Add files via upload
- Delete data/data
- Rename PQ35_46_ICAN_V3_6_9_F_20081104_ASR_V1_2 (1).dbc to PQ35_46_ICAN_V3_6_9_F_20081104_ASR_V1_2.dbc
- Add initial README for GOLF PLUS ULTIMATE project
- Poprawa komunikacji między plikami
- Update hardware.ino
- Pogrupowanie ramek CAN
- Zebranie dokładnych informacji o ramkach CAN
- Przygotowanie logiki JS pod info z ramek
- Rozkodowane 4 ramki CAN
- Rozszyfrowanie wszystkich otrzymanych ramek
- uzupełnienie stylów css
- Poprawa JS i CSS
- poprawa CSS i JS
- uzupełnienie metadanych JS
- dodana funkcja SNAPSHOT
- dodano SCAN DTC
- Revert "dodano SCAN DTC"
- naprawa C++
- add SCAN DTC
- Nowe ramki CAN
- //github.com/Negatywistczny/GOLF-MASTER
- hardware communication fix
- ADD log download
- dodano info o ID wg adresów
- dodano info o ramkach radia
- dodano programy testowe arduino
- ! KOMUNIKACJA CAN DZIAŁA !
- optymalizacja hardware.ino
- dodano MESSAGES.md
- dodano README
- zaktualizowano START.BAT
- zaktualizowano START.BAT
- zaktualizowano START.BAT
- zaktualizowano README
- Rename web_ui folder to web in documentation
- Rename MESSAGES.MD to MESSAGES.md
- Rename README.MD to README.md
- Update hardware.ino
- Stabilize async scan timing and client cleanup.
- Harden bridge clarity and websocket lifecycle.
- Refine web UI semantics and CSS maintainability.
- //github.com/Negatywistczny/GOLF-MASTER
- Modularize web frontend into ES6 architecture and optimize runtime updates.
- remove inline citation markers from state metadata
- ignore local Python environment artifacts
- ignore macOS Finder metadata files
- dekodery w js/can, bundle_tool i workflow CI; bridge: requirements.txt; dokumentacja i bundle zsynchronizowany
- added logs
- Add PQ35 snapshot diff table (UTF-8 with BOM)
- ramka 0x531 (mLicht_1_alt), meta i symulator
- NM z latch Alive, log 0x42B; Faza 4: Ring nie zeruje okna
- NM zgodne z firmware (0x80, Ring), SYS:CAN:WAKE_* w MESSAGES
- stateTags w signalMeta, checker CI, kolory modala, porządki
- unify CAN bus active/passive state and tighten passive-exit detection.
- inline passive-state whitelist check.
- remove heuristic wake path and simplify NM state flow.
- add PQ35 CAN and OSEK NM research notes.
- v02 NetState firmware, validation docs, archived v01 and field logs
- v03 firmware (KEEPALIVE/SLEEP_COOP), logi polowe i wnioski ostateczne
- v4.1 sleep-gate results and anti-regression rules
- enforce event-driven NM watchdog rules.
- add v5 recovery firmware and Test A log.
- add NM state catalog and Gemini brief.
- refresh README to current NM behavior.
- replace Gemini brief with final NM report.
- implement post-report NM execution baseline.
- finalize v10 Arduino firmware baseline.
- finalize v10 structural refactor baseline.
- close NM communication loop for final firmware.
- extend terminal log retention and fix local timestamps.
- unify message registry with activity aging and TTL states.
- render all error rows in red.
- unify error row styling under msg-row-error.
- align sentinel decoding and retire validator script.
- make alternator warning context-aware.
- implement full PQ35 scan communication stack.
- stabilize partial-frame summaries across tile, modal, and snapshot.
- cichszy skan, kanał TX, eksport logu i przyciski w sekcji wyników
- Organize DTC regression under bridge/DTC with per-test templates
- Update DTC local test, NM validation logs, add PQ35 DTC diagnostic capture
- KD557 module filter, scan pacing, no_data/no_dtc status, UI details
- Remove DTC stack from bridge, web UI, and docs.
- Archive the latest PQ35 terminal capture and remove obsolete hardware phase test fixtures.
- Add 2026-04-17 sleep (uspienie) capture log and Arduino sketch snapshot.
- Refine NM sleep/watchdog handling and archive sleepfix2 snapshot.
- Archive latest PQ35 CAN snapshot and terminal capture.
- Archive today's hardware sketch snapshot and align CAN bridge throughput defaults.
- Archive today's PQ35 terminal test logs.
- Refine 0x359 tile to show only useful, reliable signals.
- Archive today's PQ35 terminal logs.
- Add relay control outputs with CAN signal mapping.

---
