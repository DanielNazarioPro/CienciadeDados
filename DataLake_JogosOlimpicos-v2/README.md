# 🏅 Olympics Data Lake (1896–2024)

Data Lake local com **6 datasets** cobrindo os Jogos Olímpicos de 1896 a 2024.

## Fontes

| Dataset | Fonte | Período |
|---------|-------|---------|
| `hist_athlete_bio` | Base dos Dados / Olympedia | 1896–2022 |
| `hist_athlete_event_result` | Base dos Dados / Olympedia | 1896–2022 |
| `hist_game_medal_tally` | Base dos Dados / Olympedia | 1896–2022 |
| `paris2024_athletes` | Kaggle — Paris 2024 | 2024 |
| `paris2024_events` | Kaggle — Paris 2024 | 2024 |
| `paris2024_medals_total` | Kaggle — Paris 2024 | 2024 |

## Estrutura

```
olympics-datalake/
├── README.md
├── metadata_schema.json
├── raw/                             # CSVs brutos + metadados JSON
├── bronze/                          # Parquet padronizados + JOINs
│   ├── medalhas_1896_2024           # UNION histórico + Paris 2024
│   ├── resultados_enriquecidos      # Resultados + bio dos atletas
│   └── atletas_paris2024_eventos    # Atletas Paris + catálogo de eventos
└── gold/
    ├── analise_medalhas/            # Quadro final + gráficos Top 50
    ├── analise_atletas/
    ├── analise_modalidades/         # Top modalidades Paris 2024
    └── analise_genero/              # Distribuição por gênero
```

## Pipeline

```
raw/ (CSV brutos + JSON)  →  bronze/ (Parquet + JOINs)  →  gold/ (análises + gráficos)
```

## Aluno

Daniel Nazário Oliveira de Souza — Sistemas de Informação, UEA  
Professor: Luis Cueves Rodriguez
