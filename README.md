# qss-20-final

A research project examining the relationship between ICE enforcement activity and human trafficking hotline signals across U.S. Areas of Responsibility (AORs).

---

## Repository structure

```
qss-20-final/
├── data/
│   ├── international/
│   └── national/
│       ├── input/
│       └── output/
├── figures_and_tables/
│   ├── international/
│   └── national/
└── scripts/
    ├── international/
    └── national/
```

---

## Data

### International

| File | Description |
|------|-------------|
| `CTDC_global_synthetic_data_v2025.csv` | EXPLANATION |
| `ISO_codes.csv` | EXPLANATION |
| `IceRemovalData_PreviousYears.md` | EXPLANATION |
| `IceRemovalData_RecentYears.csv` | EXPLANATION |
| `regression_data_output.csv` | EXPLANATION |

### National — Input

| File | Description |
|------|-------------|
| `ICERemovalsdata.csv` | ICE data giving removals by Area of Responsibility (AOR) |
| `ice-offices(Sheet1).csv` | ICE field office data used to bridge between state-level hotline data and AOR-level ICE data |

### National — Output

| File | Description |
|------|-------------|
| `ICEEROmanualdatacleancompleted.csv` | Cleaned version of `manualdatacleanneeded.csv` after manually correcting cells to improve state-level merging (e.g. converting city names to state names) |
| `manualdatacleanneeded.csv` | Output of `IceAORcleaner.ipynb`, flagged for manual cleaning |
| `trafficking_states_master.csv` | Output of `Hotlinescraper.ipynb`, containing Human Trafficking Hotline signals across states and years |

---

## Figures and tables

### International

| File | Description |
|------|-------------|
| `map.html` | EXPLANATION |
| `national_regressions.png` | EXPLANATION |
| `regional_regressions.png` | EXPLANATION |
| `subregion_plot.png` | EXPLANATION |

### National

| File | Description |
|------|-------------|
| `AORcoef.pdf` | AOR fixed effects coefficient plot, produced by `ICE_Hotline_merge_and_model.ipynb` |
| `AORremscatter.pdf` | Scatterplot of ICE removals vs. hotline signals by AOR, produced by `ICE_Hotline_merge_and_model.ipynb` |
| `ICESankey.png` | Sankey diagram of the national-level data pipeline, produced by `Sankey.ipynb` |
| `hotlinesignalsonICEremovals` | LaTeX regression table of hotline signals on ICE removals, produced by `ICE_Hotline_merge_and_model.ipynb` |

---

## Scripts

### International

| Script | Description |
|--------|-------------|
| `clean_merge_model.ipynb` | EXPLANATION |

### National

| Script | Description |
|--------|-------------|
| `Hotlinescraper.ipynb` | Scrapes state- and year-level data from the Human Trafficking Hotline website |
| `IceAORcleaner.ipynb` | Cleans the original AOR field office dataset to produce a usable crosswalk between states and AORs |
| `ICE_Hotline_merge_and_model.ipynb` | Merges ICE and hotline datasets using AOR crosswalk, runs regression models, and produces figures |
| `Sankey.ipynb` | Builds a Sankey diagram visualizing the national-level data pipeline |
