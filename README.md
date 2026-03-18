# qss-20-final

Data:
    International:
        --CTDC_global_synthetic_data_v2025.csv --> EXPLAINATION
        --ISO_codes.csv --> EXPLAINATION
        --IceRemovalData_PreviousYears.md --> EXPLAINATION
        --IceRemovalData_RecentYears.csv --> EXPLAINATION
        --regression_data_output.csv --> EXPLAINATION
    National:
        Input:
            --ICERemovalsdata.csv --> ICE Data giving removals by Area of responsibility
            --ice-offices(Sheet1).csv --> ICE Data about feild offices for the purpose of merging between state-level hotline data and AOR-level ICE data
        Output:
            --ICEEROmanualdatacleancompleted.csv --> Data from manualdatacleanneeded.csv after manually cleaning some cells to better merge them by state (i.e. converting city names to state names.)
            --manualdatacleanneeded.csv --> Output from IceAORcleaner.ipynb, with some cleaning needed
            --trafficking_states_master.csv --> Output from Hotlinescraper, containing Human Trafficking Hotline information across states and years

figures_and_tables:
    international:
        --map.html --> EXPLAINATION
        --national_regressions.png --> EXPLAINATION
        --regional_regressions.png --> EXPLAINATION
        --subregion_plot.png --> EXPLAINATION
    national:
        --AORcoef.pdf --> Image produced by ICE_Hotline_merge_and_model.ipynb, which presents the AOR coefficents in our regression model
        --AORremscatter.pdf --> Image produced by ICE_Hotline_merge_and_model.ipynb, which presents the removals vs. hotline signals scatterplot of our data
        --ICESankey.png --> Image produced by Sankey.ipynb, which presents the Sankey diagram of the national-level data
        --hotlinesignalsonICEremovals --> LaTeX code produced by ICE_Hotline_merge_and_model.ipynb, which is the regression table results

Scripts:
    international:
        --clean_merge_model.ipynb --> PLEASE ADD
    national:
        --Hotlinescraper.ipynb --> Scraping state and year levels from the Human trafficking hotline website
        --ICE_Hotline_merge_and_model.ipynb --> Merging ICE and hotline datasets using AOR information and developing models and images
        --IceAORcleaner.ipynb --> Cleaning the origional AOR office information dataset to make it useful as a bridge
        --Sankey.ipynb --> Developing a sankey diagram for our dataset
        
