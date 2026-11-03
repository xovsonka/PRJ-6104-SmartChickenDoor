---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.033781+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "89022f47-4907-4cfe-b7e2-c78668e9e1d2"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "data model"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Konfigurovateľné parametre a stavy dvierok."


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

# 🗃️ Data Model

## ⚙️ Konfigurovateľné parametre

Nastavenia sa ukladajú do trvalej pamäte ESP32 (NVS). Citlivé polia (heslá) sa nikdy nevracajú do prehliadača.

| Nastavenie | Typ / príklad | Validácia / poznámka |
|---|---|---|
| **Názov zariadenia** | text „Kurník“ | Maximálna dĺžka; bezpečné spracovanie znakov. |
| **Aktívny režim** | MANUAL / TIME / SUN / LIGHT | Presne jedna možnosť. |
| **Čas otvorenia a zatvorenia** | HH:MM | Vyžaduje platný čas a pásmo. |
| **Zemepisná poloha** | šírka a dĺžka | Šírka −90 až 90°, dĺžka −180 až 180°; zadá používateľ. |
| **Časové pásmo** | napr. Europe/Bratislava | Letný/zimný čas podľa pravidiel pásma. |
| **Posun východ/západ** | minúty ± | Samostatne otváranie a zatváranie. |
| **BH1750: otvárací prah** | lux, napr. 30 lx | Musí byť vyšší než zatvárací prah. |
| **BH1750: zatvárací prah** | lux, napr. 10 lx | Hodnoty sú iba ukážka na kalibráciu. |
| **Čas potvrdenia svetla** | minúty, napr. 10/15 | Samostatne ráno a večer; ochrana pred krátkou zmenou. |
| **Doba pohybu – limit** | sekundy, napr. 20 s | Dostať do krajnej polohy alebo STOP s chybou. |
| **Manuálny zásah** | do ďalšej udalosti / trvalo | Jasne viditeľné v dashboarde. |
| **Wi-Fi sieť a heslo** | SSID + tajné heslo | Heslo sa nikdy nesmie vypisovať späť. |
| **AP režim** | vždy zapnutý / fallback | Nesúvisiaci s nastavením domáceho routera. |
| **Admin heslo** | tajná hodnota | Zmena pri prvom prihlásení, bezpečné pravidlá. |
| **Dátum a čas** | NTP; servisné ručné nastavenie voliteľné | Po reštarte s neplatným časom zakázať časové plány. |

## 🚪 Stavy dvierok

Stav sa určuje zo snímačov polohy (pozri [03 Design – Detekcia otvorenia a zatvorenia](./index.md)) a z prebiehajúceho príkazu: **OTVORENÉ**, **ZATVORENÉ**, **OTVÁRANIE**, **ZATVÁRANIE**, **MEDZIPOLOHA / NEZNÁMA**, **PORUCHA**.

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
