---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.161393+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "3988ea58-a3a9-430b-86e9-cfaa0c8ca5cb"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "used technologies"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Hardvér, softvér a technické zdroje."


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

# 🧰 Used Technologies

## 🔩 Hardvér

| Komponent | Úloha v projekte |
|---|---|
| **ESP32 DevKit (2,4 GHz Wi-Fi)** | Riadiaca jednotka, Wi-Fi AP+STA, DNS, webový server, logika. |
| **Motor N20 s prevodovkou (5–6 V)** | Navíjanie lanka – zdvíhanie a spúšťanie dvierok. |
| **DRV8833** | H-mostík – ovládač motora (smer, STOP). |
| **BH1750 (I²C)** | Meranie intenzity svetla v luxoch. |
| **2× Reed kontakt + magnet** | Detekcia hornej a dolnej polohy dvierok. |
| **Fyzické tlačidlá** | Lokálne OTVORIŤ / ZATVORIŤ / núdzové STOP. |
| **Zdroj 5 V / 3 A** | Jediný zdroj; paralelné vetvy pre ESP32 a DRV8833. |
| **3D tlač PETG/ASA** | Dvierka, vodiace lišty, cievka, držiak motora. |
| **Kryt IP65** | Ochrana elektroniky pred vlhkosťou a nečistotami. |

## 💻 Softvér

- Firmvér pre ESP32 (Arduino ESP32 / ESP-IDF) – Wi-Fi AP+STA, `DNSServer`, HTTP server
- Webové rozhranie: HTML / CSS / JS servírované priamo z ESP32
- Úložisko konfigurácie: NVS (s možnosťou šifrovania)
- Čas: NTP + pravidlá časového pásma

## 📚 Technické zdroje

- Espressif – Arduino ESP32 Wi-Fi API, AP a STA: https://docs.espressif.com/projects/arduino-esp32/en/latest/api/wifi.html
- Espressif – ukážka AP+STA: https://github.com/espressif/esp-idf/blob/master/examples/wifi/softap_sta/README.md
- Espressif – Captive Portal príklad a obmedzenie HTTPS: https://github.com/espressif/esp-idf/blob/master/examples/protocols/http_server/captive_portal/README.md
- Espressif – DNS captive portal: https://github.com/espressif/arduino-esp32/blob/master/libraries/DNSServer/examples/CaptivePortal/CaptivePortal.ino
- ROHM – datasheet BH1750FVI (I²C, lux, 2,4–3,6 V): https://cdn.velleman.eu/downloads/29/infosheets/bh1750fvi-e_datasheet.pdf
- Texas Instruments – DRV8833 H-mostík: https://www.ti.com/product/DRV8833
- Espressif – šifrovanie NVS: https://docs.espressif.com/projects/esp-idf/en/v5.5.1/esp32/api-reference/storage/nvs_encryption.html

*Technické parametre a orientačné cenové odhady sú určené na návrh prototypu (20. 10. 2026). Konkrétne súčiastky, zapojenie a bezpečnostné vlastnosti treba pred montážou overiť.*

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
