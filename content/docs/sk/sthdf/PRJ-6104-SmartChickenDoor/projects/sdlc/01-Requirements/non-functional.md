---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:23.927501+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "b801d891-80fe-4243-b608-4a8e01df2716"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "non functional"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Nefunkčné požiadavky, prihlásenie a zabezpečenie."


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

# 🔧 Non-Functional Requirements (NFR)

## 📋 Nefunkčné požiadavky

| ID | Oblasť | Požiadavka |
|---|---|---|
| **NF01** | Náklady | Minimalizovať cenu použitím ESP32, lacného N20 a vlastných 3D výtlačkov. |
| **NF02** | Napájanie | Jeden kvalitný stabilizovaný 5 V zdroj; overený maximálny odber, oddelené vetvy. |
| **NF03** | Odolnosť | Elektronika v kryte aspoň IP65 a správne umiestnené tesnenia/vývodky. |
| **NF04** | Prístupnosť | Responzívny web pre telefón a PC bez samostatnej aplikácie. |
| **NF05** | Dostupnosť | Lokálne tlačidlá, ochrany a automatika podľa svetla aj bez domácej Wi-Fi. |
| **NF06** | Bezpečnosť | Žiadna otvorená Wi-Fi; vlastné prístupové údaje, autentifikované príkazy, timeout relácie. |
| **NF07** | Prevádzka | Chybové stavy a maximálne časy pohybu sú deterministické a testovateľné. |
| **NF08** | Údržba | Dostupné servisné časti; možnosť bezpečnej ručnej manipulácie pri výpadku napájania. |
| **NF09** | Zrozumiteľnosť | Systém zobrazuje skutočne potvrdenú polohu, nie len predpoklad. |
| **NF10** | Súkromie | Bez cloudového konta, bez internetového vystavenia administrácie. |

## 🔐 Prihlásenie a zabezpečenie

Na štítku zo spodnej strany zariadenia budú predvolené údaje. Heslo do Wi-Fi a heslo do webovej administrácie musia byť odlišné a pre každý kus jedinečné; odporúča sa aj QR kód pre pripojenie. Ak môže mať niekto fyzický prístup ku štítku, ide o bezpečnostné riziko – umiestniť ho tak, aby nebol voľne dostupný cudzím osobám.

| Funkcia | Pravidlo |
|---|---|
| **Wi-Fi prístup** | Jedinečný SSID a dostatočne silné WPA2/WPA3 heslo; žiadna otvorená Wi-Fi. |
| **Webové konto** | Správca s jedinečným počiatočným heslom, vynútená zmena pri prvom prihlásení. |
| **Autentifikácia** | Chránené stránky a API príkazy, krátkodobá relácia, odhlásenie, timeout nečinnosti a obmedzenie pokusov. |
| **Citlivé údaje** | Nezobrazovať heslá do routera; neprenášať ich späť do prehliadača. Preferovať bezpečné úložisko NVS. |
| **HTTP/HTTPS** | Prototyp: iba izolovaná dôveryhodná lokálna sieť. HTTP neposkytuje šifrovanie hesiel; pre produkčné nasadenie a bežnú LAN vyhodnotiť HTTPS. |
| **Príkazy motora** | Overovať prihlásenie, metódu požiadavky a CSRF ochranu; neumožniť spustenie príkazu jednoduchým otvorením URL. |
| **Obnova prístupu** | Reset len fyzickým tlačidlom na zariadení, s jasným potvrdením a bez samovoľného pohybu motora. |
| **Sieťové hranice** | Nikdy neotvárať riadiace rozhranie priamo do internetu cez port-forwarding; cloud nie je súčasťou návrhu. |

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
