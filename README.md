# qss-20-final

Repository structure:

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

Data

International
- `CTDC_global_synthetic_data_v2025.csv` — Data on human trafficiking
- `ISO_codes.csv` — International country codes for merging
- `IceRemovalData_PreviousYears.md` — Data on deportations from early 2010s to early 2020s
- `IceRemovalData_RecentYears.csv` — Data on deportations from 2021 to 2025 (later dropped because of overlaps with previous file)
- `regression_data_output.csv` — Output of global regression data

National

Input:
- `ICERemovalsdata.csv` — ICE removals by Area of Responsibility
- `ice-offices(Sheet1).csv` — ICE field office locations, used to bridge state-level and AOR-level data

Output:
- `ICEEROmanualdatacleancompleted.csv` — Manually cleaned version of `manualdatacleanneeded.csv`
- `manualdatacleanneeded.csv` — Output of `IceAORcleaner.ipynb`, flagged for manual cleaning
- `trafficking_states_master.csv` — Human Trafficking Hotline signals by state and year

Figures and tables

International:
- `map.html` — Interactive map of deportations and human trafficking over the years
- `national_regressions.png` — Regression table on countries with the highest deportations / trafficking
- `regional_regressions.png` — Regression table on all sub-regions
- `subregion_plot.png` — Plots of human trafficking data and deportation data across regions

National:
- `AORcoef.pdf` — AOR fixed effects coefficient plot
- `AORremscatter.pdf` — Scatterplot of ICE removals vs. hotline signals
- `ICESankey.png` — Sankey diagram of the national data pipeline
- `hotlinesignalsonICEremovals` — LaTeX regression table

Scripts

International:
- `clean_merge_model.ipynb` — Data to install the data files, clean the data, merge, and build the regression models and visualizations

National:
- `Hotlinescraper.ipynb` — Scrapes Human Trafficking Hotline data by state and year
- `IceAORcleaner.ipynb` — Cleans AOR field office data into a state-AOR crosswalk
- `ICE_Hotline_merge_and_model.ipynb` — Merges datasets, runs models, produces figures
- `Sankey.ipynb` — Builds the national data pipeline Sankey diagram
