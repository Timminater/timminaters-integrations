# Timminater's Home Assistant integrations

Een catalogus met custom integraties voor Home Assistant. Elke integratie heeft een
eigen GitHub-repository en kan afzonderlijk via HACS worden geïnstalleerd. Bij elke
integratie staat een HACS-knop die de repository rechtstreeks in HACS opent.

## Beschikbare integraties

### CampChef BBQ Grills

[![Open in HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Timminater&repository=campchef&category=integration)

Cloudintegratie voor Camp Chef-wifigrills met grillstatus, temperatuur en
vleessondes. De beschikbare bediening hangt af van het grillmodel.
Bij opnieuw aanmelden vraagt Home Assistant een nieuwe pincode per e-mail aan.

| Eigenschap | Waarde |
|---|---|
| Versie | [1.0.1](https://github.com/Timminater/campchef/tree/cb34d3f69f8f71d0176fbb4cc6ccbe8c0d5153b1) |
| Repository | [Timminater/campchef](https://github.com/Timminater/campchef) |
| Installatie | Custom HACS-repository, categorie **Integration** |

Zie de [installatiehandleiding](https://github.com/Timminater/campchef#installation).

### HouseHeating Modbus

[![Open in HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Timminater&repository=househeating-modbus&category=integration)

Experimentele Modbus-integratie voor de HouseHeating HH-C3-12-warmtepomp,
met energie- en rendementsmonitoring, compressorstatistieken, thermostaat,
warmwaterboiler, registerbrowser en een optionele stooklijn. Versie 0.11.0
voegt 567 uitleessensoren toe die je per stuk kunt inschakelen via de
registerbrowser of de apparatenpagina. De integratie gebruikt de gedeelde
Modbus-verbinding van Home Assistant.

| Eigenschap | Waarde |
|---|---|
| Versie | [0.11.0](https://github.com/Timminater/househeating-modbus/releases/tag/v0.11.0) (experimenteel) |
| Home Assistant | 2026.10.1 of nieuwer |
| Repository | [Timminater/househeating-modbus](https://github.com/Timminater/househeating-modbus) |
| Installatie | Custom HACS-repository, categorie **Integration** |

Voeg de repository als aangepaste integratierepository toe aan HACS, installeer
**HouseHeating Modbus** en herstart Home Assistant. Voeg de integratie toe via
**Instellingen > Apparaten & diensten**. Begin met alleen uitlezen en volg de
[installatiehandleiding](https://github.com/Timminater/househeating-modbus#readme)
voor verificatie van de temperatuurschalen en het vrijgeven van bediening.

### Grundfos ALPHA2 GO

[![Open in HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Timminater&repository=grundfos-alpha2-go&category=integration)

Lokale Bluetooth-integratie voor de Grundfos ALPHA2 GO-circulatiepomp via een
actieve ESPHome Bluetooth-proxy. Leest onder meer debiet, opvoerhoogte, toerental
en vermogen uit. Optionele bediening omvat regelmodi, setpoints, debietbegrenzers,
AutoNight, werkpunt en start/stop.

| Eigenschap | Waarde |
|---|---|
| Versie | `0.3.0-dev.3` (ontwikkelversie, nog niet getest op de ALPHA2 GO K 25-75) |
| Home Assistant | 2026.11.0 of nieuwer |
| Repository | [Timminater/grundfos-alpha2-go](https://github.com/Timminater/grundfos-alpha2-go) |
| Installatie | Custom HACS-repository, categorie **Integration** |

Volg de [installatiehandleiding](https://github.com/Timminater/grundfos-alpha2-go#readme)
voor installatie en Bluetooth-koppeling. De integratie start in uitleesmodus.

### Neerslag Radar

[![Open in HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Timminater&repository=neerslag-radar&category=integration)

Neerslagverwachtingen voor een ingestelde locatie, afkomstig van Buienradar,
Buienalarm, KNMI en Open-Meteo. De integratie bevat daarnaast een Global-prognose
die per tijdslot de hoogste waarde van de geconfigureerde providers gebruikt.

| Eigenschap | Waarde |
|---|---|
| Versie | [![Nieuwste release](https://img.shields.io/github/v/release/Timminater/neerslag-radar?label=nieuwste%20versie)](https://github.com/Timminater/neerslag-radar/releases/latest) (experimenteel) |
| Home Assistant | 2026.6.0 of nieuwer |
| Repository | [Timminater/neerslag-radar](https://github.com/Timminater/neerslag-radar) |
| Installatie | Custom HACS-repository, categorie **Integration** |

#### Installeren via HACS

1. Open HACS in Home Assistant.
2. Ga naar **Integrations**.
3. Open het menu rechtsboven en kies **Custom repositories**.
4. Voeg `https://github.com/Timminater/neerslag-radar` toe met categorie
   **Integration**.
5. Zoek naar **Neerslag Radar** en installeer de integratie.
6. Herstart Home Assistant en voeg **Neerslag Radar** toe via
   **Instellingen > Apparaten & diensten**.

Raadpleeg voor configuratie, providers en bekende beperkingen de
[README van Neerslag Radar](https://github.com/Timminater/neerslag-radar#readme).

### Neerslag Radar Card

[![Open in HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Timminater&repository=neerslag-radar-card&category=plugin)

Een compacte Lovelace-kaart die de neerslagverwachtingen van Buienradar,
Buienalarm, KNMI en Open-Meteo als afzonderlijke blauwe lijnen vergelijkt. De
kaart gebruikt automatisch de locaties en providers van Neerslag Radar en laat
de berekende Global-prognose weg.

| Eigenschap | Waarde |
|---|---|
| Versie | [![Nieuwste release](https://img.shields.io/github/v/release/Timminater/neerslag-radar-card?label=nieuwste%20versie)](https://github.com/Timminater/neerslag-radar-card/releases/latest) |
| Vereist | Home Assistant 2026.6.0 en Neerslag Radar 0.3.0 of nieuwer |
| Repository | [Timminater/neerslag-radar-card](https://github.com/Timminater/neerslag-radar-card) |
| Installatie | Custom HACS-repository, categorie **Dashboard** |

#### Kaart installeren via HACS

1. Installeer en configureer eerst **Neerslag Radar** zoals hierboven beschreven.
2. Open HACS en kies rechtsboven **Custom repositories**.
3. Voeg `https://github.com/Timminater/neerslag-radar-card` toe met categorie
   **Dashboard**.
4. Zoek naar **Neerslag Radar Card** en installeer de kaart.
5. Vernieuw de browser en voeg de kaart via de visuele dashboardeditor toe.

Bij één Neerslag Radar-locatie selecteert de kaart deze automatisch. Bij meerdere
locaties verschijnt een keuzelijst in de kaarteditor.

### Energieprijs Voorspelling Card

[![Open in HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=Timminater&repository=Energieprijs_voorspelling_card&category=plugin)

Eén grafiek met de vaste Zonneplan day-ahead-uurtarieven (volle balken) en de
uurprognose van Stroomvoorspeller (gearceerde balken met bandbreedte), inclusief
overzichtsvakjes en een zoeker voor het goedkoopste aaneengesloten blok van N uur.

| Eigenschap | Waarde |
|---|---|
| Versie | [![Nieuwste release](https://img.shields.io/github/v/release/Timminater/Energieprijs_voorspelling_card?label=nieuwste%20versie)](https://github.com/Timminater/Energieprijs_voorspelling_card/releases/latest) |
| Home Assistant | 2024.6.0 of nieuwer |
| Vereist | Zonneplan-integratie. De voorspelling is optioneel via één REST-sensor. |
| Repository | [Timminater/Energieprijs_voorspelling_card](https://github.com/Timminater/Energieprijs_voorspelling_card) |
| Installatie | Custom HACS-repository, categorie **Dashboard** |

#### Kaart installeren via HACS

1. Open HACS en kies rechtsboven **Custom repositories**.
2. Voeg `https://github.com/Timminater/Energieprijs_voorspelling_card` toe met
   categorie **Dashboard**.
3. Zoek naar **Zonneplan Prijskaart** en installeer de kaart.
4. Zorg voor de twee sensoren: de tariefsensor van de HACS-integratie
   **Zonneplan** en (optioneel) de Stroomvoorspeller-uurprognose via één REST-sensor
   op `https://stroomvoorspeller.nl/data/forecast.json`; een klaar-om-te-kopiëren
   `rest.yaml`-voorbeeld staat in de repository.
5. Vernieuw de browser en voeg de kaart via de visuele dashboardeditor toe.

Zie de [README van de kaart](https://github.com/Timminater/Energieprijs_voorspelling_card#readme)
voor alle opties en het gegevenscontract.

## Over deze catalogus

De mappen in deze repository zijn Git-submodules die verwijzen naar de primaire
repository van iedere integratie. Releases, broncode, probleemmeldingen en
HACS-installaties worden vanuit die afzonderlijke repositories beheerd. Deze
catalogus zelf moet daarom niet als custom HACS-repository worden toegevoegd.

Bezoekers die alleen een integratie willen installeren, hoeven deze repository niet
te clonen.

### Clonen voor ontwikkeling

Clone de catalogus inclusief alle integraties met:

```shell
git clone --recurse-submodules https://github.com/Timminater/timminaters-integrations.git
```

Zijn de submodules bij het clonen overgeslagen, haal ze dan alsnog op met:

```shell
git submodule update --init --recursive
```

De huidige indeling is:

```text
timminaters-integrations/
|-- README.md
|-- .gitmodules
|-- campchef/ -> https://github.com/Timminater/campchef
|-- househeating-modbus/ -> https://github.com/Timminater/househeating-modbus
|-- grundfos-alpha2-go/ -> https://github.com/Timminater/grundfos-alpha2-go
|-- neerslag-radar/ -> https://github.com/Timminater/neerslag-radar
|-- neerslag-radar-card/ -> https://github.com/Timminater/neerslag-radar-card
`-- energieprijs-voorspelling-card/ -> https://github.com/Timminater/Energieprijs_voorspelling_card
```

## Problemen en bijdragen

Open een issue of pull request in de repository van de betreffende integratie:

- CampChef BBQ Grills: [Timminater/campchef](https://github.com/Timminater/campchef)
- HouseHeating Modbus: [Timminater/househeating-modbus](https://github.com/Timminater/househeating-modbus)
- Grundfos ALPHA2 GO: [Timminater/grundfos-alpha2-go](https://github.com/Timminater/grundfos-alpha2-go)
- Neerslag Radar: [Timminater/neerslag-radar](https://github.com/Timminater/neerslag-radar)
- Neerslag Radar Card: [Timminater/neerslag-radar-card](https://github.com/Timminater/neerslag-radar-card)
- Energieprijs Voorspelling Card: [Timminater/Energieprijs_voorspelling_card](https://github.com/Timminater/Energieprijs_voorspelling_card)
