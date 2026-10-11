# Natural State take-home: birds and vegetation

Two challenges, each solved in one Quarto document (R code and explanation together) with a short Markdown summary for reading.

## Where to look

| If you want to | Open |
|---|---|
| Read the results in five minutes | [`reports/birds_report.md`](reports/birds_report.md) and [`reports/vegetation_qaqc_report.md`](reports/vegetation_qaqc_report.md) |
| See the full tables, the interactive map and the code folded under each step | `scripts/quarto/birds_analysis.html` and `scripts/quarto/vegetation_qaqc.html` (download and open in a browser) |
| Read or run the code | `scripts/quarto/birds_analysis.qmd` and `scripts/quarto/vegetation_qaqc.qmd` |
| Use the outputs | `output/birds/` (labelled predictions, per-species thresholds) and `output/vegetation/herb_qaqc_flags.csv` (every QA/QC flag) |

## Layout

```
docs/       task brief, the two vegetation SOPs, Wood & Kahl (2024)
input/      the data as provided; nothing here is modified
scripts/    one .qmd per challenge, its rendered .html
output/     tables written by the scripts
reports/    markdown summaries and their figures
```

## Running it

R 4.5 and Quarto, with the packages tidyverse, janitor, here, sf, leaflet, vegan and DT. Paths are resolved with `here::i_am()`, so the documents render from any working directory:

```
quarto render scripts/quarto/birds_analysis.qmd
quarto render scripts/quarto/vegetation_qaqc.qmd
```

Rendering also rewrites the files in `output/`.
