---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-11-03T15:48:23.905923+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "819ced40-590f-4d6b-b7e2-ddfdf9b619d6"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "01 Requirements"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Cieľ, rozsah, funkčné požiadavky a katalóg softvérových funkcionalít."


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

# 01 Requirements

Zachytenie potrieb, cieľov a očakávaní používateľov.

- 🧑‍🤝‍🧑 [User Stories a scenáre používania](./user-stories.md)
- 🔧 [Nefunkčné požiadavky a zabezpečenie](./non-functional.md)

## 🎯 Cieľ a rozsah projektu

Cieľom je vyrobiť cenovo dostupný automatický vstup do kurína, ktorý sa otvorí a zatvorí podľa zvoleného režimu a ktorý vie používateľ nakonfigurovať z mobilu alebo počítača bez potreby cloudu. Projekt počíta s vlastnou 3D tlačou mechaniky a s jednoduchým lacným elektrickým zapojením.

Dokumentácia pokrýva hardvér, bezpečnosť, používateľské scenáre, úplný navrhovaný rozsah softvéru, dátové nastavenia a akceptačné testy. Ide o špecifikáciu pripravovaného prototypu, nie o potvrdenie, že už boli všetky funkcie implementované alebo bezpečnostne overené.

:::warning Dôležité
Zariadenie nebude používať solárny panel. Na meranie intenzity okolitého svetla bude použitý digitálny snímač BH1750. Pre automatické zatváranie treba samostatne preveriť ochranu zvierat pred privretím.
:::

## 🧾 Prehľad návrhu

| Oblasť | Návrh |
|---|---|
| **Mechanika** | Vertikálne 3D tlačené dvierka a vodiace lišty, motor N20, lanko a navíjacia cievka |
| **Riadenie a sieť** | ESP32, vlastná Wi-Fi `KURNIK-XXXX`, lokálny DNS, webový server, voliteľná domáca Wi-Fi |
| **Svetlo** | BH1750 cez I²C – meranie luxov; žiadny solárny panel |
| **Detekcia polohy** | 2× magnetický kontakt (Reed) + magnet na dvierkach; alternatívne koncové spínače |
| **Napájanie** | Jeden 5 V / 3 A zdroj, paralelná vetva ESP32 a motorového ovládača |
| **Ovládanie** | Web, fyzické tlačidlá, časový režim, podľa svetla, podľa východu/západu slnka |
| **Prístup** | Po pripojení k Wi-Fi zariadenia: `http://kurnik.sk`, záloha `http://192.168.4.1` |

## ✅ Funkčné požiadavky systému

| ID | Požiadavka a kritérium splnenia |
|---|---|
| **F01** | Používateľ otvorí a zatvorí dvierka cez web a lokálne tlačidlá; motor sa zastaví pri dosiahnutí snímača. |
| **F02** | Používateľ nastaví čas otvorenia a zatvorenia a zariadenie vykoná udalosti raz za deň. |
| **F03** | Používateľ zvolí astronomický režim; konfigurácia polohy a časového posunu určuje udalosti. |
| **F04** | Používateľ zvolí režim BH1750 a nastaví prahy, hysterézu a minimálne trvanie. |
| **F05** | Zariadenie vytvorí vlastnú Wi-Fi a sprístupní administráciu na `http://kurnik.sk` alebo na lokálnej IP. |
| **F06** | Prístup do administrácie vyžaduje platné webové prihlasovacie údaje. |
| **F07** | Používateľ môže pripojiť zariadenie do existujúcej Wi-Fi a vidí výsledok pripojenia. |
| **F08** | Dashboard zobrazuje aktuálne luxy, polohu, smer pohybu, režim, sieť a chyby. |
| **F09** | Nastavenia zostanú uložené po reštarte a nespôsobia spontánny nebezpečný pohyb. |
| **F10** | Pri chybe snímača, prekročení limitu, neplatnom stave alebo STOP motor zastane. |
| **F11** | Pri výpadku internetu fungujú manuálne ovládanie a svetelný režim nezávisle od NTP. |
| **F12** | Ak nie je dostupný správny čas, nesmú sa bezhlavo vykonávať plánované ani astronomické udalosti. |
| **F13** | Zariadenie signalizuje problémy, uchová posledný dôvod zastavenia a umožní kontrolu snímačov. |

## 🧩 Katalóg softvérových funkcionalít

