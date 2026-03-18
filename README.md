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
- `CTDC_global_synthetic_data_v2025.csv` — EXPLANATION
- `ISO_codes.csv` — EXPLANATION
- `IceRemovalData_PreviousYears.md` — EXPLANATION
- `IceRemovalData_RecentYears.csv` — EXPLANATION
- `regression_data_output.csv` — EXPLANATION

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
- `map.html` — EXPLANATION
- `national_regressions.png` — EXPLANATION
- `regional_regressions.png` — EXPLANATION
- `subregion_plot.png` — EXPLANATION

National:
- `AORcoef.pdf` — AOR fixed effects coefficient plot
- `AORremscatter.pdf` — Scatterplot of ICE removals vs. hotline signals
- `ICESankey.png` — Sankey diagram of the national data pipeline
- `hotlinesignalsonICEremovals` — LaTeX regression table

Scripts

International:
- `clean_merge_model.ipynb` — EXPLANATION

National:
- `Hotlinescraper.ipynb` — Scrapes Human Trafficking Hotline data by state and year
- `IceAORcleaner.ipynb` — Cleans AOR field office data into a state-AOR crosswalk
- `ICE_Hotline_merge_and_model.ipynb` — Merges datasets, runs models, produces figures
- `Sankey.ipynb` — Builds the national data pipeline Sankey diagram
