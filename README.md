# Netflix Data Analysis

> **Projeto de portfólio em Ciência de Dados** sobre catálogo, audiência e desempenho das ações da Netflix.

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-data%20analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![scikit--learn](https://img.shields.io/badge/scikit--learn-clustering-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

## Visão geral

Este projeto explora três perspectivas complementares do ecossistema Netflix: as características e avaliações do catálogo, a permanência de títulos no ranking diário dos Estados Unidos e o histórico de preços das ações. A análise combina estatística descritiva, visualização, correlação e agrupamento com **K-means** para transformar bases públicas em perguntas de negócio compreensíveis.

O repositório foi organizado para funcionar como um projeto de portfólio: os notebooks estão numerados em ordem de leitura, os dados brutos ficam isolados em `data/raw/` e a documentação explica como reproduzir a análise.

## Perguntas analisadas

| Pergunta | Abordagem | Evidência principal |
| --- | --- | --- |
| A duração dos filmes está associada à avaliação? | Correlação, gráficos de dispersão e K-means | A associação linear observada é fraca, portanto duração, isoladamente, não explica bem a nota. |
| Filmes antigos recebem avaliações maiores? | Comparação de médias, variâncias e correlação com o ano | Há diferença descritiva entre grupos, mas ela não deve ser interpretada como causalidade. |
| Audiência e preço da ação se movimentam juntos? | Alinhamento temporal, médias móveis, correlação e K-means | Existe associação moderada no recorte estudado, mas fatores externos também podem influenciar o preço. |

## Principais achados descritivos

Os dados utilizados contêm **5.850 títulos** no catálogo, **7.100 registros** do Top 10 diário e **5.044 observações** de mercado. O catálogo cobre lançamentos de 1945 a 2022; o ranking diário cobre abril de 2020 a março de 2022; e a série de ações começa em maio de 2002 e vai até junho de 2022.

No catálogo, há 3.744 filmes e 2.106 séries. Para os filmes com duração e avaliação disponíveis, a duração média é de aproximadamente 101 minutos e a nota média do IMDb é de aproximadamente 6,25. Esses valores são estatísticas descritivas da amostra, não estimativas atuais sobre a Netflix.

> **Nota metodológica:** correlação e agrupamento identificam padrões nos dados, mas não demonstram causalidade. A comparação com o preço da ação também não deve ser usada para recomendação financeira.

## Estrutura do repositório

```text
.
├── data/
│   └── raw/
│       ├── catalog.csv
│       ├── daily_top_10.csv
│       └── netflix_stocks.csv
├── docs/
│   └── DATA_DICTIONARY.md
├── notebooks/
│   ├── 01_analise_exploratoria.ipynb
│   └── 02_relatorio_final.ipynb
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Como executar

### 1. Clone o projeto

```bash
git clone https://github.com/Francelinojr/Analise-de-Dados_da_Netflix.git
cd Analise-de-Dados_da_Netflix
```

### 2. Crie um ambiente virtual

```bash
python -m venv .venv
# Linux/macOS
source .venv/bin/activate
# Windows PowerShell: .venv\Scripts\Activate.ps1
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Abra os notebooks

```bash
cd notebooks
jupyter notebook
```

Execute primeiro `01_analise_exploratoria.ipynb` e, em seguida, `02_relatorio_final.ipynb`. Os caminhos relativos já foram ajustados para que os notebooks encontrem os arquivos em `data/raw/`.

## Fontes dos dados

As bases foram obtidas de conjuntos públicos disponibilizados no Kaggle. Consulte o [dicionário de dados](docs/DATA_DICTIONARY.md) para conhecer as variáveis e as limitações de cada fonte.

## Colaboração

O projeto foi desenvolvido por **Francelino Teotonio Júnior**, em colaboração com **Ana Paula Cardoso de Castro Kendall** e **Vivianny Khatly Medeiros Pereira**. A organização atual prioriza clareza, reprodutibilidade e comunicação dos resultados.

## Licença

Este projeto é distribuído sob a licença MIT. Os direitos e termos das bases de terceiros permanecem sujeitos às respectivas fontes originais.

## Referências

[1] https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies?select=titles.csv "Netflix TV Shows and Movies"
[2] https://www.kaggle.com/datasets/prasertk/netflix-daily-top-10-in-us "Netflix Daily Top 10"
[3] https://www.kaggle.com/datasets/akpmpr/updated-netflix-stock-price-all-time "Netflix Stock Price — All Time"
