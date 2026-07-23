# Timminater's Home Assistant integrations

Een catalogus met custom integraties voor Home Assistant. Elke integratie heeft een
eigen GitHub-repository en kan afzonderlijk via HACS worden geïnstalleerd.

## Beschikbare integraties

### Neerslag Radar

Neerslagverwachtingen voor een ingestelde locatie, afkomstig van Buienradar,
Buienalarm, KNMI en Open-Meteo. De integratie bevat daarnaast een Global-prognose
die per tijdslot de hoogste waarde van de geconfigureerde providers gebruikt.

| Eigenschap | Waarde |
|---|---|
| Versie | [![Nieuwste release](https://img.shields.io/github/v/release/Timminater/neerslag-radar?label=nieuwste%20versie)](https://github.com/Timminater/neerslag-radar/releases/latest) (experimenteel) |
| Home Assistant | 2026.6 of nieuwer |
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

Een compacte Lovelace-kaart die de neerslagverwachtingen van Buienradar,
Buienalarm, KNMI en Open-Meteo als afzonderlijke blauwe lijnen vergelijkt. De
kaart gebruikt automatisch de locaties en providers van Neerslag Radar en laat
de berekende Global-prognose weg.

| Eigenschap | Waarde |
|---|---|
| Versie | [![Nieuwste release](https://img.shields.io/github/v/release/Timminater/neerslag-radar-card?label=nieuwste%20versie)](https://github.com/Timminater/neerslag-radar-card/releases/latest) |
| Vereist | Neerslag Radar 0.3.0 of nieuwer |
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
|-- neerslag-radar/ -> https://github.com/Timminater/neerslag-radar
`-- neerslag-radar-card/ -> https://github.com/Timminater/neerslag-radar-card
```

## Problemen en bijdragen

Open een issue of pull request in de repository van de betreffende integratie. Voor
Neerslag Radar kan dat via
[Timminater/neerslag-radar](https://github.com/Timminater/neerslag-radar) en voor
de kaart via
[Timminater/neerslag-radar-card](https://github.com/Timminater/neerslag-radar-card).
