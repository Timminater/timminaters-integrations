# Timminater's Home Assistant integrations

Deze repository is de centrale ontwikkelmap en catalogus voor mijn Home Assistant-
integraties. Iedere integratie staat onder `integrations/` als een volledig zelfstandige
repositorystructuur, zodat deze afzonderlijk voor HACS gepubliceerd kan worden.

## Integraties

| Integratie | Status | Providers | Broncode |
|---|---|---|---|
| Neerslag Radar | 0.1.0, experimenteel | Buienradar, Buienalarm, KNMI en Open-Meteo | [Open map](integrations/neerslag-radar/) |

## Repository-indeling

```text
timminaters-integrations/
├── README.md
└── integrations/
    └── neerslag-radar/
        ├── custom_components/neerslag_radar/
        ├── tests/
        ├── hacs.json
        └── README.md
```

De hoofdrepository bewaart alle integraties en hun geschiedenis. Voor publicatie als
zelfstandige HACS-repository kan een integratiemap met Git subtree worden gesplitst:

```shell
git subtree split --prefix integrations/neerslag-radar -b release/neerslag-radar
git push neerslag-radar release/neerslag-radar:main
```

De remote `neerslag-radar` moet daarbij verwijzen naar de afzonderlijke GitHub-
repository voor die integratie. Hierdoor blijft deze catalogus compleet, terwijl iedere
HACS-repository de vereiste integratiebestanden op het repository-rootniveau heeft.
