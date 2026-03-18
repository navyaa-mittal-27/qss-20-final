qss-20-final
A research project examining the relationship between ICE enforcement activity and human trafficking hotline signals across U.S. Areas of Responsibility (AORs).

Repository structure
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

Data
International
FileDescriptionCTDC_global_synthetic_data_v2025.csvEXPLANATIONISO_codes.csvEXPLANATIONIceRemovalData_PreviousYears.mdEXPLANATIONIceRemovalData_RecentYears.csvEXPLANATIONregression_data_output.csvEXPLANATION
National — Input
FileDescriptionICERemovalsdata.csvICE data giving removals by Area of Responsibility (AOR)ice-offices(Sheet1).csvICE field office data used to bridge between state-level hotline data and AOR-level ICE data
National — Output
FileDescriptionICEEROmanualdatacleancompleted.csvCleaned version of manualdatacleanneeded.csv after manually correcting cells to improve state-level merging (e.g. converting city names to state names)manualdatacleanneeded.csvOutput of IceAORcleaner.ipynb, flagged for manual cleaningtrafficking_states_master.csvOutput of Hotlinescraper.ipynb, containing Human Trafficking Hotline signals across states and years

Figures and tables
International
FileDescriptionmap.htmlEXPLANATIONnational_regressions.pngEXPLANATIONregional_regressions.pngEXPLANATIONsubregion_plot.pngEXPLANATION
National
FileDescriptionAORcoef.pdfAOR fixed effects coefficient plot, produced by ICE_Hotline_merge_and_model.ipynbAORremscatter.pdfScatterplot of ICE removals vs. hotline signals by AOR, produced by ICE_Hotline_merge_and_model.ipynbICESankey.pngSankey diagram of the national-level data pipeline, produced by Sankey.ipynbhotlinesignalsonICEremovalsLaTeX regression table of hotline signals on ICE removals, produced by ICE_Hotline_merge_and_model.ipynb

Scripts
International
ScriptDescriptionclean_merge_model.ipynbEXPLANATION
National
ScriptDescriptionHotlinescraper.ipynbScrapes state- and year-level data from the Human Trafficking Hotline websiteIceAORcleaner.ipynbCleans the original AOR field office dataset to produce a usable crosswalk between states and AORsICE_Hotline_merge_and_model.ipynbMerges ICE and hotline datasets using AOR crosswalk, runs regression models, and produces figuresSankey.ipynbBuilds a Sankey diagram visualizing the national-level data pipeline
