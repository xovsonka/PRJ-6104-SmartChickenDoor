---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:23.975148+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "19fb2853-6b4a-471b-bcc0-7be18fb911bc"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "feasibility study"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Potrebný hardvér a orientačný rozpočet prototypu."


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

# 📈 Feasibility Study

## 🛒 Potrebný hardvér a orientačný rozpočet

Odhad je pre jeden funkčný prototyp. Dvierka, vodiace lišty, cievku a držiak motora vytlačí používateľ. Ceny sa menia podľa obchodu, poštovného a kvality. Suma nezahŕňa filament, prácu a nástroje.

| Komponent | Počet | Odhad |
|---|---|---|
| **ESP32 DevKit s 2,4 GHz Wi-Fi** | 1 | 4–8 € |
| **Motor N20 s prevodovkou pre 5–6 V** | 1 | 3–7 € |
| **Motorový ovládač DRV8833** | 1 | 1,50–3 € |
| **BH1750 modul I²C** | 1 | 1–4 € |
| **Magnetický Reed snímač** | 2 | 1–4 € spolu |
| **Magnet na dvierka** | 1 | 0–1 € |
| **Fyzické tlačidlá** | 2–3 | 1–3 € |
| **USB / DC zdroj 5 V / 3 A** | 1 | 0–7 € |
| **Ochranný kryt IP65** | 1 | 4–8 € |
| **Lanko, káble, vývodky, poistka, kondenzátor** | sada | 3–7 € |
| **Skrutky a montážny materiál** | sada | 2–5 € |
| **Vytlačené diely** | sada | filament mimo súčtu |

:::tip Celkové náklady
Približne **21–57 €** bez filamentu a dopravy; ak už máš 5 V adaptér a kúpiš diely lacno z Číny, praktický cieľ je okolo **25–40 €**. Bezpečnostná mechanika a jej odladenie môžu výslednú sumu zvýšiť.
:::

## ✂️ Čo sa dá vynechať a čo nie

Samostatný Wi-Fi modul netreba – ESP32 ho obsahuje. Solárny panel a ďalší menič napätia nie sú potrebné. RTC môže byť voliteľný, ale jeho vynechanie znamená, že pri výpadku napájania bez dostupného internetu sa časové a astronomické režimy nesmú považovať za spoľahlivé. Magnetické snímače polohy, ochranu pred pádom a proti privretiu nevypúšťať len kvôli cene.

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
