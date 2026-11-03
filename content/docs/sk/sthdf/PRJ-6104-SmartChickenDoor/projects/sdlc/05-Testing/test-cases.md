---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.224689+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "5bd180e2-ae37-4ad4-b16e-9ef49363e960"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "test cases"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Akceptačné a integračné testy T01–T22."


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

# ✅ Test Cases

## 🧪 Akceptačné a integračné testy

| ID | Scenár | Očakávaný výsledok | Výsledok |
|---|---|---|---|
| **T01** | Pripojiť mobil k `KURNIK-XXXX`. | Zariadenie poskytne lokálnu IP a web. | ⬜ |
| **T02** | Otvoriť `http://kurnik.sk` na AP. | Zobrazí sa login; záloha `192.168.4.1`. | ⬜ |
| **T03** | Zadať nesprávne webové heslo. | Vstup sa zamietne, pokusy sa limitujú. | ⬜ |
| **T04** | Prvé prihlásenie heslom zo štítku. | Vyžaduje sa zmena hesla správcu. | ⬜ |
| **T05** | Zvoliť domácu Wi-Fi a správne heslo. | ESP32 sa pripojí, zobrazí IP a stav. | ⬜ |
| **T06** | Zadať nesprávne heslo domácej Wi-Fi. | Zostane dostupný AP a konfigurácia. | ⬜ |
| **T07** | Otvoriť web z domácej Wi-Fi. | Funguje cez lokálnu IP; `kurnik.sk` bez DNS úpravy nie je sľúbené. | ⬜ |
| **T08** | Spustiť otvorenie / zatvorenie z dashboardu. | Motor ide správnym smerom a končí na snímači. | ⬜ |
| **T09** | Použiť STOP počas pohybu. | Motor okamžite prestane dostávať príkaz na pohyb. | ⬜ |
| **T10** | Použiť tlačidlá bez spojenia s Wi-Fi. | Dvierka reagujú podľa bezpečnostných pravidiel. | ⬜ |
| **T11** | Nastaviť časový režim. | Plánovaná udalosť nastane iba raz. | ⬜ |
| **T12** | Nastaviť astronomický režim a polohu. | Zobrazia sa správne dátumy/časy vrátane pásma. | ⬜ |
| **T13** | Zmeniť osvetlenie BH1750 okolo prahov. | Hysteréza zabráni kmitaniu. | ⬜ |
| **T14** | Krátko zakryť snímač svetla. | Bez reakcie pred vypršaním stabilizačného intervalu. | ⬜ |
| **T15** | Odpojiť BH1750. | Chyba senzora, žiadne slepé riadenie podľa svetla. | ⬜ |
| **T16** | Aktivovať oba polohové snímače. | STOP a chyba neplatnej kombinácie. | ⬜ |
| **T17** | Simulovať nedosiahnutie koncového snímača. | Po limite STOP a stav PORUCHA. | ⬜ |
| **T18** | Reštartovať počas pohybu. | Pohon nezačne samovoľne ďalší pohyb. | ⬜ |
| **T19** | Odpojiť napájanie s otvorenými dvierkami. | Dvierka nespadnú ani sa neuvoľní lanko. | ⬜ |
| **T20** | Overiť ochranu priestoru zatvárania. | Mechanizmus pri prekážke nevyvinie nebezpečný tlak. | ⬜ |
| **T21** | Vypnúť internet a reštartovať zariadenie. | Pri neplatnom čase sa neaktivuje TIME/SUN, LIGHT funguje. | ⬜ |
| **T22** | Uložiť režim, prahy a Wi-Fi; reštartovať. | Nastavenia ostanú, heslá sa nezobrazia. | ⬜ |

*Výsledok: ⬜ netestované · ✅ prešlo · ❌ zlyhalo – výsledky zapisuj aj do [Test Results](./test-results.md).*

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
