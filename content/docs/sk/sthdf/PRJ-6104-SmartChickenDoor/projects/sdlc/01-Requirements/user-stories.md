---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:23.943781+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "3c6d1be4-e75f-4ff5-b78e-0e8a16c849f2"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "user stories"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Používateľ, prvé spustenie a bežné používanie zariadenia."


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

# 🧑‍🤝‍🧑 User Stories a scenáre používania

## 👤 Používateľ

Hlavná rola je **správca kurína** (majiteľ zariadenia). Nepočíta sa s cloudovým účtom ani mobilnou aplikáciou; ovládanie prebieha cez zabudovanú webovú stránku. Voliteľná servisná rola môže používať diagnostiku, avšak pre prvý prototyp postačí jeden účet správcu.

## 🚀 Prvé spustenie – od zapojenia po webové ovládanie

1. Používateľ pripojí bezpečný 5 V zdroj. ESP32 spustí vlastnú zabezpečenú Wi-Fi sieť s názvom `KURNIK-XXXX`, kde XXXX predstavuje krátky jedinečný identifikátor zariadenia.
2. Na spodnej strane zariadenia je štítok: názov Wi-Fi, jedinečné heslo Wi-Fi, prihlasovacie meno správcu, jedinečné počiatočné webové heslo a adresa `http://kurnik.sk`. Heslá Wi-Fi a webu sú rozdielne.
3. Používateľ sa z telefónu pripojí k Wi-Fi `KURNIK-XXXX`. Telefón môže zobraziť upozornenie „sieť bez internetu“ – je to očakávané.
4. V prehliadači otvorí presne `http://kurnik.sk`. Lokálny DNS server zariadenia v režime AP presmeruje doménu na IP ESP32; ako záloha funguje `http://192.168.4.1`.
5. Zobrazí sa prihlasovacia stránka. Používateľ zadá prihlasovacie údaje zo štítku. Pri prvom prihlásení bude vyzvaný na zmenu počiatočného hesla správcu.
6. Po prihlásení sa otvorí hlavná obrazovka so stavom dvierok, svetlom v luxoch, zvoleným režimom, možnosťami OTVORIŤ / ZATVORIŤ / STOP a prístupom k nastaveniam.
7. V časti Wi-Fi môže vyhľadať domácu sieť, zadať jej heslo a uložiť pripojenie. Zariadenie oznámi úspech/neúspech a zobrazí adresu prístupu v domácej sieti.
8. Používateľ nastaví typ prevádzky, prahové hodnoty svetla alebo časy, prípadne polohu a časové pásmo, a uloží konfiguráciu. Následne môže spustiť bezpečný test otvorenia a zatvorenia.

:::info Režim AP a internet
Pripojenie k Wi-Fi zariadenia neprináša internet. Lokálny DNS „kurnik.sk“ platí iba v sieti vysielanej ESP32; nepredpokladá registráciu ani vlastníctvo verejnej domény kurnik.sk.
:::

## 🔁 Bežné používanie

Po zapnutí alebo reštarte ESP32 obnoví konfiguráciu a zistí fyzickú polohu dvierok z dvojice snímačov. Systém zobrazuje poslednú akciu, prípadnú chybu a priebežné meranie svetla. Používateľ môže kedykoľvek zvoliť iný režim alebo odoslať manuálny príkaz, ak bezpečnostná logika dovolí pohyb.

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
