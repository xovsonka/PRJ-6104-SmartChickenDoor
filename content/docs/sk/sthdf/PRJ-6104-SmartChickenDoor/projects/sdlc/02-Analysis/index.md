---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:23.987920+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "ec9c121e-fccb-45ea-9b64-2c34c6270711"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "02 Analysis"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Bezpečnostné riziká, mitigácie a otvorené technické rozhodnutia."


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

# 02 Analysis

Analýza uskutočniteľnosti, rizík a alternatív riešenia.

- 📈 [Feasibility Study – hardvér a rozpočet](./feasibility-study.md)

## ⚠️ Bezpečnostné riziká, hranice a opatrenia

| Riziko | Mitigácia |
|---|---|
| **Privretie sliepky** | Navrhnúť a overiť ochranu pred prekážkou, obmedzenie sily a bezpečný spôsob zastavenia; testovať s neživou bezpečnou skúšobnou prekážkou. |
| **Pád z otvorenej polohy** | Mechanická zádržná poistka alebo motor s preukázaným udržaním záťaže pri výpadku napájania. |
| **Zaseknutie dvierok** | Časový limit, detekcia neúspešného dokončenia, blokovanie opakovaného pohybu bez zásahu. |
| **Vlhkosť / korózia** | IP65 kryt, kabeláž vo vývodkách, ochrana snímačov pred dažďom a kondenzáciou. |
| **Náhodný reset ESP32** | Motor defaultne vypnutý, nezávislé kontroly stavu snímačov a konfigurácie. |
| **Slabý zdroj** | Zmerať rozbehový a blokovací prúd motora, v prípade potreby vybrať primeraný zdroj. |
| **Únik hesla pri HTTP** | Sieť považovať za dôveryhodnú, nepovoliť internetový port-forwarding; nasadenie mimo izolovaného AP vyžaduje zváženie HTTPS. |
| **Zneužitie štítku s heslami** | Štítok prístupný iba majiteľovi; jedinečné údaje, vynútená zmena webového hesla. |
| **Výpadok času / internetu** | Prevádzka svetla a tlačidiel; neprípustné spustenie podľa neznámeho času. |

## ❓ Otvorené technické rozhodnutia

- Presný rozmer, hmotnosť a zdvih vytlačených dvierok; reálny krútiaci moment zvoleného motorčeka N20.
- Spôsob zaistenia otvorenej polohy pri odpojení napájania a núdzového mechanického otvorenia.
- Účinná ochrana proti privretiu pri gravitačnom zatváraní; jej súčasť a cena.
- Voľba montážneho krytu a bezpečného umiestnenia 5 V adaptéra v blízkosti kurína.
- Či v domácej Wi-Fi ponechať AP trvalo zapnutý, alebo ho zapínať iba na nastavenie / pri strate STA.
- Povinnosť TLS/HTTPS pri konečnom použití v domácej LAN; spôsob poskytovania certifikátu.

---
**Navigation:** [⬆️ Up](../index.md) · [🏠 Home](../index.md)
