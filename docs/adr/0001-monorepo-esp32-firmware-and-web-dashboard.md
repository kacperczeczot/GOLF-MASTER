[Strona główna](../../README.md) > [Dokumentacja](../README.md) > [ADR](README.md) > [ADR 0001](0001-monorepo-esp32-firmware-and-web-dashboard.md)

---

# ADR 0001: Architektura Monorepo: Firmware ESP32 + Web Telemetry Dashboard

* **Status:** Zaakceptowany
* **Data:** 2026-06-01
* **Autorzy:** Kacper Czeczot

---

## Kontekst
Diagnostyka pokładowa i monitoring parametrów pojazdu Volkswagen Golf Plus (magistrala CAN, wskaźniki ciśnienia doładowania, temperatury DPF/oleju/płynu, statystyki spalania) wymagały odrębnego firmware sprzętowego mikrokontrolera ESP32 oraz lekkiego, w 100% offline'owego panelu webowego do wizualizacji na żywo i analizy logów.

## Decyzja
1. **Model Monorepo (`apps/`):**
   - `apps/firmware/` — oprogramowanie wbudowane C++/Arduino dla ESP32 (MCP2515 CAN transceiver, BLE UART, protokół binarny).
   - `apps/web/` — panel webowy (Vanilla HTML5 / CSS3 / ES Modules) z offline'owym bundlerem `bundle_tool.py` i obsługą Web Bluetooth API.
2. **Centralny rejestr danych w `data/`:**
   - `data/` — specyfikacja parametrów PID pojazdu.
   - `data/logs/` i `data/archiwum/` — rejestry telemetrii i kodów błędów DTC.
3. **Skrypty w `scripts/`:**
   - Skrypty szybkiego uruchamiania `scripts/start.command` i `scripts/start.bat`.

## Konsekwencje
### Pozytywne:
- Czysta separacja kodu mikrokontrolera od panelu frontendowego.
- Zgodność z Kanonem Root Monorepo DevEx.
