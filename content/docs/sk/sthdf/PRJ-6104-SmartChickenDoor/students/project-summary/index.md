---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.885496+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "b375a69c-970c-442f-80cd-a6400f5e332b"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "project summary"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Project Summary – PRJ-6104 Smart Chicken Door."


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

# 📝 Project Summary

## 🔖 Identifikácia
## 1️⃣ Názov projektu
- **Názov projektu:** `PRJ-6104-SmartChickenDoor` – Inteligentné dvierka pre sliepky
- **Stručný popis:** Lacný automatický vstup do kurína s ESP32, vertikálnym posuvom dvierok na lanku a svetelným snímačom BH1750. Dvierka sa otvárajú a zatvárajú manuálne, podľa času, podľa východu/západu slnka alebo podľa intenzity svetla. Ovládanie a nastavenia prebiehajú cez zabudovanú webovú stránku z mobilu alebo PC – bez cloudu a bez aplikácie.

## 2️⃣ Členovia tímu

| ST ID | Meno | Rola v tíme | Kompetencie |
|-------|------|-------------|-------------|
| ST0XX | Filip Chromek | _doplniť_ | _doplniť_ |
| ST0XX | Dominik Mojto | _doplniť_ | _doplniť_ |
| ST0XX | Alexander Ovšonka | _doplniť_ | _doplniť_ |

## 3️⃣ Motivácia tímu
- Prečo ste si vybrali tento projekt? _(doplňte)_
- Aký osobný alebo profesný zmysel má pre vás riešenie tejto témy? _(doplňte)_
- **Prečo je projekt dôležitý / aký problém rieši:** odbremení chovateľa od každodenného ručného otvárania a zatvárania kurína a chráni sliepky v noci – pri nízkej cene, s vlastnou 3D tlačou a bez závislosti od cloudu.

## 4️⃣ Cieľ a pridaná hodnota projektu
- **Finálny cieľ:** funkčný prototyp automatických dvierok, ktoré sa otvoria a zatvoria podľa zvoleného režimu a dajú sa nakonfigurovať z mobilu alebo počítača bez cloudu.
- **Ako spoznáme úspech:** prototyp prejde [akceptačnými testami T01–T22](../../projects/sdlc/05-Testing/test-cases.md) – najmä bezpečnostnými (STOP, časový limit pohybu, ochrana proti privretiu, dvierka nespadnú pri výpadku napájania).

## 5️⃣ Popis riešenia
- **Mechanika:** vertikálne 3D tlačené dvierka a vodiace lišty (PETG/ASA), motor N20, lanko a navíjacia cievka.
- **Riadenie a sieť:** ESP32 s vlastnou Wi-Fi `KURNIK-XXXX`, lokálnym DNS (`http://kurnik.sk`), webovým serverom a voliteľným pripojením do domácej Wi-Fi.
- **Snímanie:** BH1750 (svetlo v luxoch) a 2× Reed kontakt + magnet (horná/dolná poloha).
- **Pohon a napájanie:** ovládač DRV8833, jeden zdroj 5 V / 3 A.
- **Ovládanie:** web, fyzické tlačidlá, režimy MANUÁLNY / ČASOVÝ / SLNKO / SVETLO.
- Podrobnosti: [03 Design](../../projects/sdlc/03-Design/index.md) · [Architektúra](../../projects/sdlc/03-Design/architecture-diagram.md)

## 6️⃣ Projektový plán
- Odhadovaný čas na prácu: _x hodín / týždeň_
- Predpokladaný stav v čase prezentácie: _MVP / prototyp / dokumentácia / funkčný produkt_
- Hlavné míľniky (podrobne v [04 Implementation](../../projects/sdlc/04-Implementation/index.md)):
  - [ ] 1. Mechanika – 3D tlač dvierok, líšt, cievky a držiaka
  - [ ] 2. Pohon – N20 + DRV8833, meranie prúdu, ručný STOP
  - [ ] 3. Senzory – Reed kontakty a BH1750
  - [ ] 4. Základ firmvéru – stavy dvierok, limity, tlačidlá
  - [ ] 5. Wi-Fi a login – AP, DNS alias, webserver, zmena hesla
  - [ ] 6. Web konfigurácia – dashboard, režimy, prahy, časy
  - [ ] 7. Bezpečnosť a testy
  - [ ] 8. P2 funkcie – história, FW update, kalibrácia, mDNS

### 📅 Míľniky a výstupy
- **Do januára dodáme:**
  - [ ] prototyp
  - [ ] prezentáciu
  - [ ] dokumentáciu

## 7️⃣ Zákazník a hodnoty
- **Používateľ:** správca kurína – majiteľ domáceho chovu sliepok.
- **Prínos:** automatické a bezpečné otváranie/zatváranie, ovládanie z mobilu bez aplikácie a cloudu, nízka cena (orientačne 25–40 € bez filamentu – pozri [Feasibility Study](../../projects/sdlc/02-Analysis/feasibility-study.md)).

## 8️⃣ Očakávané výstupy
- **Dokumentácia:** SDLC sekcie v tomto repozitári, [návrhová dokumentácia v0.3](../../media/Inteligentne_dvierka_pre_sliepky_dokumentacia_v03.docx), README
- **Artefakty:** 3D modely dielov, firmvér pre ESP32, webové rozhranie, funkčný prototyp

## 📚 Kontext
- Technické zdroje: [Used Technologies](../../projects/sdlc/04-Implementation/used-technologies.md)
- KNIFE príspevky, literatúra, inšpirácie: _(doplňte)_

## 🧭 Riziká a závislosti
- **Riziká:** privretie sliepky, pád dvierok z otvorenej polohy, zaseknutie, vlhkosť a korózia, slabý zdroj, únik hesla pri HTTP – podrobne v [02 Analysis](../../projects/sdlc/02-Analysis/index.md).
- **Závislosti:** reálny krútiaci moment motora N20, spôsob zaistenia otvorenej polohy, dostupnosť súčiastok a 3D tlače.

## 9️⃣ Reflexia a ďalšie kroky
Čo očakávate, že sa naučíte? _(doplňte)_  
Ako by sa projekt mohol rozvíjať ďalej? Napr. P2 funkcie – história udalostí, kalibrácia, aktualizácia firmvéru, kontrola prekážok, mDNS `kurnik.local`.

---

## Navigácia
- [↩️ Späť](../index.md)
