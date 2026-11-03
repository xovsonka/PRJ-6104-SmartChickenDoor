# 🐔 PRJ-6104 – Smart Chicken Door

**Inteligentné dvierka pre sliepky** – lacný modul s ESP32, vertikálnym posuvom dvierok na lanku, svetelným snímačom BH1750 a kompletným webovým rozhraním. Dvierka sa otvárajú a zatvárajú manuálne, podľa času, podľa východu/západu slnka alebo podľa svetla – ovládanie z mobilu alebo PC, bez cloudu.

Tímový projekt pre predmet **Systémové myslenie v IT a digitálna fabrikácia** (FIIT STU), 2026/2027.

## 👥 Tím

| Meno | Rola |
|---|---|
| Filip Chromek | PM – projektový manažér |
| Dominik Mojto | SW – firmvér a webové rozhranie |
| Alexander Ovšonka | HW – mechanika a elektronika |

## 🧾 Prehľad riešenia

| Oblasť | Návrh |
|---|---|
| **Mechanika** | Vertikálne 3D tlačené dvierka a vodiace lišty, motor N20, lanko a navíjacia cievka |
| **Riadenie a sieť** | ESP32, vlastná Wi-Fi `KURNIK-XXXX`, lokálny DNS, webový server, voliteľná domáca Wi-Fi |
| **Svetlo** | BH1750 cez I²C – meranie luxov; žiadny solárny panel |
| **Detekcia polohy** | 2× magnetický kontakt (Reed) + magnet na dvierkach |
| **Napájanie** | Jeden 5 V / 3 A zdroj, paralelná vetva ESP32 a ovládača DRV8833 |
| **Ovládanie** | Web, fyzické tlačidlá, časový režim, podľa svetla, podľa východu/západu slnka |

## 📂 Kde čo nájdeš

Celý obsah projektu je v [`content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/`](content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/index.md):

| Časť | Obsah |
|---|---|
| [`projects/sdlc/`](content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/projects/sdlc/index.md) | Technická dokumentácia – požiadavky, analýza, návrh, implementácia, testy, API |
| [`projects/7ds/`](content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/projects/7ds/index.md) | 7Ds – manažérsky cyklus projektu |
| [`projects/q12/`](content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/projects/q12/index.md) | Q12 – hodnotová os |
| [`students/`](content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/students/index.md) | 7 povinných deliverables (About Me, Project Summary, Pitch, Reflexia…) |
| [`media/`](content/docs/sk/sthdf/PRJ-6104-SmartChickenDoor/media/) | Obrázky a pôvodná návrhová dokumentácia v0.3 (.docx) |

Ostatné priečinky (`core/`, `config/`, `publishing/`) pochádzajú zo šablóny predmetu – nástroje, konfigurácia a Docusaurus stránka.

## 🛠️ Ako pracovať

```bash
git pull                 # stiahni zmeny od ostatných v tíme
# ... uprav .md súbory ...
git add -A
git commit -m "Popis zmeny"
git push
```

Lokálny náhľad stránky (Docusaurus): `make dev` · prehľad príkazov: `make help`

## 🔗 Odkazy

- Šablóna predmetu: [06-STH-Projects/2026_sthdf_class_template](https://github.com/06-STH-Projects/2026_sthdf_class_template)
- [K000119 – Ako si vytvoriť čistý klon triedneho repozitára](https://knifes.systemthinking.sk/sk/knifes/K000119-klon-triedneho-repozitara)
- 🧭 Portál predmetu: [sthdf.systemthinking.sk](https://sthdf.systemthinking.sk)
- 📚 KNIFE dokumentácia: [knifes.systemthinking.sk](https://knifes.systemthinking.sk)

## License

- **Kód a skripty**: [MIT License](./LICENSE)
- **Vzdelávací obsah a dokumentácia** (`.md` súbory, metodiky, poznámky): [CC-BY 4.0 License](./LICENSE-DOCS)
