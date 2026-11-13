# Netflix Content Strategy: Exploratory Data Analysis

Python EDA of the Netflix catalogue (8,807 movies and TV shows, mid-2021) to answer: **what type of content should Netflix produce, and how can it grow in different countries?**

**Notebook:** [`Netflix_Case_Study.ipynb`](Netflix_Case_Study.ipynb) (runs on Google Colab, outputs included)

## Key findings
- Movies outnumber TV Shows about 70/30 (6,131 vs 2,676), but in 2021 releases TV Shows (315) overtook Movies (277).
- International Movies and International TV Shows are the top genres; the US, India and the UK supply the most titles.
- TV-MA and TV-14 are the most common ratings: the catalogue skews mature/teen.
- Additions peaked in 2019; July and December are the busiest months, February the quietest.

## What the notebook does
Unnests multi-value columns (director, cast, country, genre) with `split` + `explode`, merges them back on title, removes duplicates, treats missing values (documented assumptions), builds date features, then charts type, rating, country, release year, genre, additions per year/month, and top actors/directors, ending with business insights, recommendations and limitations.

## Run it
**Google Colab:** File > Upload notebook, run all cells, upload `data/netflix.csv` when asked.
**Locally:** `pip install -r requirements.txt` then `jupyter notebook Netflix_Case_Study.ipynb`

## Structure
```
.
├── Netflix_Case_Study.ipynb
├── data/netflix.csv
├── images/
├── requirements.txt
└── README.md
```

## Limitations
The data shows what is available, not what is watched (no viewership or revenue data). Missing countries (~6%) were assumed to be the United States. Genre and country counts overlap because titles carry several tags. 2021 is a partial year.
