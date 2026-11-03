---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.112170+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "364083e0-beb4-4ac6-817f-524344756800"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "code structure"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Moduly firmvéru ESP32 a ich zodpovednosti."


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

# 🧩 Code Structure

## 🧠 Implementačná architektúra firmvéru

Softvér je rozdelený na moduly, ktoré si neblokujú prácu. Webový handler iba validuje používateľa a príkaz, zatiaľ čo pohyb motorom vykonáva samostatný riadiaci stavový automat. Nesmie sa stať, že výpadok prehliadača alebo pomalá Wi-Fi spôsobí nekontrolovaný pohyb.

| Modul | Zodpovednosť |
|---|---|
| **wifi_manager** | Spustenie AP, pripojenie k routeru, stav siete, obnova spojenia. |
| **dns_portal** | Lokálna DNS odpoveď pre `kurnik.sk` v AP; voliteľný captive portal. |
| **web_server** | HTML/CSS/JS stránky, autentifikácia, HTTP API, validácia vstupov. |
| **config_store** | Trvalé uloženie konfigurácie a hesiel; migrácia verzií konfigurácie. |
| **light_sensor** | I²C BH1750, filtrovanie, platnosť čítania a kalibrácia. |
| **position_sensors** | Horný a dolný Reed kontakt, odrušenie signálu a diagnostika. |
| **motor_control** | DRV8833, smer, STOP, časové limity a blokovanie chybných akcií. |
| **scheduler** | TIME, SUN, LIGHT pravidlá, odolnosť voči opakovaniu udalostí. |
| **clock_service** | NTP, časové pásmo, stav synchronizácie, zimný/letný čas. |
| **safety_manager** | Nadradené bezpečnostné podmienky a evidencia porúch. |
| **event_log (P2)** | Kruhový záznam udalostí a chýb, bez hesiel. |

Návrh HTTP API je v [08 Documentation → API Reference](../08-Documentation/api-reference.md).

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
