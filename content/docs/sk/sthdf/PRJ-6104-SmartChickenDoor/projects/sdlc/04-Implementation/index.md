---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.125601+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "84ccdba0-2190-4959-bc1d-3928570fb1e1"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "04 Implementation"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Plán realizácie po etapách."


# 👥 AUTHORSHIP ------------------------------------------------------

# Hlavný autor – z globálneho configu
author: "Filip Chromek, Dominik Mojto, Alexander Ovšonka"

# Zoznam autorov – generuje skript
authors:
  - "Filip Chromek, Dominik Mojto, Alexander Ovšonka"


# 🗂 CLASSIFICATION ---------------------------------------------------

# Nadradená kategória – môže doplniť používateľ
category: ""

# Typ dokumentu (guide, case, tutorial...) – používateľ (voliteľné)
type: ""

# Priorita (low/medium/high) – voliteľné
priority: ""

# Tagy – odporúča sa 2–6 tagov.
# Typy tagov:
#   - rámce: knife, 7ds, sdlc, q12
#   - účel: tutorial, guide, pattern, case-study
#   - téma: git, backup, ai, communication
#   - úroveň: beginner, intermediate, advanced
tags: []


# 🌍 LOCALIZATION -----------------------------------------------------

# Jazyk dokumentu – doplní skript podľa štruktúry
locale: "sk"


# 🕒 LIFECYCLE --------------------------------------------------------

# Dátum vytvorenia – generuje skript
created: "2026-11-03 15:48"

# Dátum poslednej úpravy – dopĺňa človek
modified: "2026-11-03 15:48"

# Stav dokumentu – default "backlog"
status: "backlog"

# Viditeľnosť – default "public"
privacy: "public"


# ⚖ INTELLECTUAL PROPERTY -------------------------------------------

# Držiteľ práv k obsahu – dopĺňa skript
rights_holder_content: "Filip Chromek, Dominik Mojto, Alexander Ovšonka"

# Systémový vlastník práv
rights_holder_system: "CAA / KNIFE / LetItGrow"

# Licencia
license: "CC-BY-NC-SA-4.0"

# Disclaimer
disclaimer: "Use at your own risk. Methods provided as-is; participation is voluntary and context-aware."

# Copyright
copyright: "© 2025 Filip Chromek, Dominik Mojto, Alexander Ovšonka"


# 🔗 ORIGIN / PROVENANCE ---------------------------------------------

# Repozitár pôvodu
origin_repo: ""

# URL pôvodného repozitára
origin_repo_url: ""

# Commit pôvodu
origin_commit: ""

# Branch pôvodu
origin_branch: ""

# Systém pôvodu (CAA/KNIFE/STHDF…)
origin_system: "CAA"

# Pôvodný autor
origin_author: "Filip Chromek, Dominik Mojto, Alexander Ovšonka"

# Importovaný zdroj
origin_imported_from: ""

# Dátum importu
origin_import_date: ""


# 🧱 RESERVED ---------------------------------------------------------

fm_reserved1: ""
fm_reserved2: ""
---

<!-- SDLC_INSTANCE_ID: PRJ-6104-SmartChickenDoor -->

# 04 Implementation

Realizácia návrhu – kód, konfigurácia, pipeline.

- 🧩 [Code Structure – moduly firmvéru](./code-structure.md)
- 🧰 [Used Technologies – hardvér, softvér, zdroje](./used-technologies.md)

## 🗓️ Plán realizácie

| Etapa | Výstup | Stav |
|---|---|---|
| **1. Mechanika** | Rozmery, 3D tlač PETG dvierok, líšt, cievky a držiaka; overenie zádržnej polohy. | ⬜ |
| **2. Pohon** | Motor N20 + DRV8833, jeden zdroj 5 V; meranie prúdu a bezpečný ručný STOP. | ⬜ |
| **3. Senzory** | Montáž magnetu, dvojice Reed kontaktov a BH1750; overenie vo vlhkom prostredí. | ⬜ |
| **4. Základ firmware** | Stavy dvierok, detekcia chýb, pohyb, časové limity, fyzické tlačidlá. | ⬜ |
| **5. Wi-Fi a login** | `KURNIK-XXXX`, DNS alias `kurnik.sk`, webserver, prvotný účet a zmena hesla. | ⬜ |
| **6. Web konfigurácia** | Dashboard, Wi-Fi STA, režimy, prahy, časy, poloha a trvalé uloženie. | ⬜ |
| **7. Bezpečnosť/testy** | Blokovanie chybných príkazov, ochrana pred privretím, výpadky, vlhkosť. | ⬜ |
| **8. P2 funkcie** | Udalosti, firmware update, kalibrácia, obnova nastavení, mDNS. | ⬜ |

*Stav: ⬜ nezačaté · 🟨 rozpracované · ✅ hotové*

---
**Navigation:** [⬆️ Up](../index.md) · [🏠 Home](../index.md)
