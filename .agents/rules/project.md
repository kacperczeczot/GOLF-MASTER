---
name: Reguły Domenowe GOLF-MASTER
description: Standardy diagnostyki CAN-bus, komunikacji BLE UART i architektury Monorepo.
---

# Reguły Domenowe: GOLF-MASTER

Projekt stanowi system telemetryczny pojazdu Volkswagen Golf Plus.

---

## 1. Architektura Monorepo
- **`apps/firmware/`**: Oprogramowanie ESP32 C++/Arduino. Zmiany w protokole BLE lub ramkach CAN muszą być odzwierciedlone w `docs/MESSAGES.md`.
- **`apps/web/`**: Panel telemetryczny ES Modules. Każda zmiana w kodzie JS wymaga walidacji bundlera:
  ```bash
  python3 apps/web/bundle_tool.py check
  python3 apps/web/check_signal_meta_state_tags.py
  ```
- **`data/`**: Zrzuty telemetrii, logi i bazy PID-ów.

---

## 2. Standardy DevEx
Projekt bezwzględnie przestrzega reguł Monorepo zdefiniowanych w:
👉 **[devex-standards](https://github.com/kacperczeczot/devex-standards)**
