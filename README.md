# Cluster hello

Bootstraps a synthetic GPP series and prints a 95% interval.

## Run
Rscript scripts/cluster_hello.R 200

## Files
scripts/  the analysis code
jobs/     Slurm job scripts
docs/     notes and templates

## Author
Merle Braun


tipps:
git add dateiname (fügt zum local ding hinzu)
git commit -m "commit message"
git push (fügt zum github hinzu)

git status (zeigt den aktuellen status der file an)
touch datei (zum erstellen)

## Block 4 – FLUXNET data summary

### Selected flux towers

- US-Prr – United States
- CH-Oe3 – Switzerland
- ES-LJu – Spain
- DK-Sor – Denmark
- JP-Hc3 – Japan

### Requirements

R and Quarto must be installed. The required R packages can be installed using:

```r
install.packages(c(
  "readr", "dplyr", "tidyr", "ggplot2",
  "knitr", "maps", "lubridate",
  "scales", "rmarkdown"
))
```

### Data

Place the five original FLUXNET ZIP files in `data/raw/`. The raw data are excluded from version control.

The metadata snapshot used for this analysis is:

`data/snapshots/fluxnet_shuttle_snapshot_20261119T174438.csv`

### Reproducing the report

Run the following command from the root directory of the repository:

```bash
quarto render reports/block4_data_summary.qmd
```

The rendered HTML report is generated at:

`reports/block4_data_summary.html`

The report includes site characteristics, data coverage, summary statistics, daily carbon flux time series, seasonal diurnal cycles and an energy balance analysis.