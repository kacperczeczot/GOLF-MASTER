[Strona główna](../README.md) > [Dokumentacja](README.md) > [Standardy](STANDARDS.md)

---

# Standardy Inżynieryjne Projektu: GOLF-MASTER

Projekt funkcjonuje w oparciu o model architektoniczny **Monorepo** ([`template-monorepo`](https://github.com/kacperczeczot/template-monorepo)) i przestrzega globalnych standardów inżynieryjnych centralnej Konstytucji **[`devex-standards`](https://github.com/kacperczeczot/devex-standards)**.

---

## 1. Zgodność ze Standardami Zewnętrznymi

| Standard | Implementacja w Projekcie | Oficjalna Specyfikacja |
| :--- | :--- | :--- |
| **Conventional Commits** | Commity w języku angielskim (`feat:`, `fix:`, `docs:`, `refactor:`) | [conventionalcommits.org](https://www.conventionalcommits.org/pl/v1.0.0/) |
| **Semantic Versioning** | SemVer (`MAJOR.MINOR.PATCH`) | [semver.org](https://semver.org/lang/pl/) |
| **Keep a Changelog** | [`CHANGELOG.md`](../CHANGELOG.md) wg specyfikacji 1.1.0 | [keepachangelog.com](https://keepachangelog.com/pl/1.1.0/) |
| **ADR** | Rejestr Decyzji w [`docs/adr/`](adr/README.md) | [adr.github.io](https://adr.github.io/) |
| **EditorConfig** | [`.editorconfig`](../.editorconfig) w root dla spójności IDE | [editorconfig.org](https://editorconfig.org/) |

---

## 2. Bramki Jakościowe i Weryfikacja

- **Weryfikacja bundla panelu webowego:**
  ```bash
  python3 apps/web/bundle_tool.py check
  ```
- **Weryfikacja metadanych sygnałów telemetrii:**
  ```bash
  python3 apps/web/check_signal_meta_state_tags.py
  ```

---

## 3. Źródło Prawdy (SSOT)
👉 **[devex-standards / Architecture Rules](https://github.com/kacperczeczot/devex-standards/blob/main/docs/architecture/RULES.md)**
👉 **[devex-standards / Tooling Rules](https://github.com/kacperczeczot/devex-standards/blob/main/docs/tooling/RULES.md)**
