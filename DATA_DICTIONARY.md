# Dicionário de dados

## `data/raw/catalog.csv`

| Campo | Descrição |
| --- | --- |
| `id` | Identificador do título. |
| `title` | Nome do filme ou série. |
| `type` | Tipo do conteúdo: filme ou série. |
| `release_year` | Ano de lançamento. |
| `runtime` | Duração em minutos para filmes. |
| `genres` | Gêneros associados ao título. |
| `age_certification` | Classificação indicativa, quando disponível. |
| `seasons` | Número de temporadas para séries, quando disponível. |
| `imdb_score` | Nota do IMDb. |
| `imdb_votes` | Quantidade de votos no IMDb. |
| `tmdb_popularity` | Métrica de popularidade do TMDB. |
| `tmdb_score` | Nota do TMDB. |

## `data/raw/daily_top_10.csv`

| Campo | Descrição |
| --- | --- |
| `As of` | Data de referência do ranking. |
| `Rank` | Posição do título no Top 10. |
| `Year to Date Rank` | Posição acumulada no ano. |
| `Last Week Rank` | Posição registrada na semana anterior. |
| `Title` | Nome do título. |
| `Type` | Tipo de conteúdo. |
| `Netflix Exclusive` | Indicador de exclusividade, quando disponível. |
| `Netflix Release Date` | Data de lançamento na Netflix. |
| `Days In Top 10` | Quantidade de dias no Top 10. |
| `Viewership Score` | Pontuação de audiência da base. |

## `data/raw/netflix_stocks.csv`

| Campo | Descrição |
| --- | --- |
| `Date` | Data de negociação. |
| `Open`, `High`, `Low`, `Close` | Preços de abertura, máxima, mínima e fechamento. |
| `Adj Close` | Preço de fechamento ajustado. |
| `Volume` | Volume negociado. |

## Cuidados de interpretação

As bases têm origens, granularidades e períodos diferentes. O notebook final restringe e alinha os períodos necessários antes de comparar audiência e preço. Valores ausentes são tratados de acordo com a variável e o objetivo da análise; não se deve interpretar ausência como zero.
