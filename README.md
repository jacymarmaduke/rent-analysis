# A Field Guide to Apartment Hunting in Germany

## About
This repository contains an in-depth analysis of the German apartment market, with a special focus on how local/regional population and apartment characteristics relate to the cost of rent. The analysis culminated in this Tableau storyboard: https://public.tableau.com/app/profile/jacquelyn.marmaduke/viz/GermanRentStoryboard/Germanrentstoryboard?publish=yes

## Objective
My overarching question: How can data help prospective renters find a good deal on a German apartment? Or put in a more analytical way: Which factors best predict an apartment's rent? I narrowed the wide pool of variables down to location, the rate of local (district) population growth and a shortlist of influential apartment characteristics. I also used k-means cluster analysis to determine the target rent for five different "personalities" of apartments, and I created a new "hidden gem" variable to judge an apartment's desirability relative to its rent.

## Data
A Kaggle user scraped over 250,000 residential rental listings from Immoscout24, Germany's top real estate website. The listings, scraped on four dates between 2018 and 2020, include extensive detail on each unit, from monthly rent and apartment size to telecom offers and text descriptions. The raw data is available [here](https://www.kaggle.com/datasets/corrieaar/apartment-rental-offers-in-germany).

I used two geoJSON files for mapping purposes. They're included in this repository and are also available [here](https://github.com/isellsoap/deutschlandGeoJSON/tree/main/4_kreise).

Data on state and district population and apartment stock is from Statistisches Bundesamt (the Federal Statistical Office of Germany). I used various datasets to create two population datasets tailored to this project, both of which are included in this repository. Raw data on a range of population and housing statistics is available [here](https://www-genesis.destatis.de/genesis/online?operation=themes&code=1#abreadcrumb).

## A note on reproducibility
The rent data files are too large to include in this repository. The raw data is linked above. To reproduce components of this project or conduct your own analysis, start with the raw data and run scripts 1 and 2 (you'll just need to update the file paths and download the population datasets in the 'cleaned data' folder). If you'd like to make your own maps with the accompanying geoJSON file, script 9 (section 02) contains code for updating the district names to match those in the geoJSON file.

## Contents
**rent project summary:** Contains additional information about the goals of this project and the data sources, including explanations of all variables.

**cleaned data:**

district_pop.csv: Contains each district's population and annual rate of change (percentage, averaged between 2018 and 2020). Source: Statistisches Bundesamt

med_district_rents.csv: Contains the median rent of each district. I edited the district names to match those in the geoJSON file.

median state rents.csv: Contains the median rent of each state. I edited the state names to match those in the geoJSON file.

state_pop.csv: Contains population and residential property statistics for each German state. Source: Statistisches Bundesamt

**geo data:**

2_hoch.geo.json: Contains location data for Germany's 16 states (Bundesländer). 

3_mittel.geo.json: Contains location data for 400 German districts (Kreise).

**scripts:** Contains 14 Jupyter notebooks where I carried out data cleaning, analysis, visualization and mapping. 
