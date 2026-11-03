---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:24.066066+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "582439de-a5d2-4dfe-9b6e-29efb630ae8e"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "ui mockups"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Návrh obrazoviek webového rozhrania."


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

# 🎨 UI Mockups

## 🖥️ Návrh obrazoviek webového rozhrania

| Obrazovka / URL | Obsah a akcie |
|---|---|
| **Prihlásenie `/login`** | Prihlasovacie meno, heslo, zobrazovanie chyby bez prezrádzania detailov; prvé prihlásenie presmeruje na zmenu hesla. |
| **Prehľad `/`** | Stav dvierok a motora, aktívny režim, meranie luxov, horný/dolný snímač, posledná udalosť, čas, stav Wi-Fi, tlačidlá OTVORIŤ / ZATVORIŤ / STOP. |
| **Režimy `/mode`** | Výber jedného režimu: manuálny, časový, astronomický alebo svetelný; potvrdenie zmeny a informácia o vplyve na aktuálnu automatiku. |
| **Časový plán `/schedule`** | Otvorenie HH:MM, zatvorenie HH:MM; validácia konfliktov a nastavenie platného časového pásma. |
| **Slnko `/sun`** | Zemepisná šírka a dĺžka, časové pásmo, posun otvorenia voči východu a zatvorenia voči západu; náhľad časov pre dnešok. |
| **Svetlo `/light`** | Aktuálna hodnota BH1750 v luxoch, otvárací/zatvárací prah, stabilizačné intervaly, oneskorenie; vizualizácia prahu a kalibračná pomôcka. |
| **Wi-Fi `/wifi`** | Zoznam nájdených sietí, SSID, heslo (skryté), Test a uloženie, stav pripojenia, lokálna IP, prepínač režimu AP. |
| **Zariadenie `/settings`** | Názov zariadenia, časové pásmo, limity pohybu, politika ručného zásahu, uloženie a obnovenie bezpečných predvolieb. |
| **Účet `/account`** | Zmena webového hesla, odhlásenie, kontrola predvolených údajov, neukazovať uložené heslá. |
| **Diagnostika `/diagnostics`** | Stav snímačov, luxy, signál Wi-Fi, čas od štartu, platnosť času, posledná chyba, informácie o FW. |
| **Servis `/service` (P2)** | Kontrola senzorov, bezpečná kalibrácia, test pohybu, história udalostí, prípadne aktualizácia FW. |
| **Chybové stavy** | Jasne uvedený problém, čas výskytu, blokovaný príkaz a odporúčaný postup opravy. |

## 📱 Príklad úvodnej obrazovky – textový wireframe

```text
KURNÍK | Dashboard
Stav: ZATVORENÉ • Režim: SVETLO • Osvetlenie: 17 lx • Wi-Fi: pripojená
Posledná akcia: zatvorené 19:12

[ OTVORIŤ ]  [ ZATVORIŤ ]  [ STOP ]

Menu: Režimy / Svetlo / Časy / Wi-Fi / Diagnostika
```

*Údaje sú ilustračné, nie skutočné meranie.*

Po potvrdení príkazu má rozhranie zobraziť priebežný stav OTVÁRANIE alebo ZATVÁRANIE a následne potvrdený koncový stav. Neznáma poloha sa nesmie vykresliť ako „otvorené“ len podľa uplynutia času.

---
**Navigation:** [⬆️ Up](./index.md) · [🏠 Home](../index.md)