Konkrétne implementačné požiadavky softvéru. **P1** = základná verzia, **P2** = plánované rozšírenie. Označenia SW slúžia na sledovanie implementácie a testov.

| ID | Prio. | Funkcionalita | Špecifikácia |
|---|---|---|---|
| **SW01** | P1 | AP Wi-Fi | Zariadenie vysiela vlastnú Wi-Fi `KURNIK-XXXX` a pridelí klientovi IP. |
| **SW02** | P1 | Lokálny DNS | Na AP preloží `kurnik.sk` na lokálnu IP ESP32; dostupná IP záloha. |
| **SW03** | P1 | Prihlásenie | Login používateľským menom a heslom zo štítku; overenie relácie. |
| **SW04** | P1 | Zmena hesla | Pri prvom prihlásení zmena hesla; ďalšia zmena v Nastaveniach. |
| **SW05** | P1 | Domáca Wi-Fi | Sken sietí, zadanie hesla, pripojenie, stav a opätovný pokus. |
| **SW06** | P1 | Dashboard | Aktuálna poloha, pohyb, aktívny režim, svetlo v luxoch, čas, sieť, chyba. |
| **SW07** | P1 | Otvoriť | Manuálny príkaz na pohyb nahor pri splnení bezpečnostných podmienok. |
| **SW08** | P1 | Zatvoriť | Manuálny príkaz na pohyb nadol pri splnení bezpečnostných podmienok. |
| **SW09** | P1 | STOP | Okamžité zastavenie motora z webu aj pri chybe. |
| **SW10** | P1 | Voľba režimu | Manuálny / Čas / Slnko / Svetlo; vždy iba jeden aktívny režim. |
| **SW11** | P1 | Časový plán | Samostatný denný čas otvorenia a zatvorenia. |
| **SW12** | P1 | Astronomické udalosti | Výpočet východu a západu slnka podľa polohy/dátumu, posuny minút. |
| **SW13** | P1 | Svetelná automatika | BH1750: nastaviteľné prahy v luxoch, hysteréza a stabilizačné intervaly. |
| **SW14** | P1 | Snímanie polohy | Dva Reed snímače; otvorené, zatvorené, medzipoloha, porucha. |
| **SW15** | P1 | Riadenie motora | DRV8833: smer pohybu, zastavenie na príslušnom senzore. |
| **SW16** | P1 | Ochrany | Timeout pohybu, STOP pri chybe, spracovanie konfliktu senzorov. |
| **SW17** | P1 | Konfigurácia | Uloženie a načítanie nastavení z pamäte ESP32. |
| **SW18** | P1 | Čas a pásmo | NTP z internetu, zobrazenie platnosti času, časové pásmo / letný čas. |
| **SW19** | P1 | Bezpečný reštart | Po štarte neotáčať motorom automaticky, zhodnotiť polohu a chyby. |
| **SW20** | P1 | Fyzické ovládanie | Lokálne tlačidlá OTVORIŤ / ZATVORIŤ, odporúčané aj núdzové STOP. |
| **SW21** | P1 | Diagnostika | Stav oboch snímačov, posledná akcia, dôvod zastavenia, stav BH1750. |
| **SW22** | P1 | Chybové správy | Čitateľné chyby v UI a blokovanie rizikových operácií. |
| **SW23** | P2 | História udalostí | Záznam otvorenia/zatvorenia, výpadkov, zmien režimu a chybných pokusov. |
| **SW24** | P2 | Kalibrácia | Servisná obrazovka na overenie polôh a meraní; s bezpečnostným blokovaním. |
| **SW25** | P2 | Aktualizácia FW | Lokálne nahratie firmvéru; počas aktualizácie zakázať pohyb a overovať obraz. |
| **SW26** | P2 | Továrenský reset | Fyzické potvrdenie obnovenia nastavení, hesiel a Wi-Fi. |
| **SW27** | P2 | Kontrola prekážok | Vstup z vhodného bezpečnostného snímača alebo mechanizmu; STOP pri zatváraní. |
| **SW28** | P2 | mDNS kurnik.local | Doplňujúci prístup cez domácu Wi-Fi, ak ho klient podporuje. |
| **SW29** | P2 | Stav AP režimu | Povoliť trvalo AP+STA alebo AP len pri konfigurácii/chybe domácej Wi-Fi. |
| **SW30** | P2 | Záloha nastavení | Export / import nesenzitívnej konfigurácie, bez hesiel. |

---
**Navigation:** [⬆️ Up](../index.md) · [🏠 Home](../index.md)
