# 🏅 Olympics Data Lake

Data Lake local com dados históricos dos Jogos Olímpicos (1896–2024).

## Objetivo

Consolidar o quadro de medalhas olímpicas por país, com separação entre
Jogos de Verão e Jogos de Inverno, a partir de fontes públicas.

## Fontes

| Arquivo | Fonte | Período |
|---------|-------|---------|
| `olympics_historico.csv` | Base dos Dados / Olympedia | 1896–2022 |
| `olympics_paris2024.csv` | Kaggle — Paris 2024 | 2024 |

## Estrutura

```
olympics-datalake/
├── README.md
├── metadata_schema.json
├── raw/                        # Dados brutos originais
│   ├── olympics_historico.csv
│   ├── olympics_historico.json
│   ├── olympics_paris2024.csv
│   └── olympics_paris2024.json
├── bronze/                     # Dados padronizados e integrados
│   ├── olympics_historico.parquet
│   ├── olympics_paris2024.parquet
│   ├── medalhas_1896_2024.csv
│   ├── medalhas_1896_2024.parquet
│   └── medalhas_1896_2024.json
└── gold/
    └── analise_medalhas/       # Quadro final + gráficos
        ├── medalhas_summary.csv
        ├── medalhas_verao.csv
        ├── medalhas_inverno.csv
        ├── medalhas_total.csv
        ├── top50_verao.png
        ├── top50_inverno.png
        ├── top50_total.png
        └── metadata.json
```

## Pipeline

```
raw/ (CSV brutos)
  └─► bronze/ (padronização + Parquet + JOIN entre fontes)
        └─► gold/ (agregação final + visualizações)
```

## Aluno

Daniel Nazário Oliveira de Souza — Sistemas de Informação, UEA
Professor: Luis Cueves Rodriguez
