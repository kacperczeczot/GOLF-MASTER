# GOLF-MASTER — System Diagnostyki Pokładowej & Analityki Telemetrii

> Monorepo systemu diagnostyczno-telemetrycznego dla pojazdu Volkswagen Golf Plus: firmware ESP32 CAN-bus + offline Web Dashboard analityki pojazdu.

---

## 1. Dokumentacja i Standardy Monorepo


| Dokument / Sekcja | Opis |
| :--- | :--- |
| [Standardy Projektu (`docs/STANDARDS.md`)](docs/STANDARDS.md) | Certyfikat zgodności Monorepo ze standardami DevEx |
| [Specyfikacja Komunikatów (`docs/MESSAGES.md`)](docs/MESSAGES.md) | Formaty ramek danych BLE, protokoły telemetrii |
| [Baza Dokumentacji (`docs/README.md`)](docs/README.md) | Centralny hub dokumentacyjny projektu |
| [Rejestr Decyzji ADR (`docs/adr/`)](docs/adr/README.md) | Rejestr Decyzji Architektonicznych |
| [Reguły AI Projektu (`.agents/rules/project.md`)](.agents/rules/project.md) | Instrukcje domenowe dla asystentów AI |

---

## 2. Aplikacje Monorepo (`apps/`)

| Aplikacja | Ścieżka | Technologia | Opis |
| :--- | :--- | :--- | :--- |
| **Firmware ESP32** | [`apps/firmware/`](apps/firmware/) | C++ / Arduino | Oprogramowanie mikrokontrolera do odczytu magistrali CAN (OBD2) i transmisji BLE |
| **Web Dashboard** | [`apps/web/`](apps/web/) | Vanilla HTML / CSS / JS | Offline'owy panel analityczny na żywo i przeglądarka logów telemetrii |

---

## 3. Zbiory Danych i Skrypty

* 📁 [**`data/`**](data/) — Parametry pojazdu, specyfikacje PID oraz logi diagnostyczne (`data/logs/`).
* 📁 [**`scripts/`**](scripts/) — Skrypty uruchomieniowe (`scripts/start.command`, `scripts/start.bat`) oraz aktualizacji OTA.

---

## 4. Szybki Start

```bash
# Uruchomienie lokalnego panelu telemetrycznego
./scripts/start.command

# Weryfikacja spójności bundla webowego
python3 apps/web/bundle_tool.py check
```
