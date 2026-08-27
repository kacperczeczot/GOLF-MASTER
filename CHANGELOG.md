# Dziennik Zmian (Changelog)

Wszystkie istotne zmiany w projekcie są dokumentowane w tym pliku zgodnie ze standardem [Keep a Changelog](https://keepachangelog.com/pl/1.1.0/) oraz [Semantic Versioning](https://semver.org/lang/pl/).

---

## [Unreleased]

### Added
- Dostosowanie repozytorium do standardów DevEx w architekturze Monorepo.
- Struktura `apps/`: `apps/firmware/` (ESP32) oraz `apps/web/` (Web Dashboard).
- Struktura dokumentacji `docs/` z certyfikatem `docs/STANDARDS.md`, `docs/MESSAGES.md` i rejestrem `docs/adr/`.
- Konsolidacja logów w `data/logs/` i `data/archiwum/`.
- Pliki konfiguracyjne: `.editorconfig`, `.agents/rules/project.md`, `.github/pull_request_template.md`.

---

## [1.0.0] - 2026-06-01

### Added
- Firmware ESP32 do odczytu ramek CAN-bus (OBD2) i transmisji danych przez Bluetooth LE UART.
- Responsywny panel webowy HTML/CSS/JS do wizualizacji parametrów na żywo.
- Narzędzie bundlujące `bundle_tool.py`.
