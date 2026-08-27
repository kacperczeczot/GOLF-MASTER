[Strona główna](../README.md) > [Dokumentacja](README.md)

---

# Dokumentacja Techniczna Systemu GOLF-MASTER

Centralny katalog dokumentacji inżynieryjnej, specyfikacji protokołów CAN-bus/OBD2 oraz rejestru decyzji architektonicznych.

---

## 1. Moduły Dokumentacji

| Dokument / Sekcja | Status | Opis |
| :--- | :--- | :--- |
| [Standardy Inżynieryjne (`docs/STANDARDS.md`)](STANDARDS.md) | 🔴 `[WYMAGANY]` | Certyfikat zgodności Monorepo ze standardami DevEx |
| [Specyfikacja Komunikatów (`docs/MESSAGES.md`)](MESSAGES.md) | 🔴 `[WYMAGANY]` | Format ramek BLE, protokoły telemetrii i komendy OTA |
| [Rejestr Decyzji ADR (`docs/adr/`)](adr/README.md) | 🔴 `[WYMAGANY]` | Rejestr Decyzji Architektonicznych systemu |

---

## 2. Aplikacje Monorepo (`apps/`)
* ⚡ [**`apps/firmware/`**](../apps/firmware/README.md) — Firmware mikrokontrolera ESP32 (C++/Arduino) do odczytu CAN-bus.
* 📊 [**`apps/web/`**](../apps/web/README.md) — Offline Web Dashboard analityki i wizualizacji telemetrii.

---

## 3. Zbiory Danych i Logi (`data/`)
* 📁 [**`data/`**](../data/) — Parametry pojazdu, specyfikacje PID-ów, logi diagnostyczne (`data/logs/`) i archiwum (`data/archiwum/`).
