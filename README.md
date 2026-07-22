# Timminater's Home Assistant integrations

Deze repository is de centrale catalogus voor mijn Home Assistant-integraties. Iedere
integratie is gekoppeld als Git-submodule en wordt ontwikkeld, getest en gepubliceerd
vanuit een eigen primaire repository.

## Integraties

| Integratie | Status | Providers | Broncode |
|---|---|---|---|
| Neerslag Radar | 0.1.0, experimenteel | Buienradar, Buienalarm, KNMI en Open-Meteo | [Broncode](https://github.com/Timminater/neerslag-radar) |

## Repository-indeling

```text
timminaters-integrations/
├── README.md
├── .gitmodules
└── neerslag-radar/ → https://github.com/Timminater/neerslag-radar
```

## Catalogus clonen

```shell
git clone --recurse-submodules https://github.com/Timminater/timminaters-integrations.git
```

Na een clone zonder submodules kunnen ze alsnog worden opgehaald met:

```shell
git submodule update --init --recursive
```

## Integraties bijwerken

Wijzigingen worden eerst gecommit en gepusht in de primaire integratierepository. Werk
daarna de verwijzing in deze catalogus bij en commit de gewijzigde submodulepointer:

```shell
git submodule update --remote neerslag-radar
git add neerslag-radar
git commit -m "Update Neerslag Radar"
```

Neerslag Radar kan rechtstreeks als custom HACS-repository worden toegevoegd via
`https://github.com/Timminater/neerslag-radar` met type **Integration**.
