# Environmental Data Analytics Project *by Monisha Eadala*

Final project repository for Environmental Data Analytics (ENV 872L) at Duke University, Spring 2020

## Summary

This repository contains the the relevant datasets (all versions - raw and processed), different aspects and the progress of my final project right from its inception to completion (code segragated as per different stages - processing, wrangling, data exploration, data analysis, final output). This repository will aid in quality documentation, efficient data analysis, and future replication or improvisation plans. 

My goal is to study water quality with the help of the NTL-LTER Lake Datasets provided to me through the Environmental Data Analytics class taught at Nicholas School of the Environment in Spring 2020. The datasets contains the concentrations of key minerals/nutrients and physical attributes measured in various lakes of Wisconsin. 

Eutrophication is a phenamenon caused due to excess of nutrients in water and it causes structural changes to the ecosystem in the form of increased production of algae and aquatic plants, depletion of fish species, general deterioration of water quality and other effects that reduce and preclude use. Therefore, it is important to observe and manage lakes and their nutrient loading from time to time to conserve water and its dependent ecosystems. 

Through this project, I hope to understand the causes of eutrophication and the correlations between the measure of elements and nutrients contianed in the datasets. I intent to answer my research questions through data wrangling, processing, exploring, and visualization techniques taught in class using the Wisconsin Lakes as the sample.

## Investigators

**Monisha Eadala**, Graduate Student - Master of International Devlolpment Policy, Class of 2020, Sanford School of Public Policy, Duke University

For more information, please contact Monisha Eadala through *monisha.eadala@duke.edu*

## Keywords

Eutrophicatiom, Algal bloom, Lake, Wisconsin, Water quality, Nitrogen, Phosphoros, Oxygen, Carbon, Temperature, Irradiance

## Database information

The datasets in this repository contain data from studies on several lakes in the North Temperate Lakes District in Wisconsin, USA. Data were collected as part of the Long Term Ecological Research station established by the National Science Foundation. 

Data were collected from the North Temperate Lakes Long Term Ecological Research website. More information can be found here: https://lter.limnology.wisc.edu/about/overview. Data were collected using the Data tool (https://lter.limnology.wisc.edu/data).

From the Data homepage, the following were typed and searched: 
1. *Cascade Project at North Temperate Lakes LTER Core Data Carbon 1984 - 2016*
2. *Cascade Project at North Temperate Lakes LTER Core Data Physical and Chemical Limnology 1984 - 2016*
3. *Cascade Project at North Temperate Lakes LTER Core Data Nutrients 1991 - 2016*

Each of relevant files were downloaded through "Download All Data (csv)" button. 

## Folder structure, file formats, and naming conventions 

The folders contained in the reposity are: 
1. "Data" folder further subdivided into "Raw" and "Processed" folders that each contain their relevant csv files
2. "Code" folder that contains the three R markdown files - "Processing&Wrangling", "Data_exploration" and "Data_analysis" 
3. "Output" folder that contains the final project file in r markdown and PDF formats
4. "Other" folder will contain files that do not fit any of the above-mentioned categories

The files are either named as per their description of the data, or their function. For example, raw datasets in the initial stage are named "Raw", while any dataset that has departed from the raw dataset is named "Processed". The R markdown files stored in the 'Code' folder are named according to the stages of the analysis; for example, the code relevant to the processing and wrangling stages of the project are in the file named "Processions&Wranging" and the code relevant to the data exploration stage of the project is named "Data_exploration". The CSV files will be named according to their default name found in its source website, combined with important elements or column names that they contain and the type/stage of the data (whether raw or processed). 

## Metadata

There are three raw data filed in the repository:
1. 'NTL-LTER_Lake_Carbon_Raw.csv' file: This contains data relevant to dissolved organic and inorganic carbon, particulate organic matter, partial pressure of CO2 and absorbance at 440nm. Samples were collected with a Van Dorn sampler. Organic carbon and absorbance samples were collected from the epilimnion, metalimnion, and hypolimnion (upper, intermediate, and lower layers of the stratified lakes respectively). Inorganic samples were collected at depths corresponding to 100%, 50%, 25%, 10%, 5%, and 1% of surface irradiance, as well as one sample from the hypolimnion. Samples for the partial pressure of CO2 were collected from two meters above the lake surface (air) and just below the lake surface (water). Sampling frequency varies, and the number of site are 14. (As noted in https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-ntl.350.6)

This dataset contains the below column names and their relevant details:

Column Name        | Class    | Units   |Relevant Dataset Information
-------------------|----------|---------|----------------------------
lakeid             | factor   | -       | Provides the IDs of the lakes either in the form of capital letters or words; for example, L, R, T, E, Tbog, Roach, Ward, etc. 
lakename           | factor   | -       | Provides the names of the lakes; for example, Paul Lake, Peter Lake, Tuesday Lake, East Long Lake, etc.
year4              | integer  | -       | Provides the year in which its respective data was collected in four digits from 1984 to 2016
daynum             | integer  | -       | Provides the number of the day on which its data was collected from from 1 to 366
sampledate         | factor   | -       | Provides the date on which its data was collected in m/d/y format
depth              | factor   | m       | Provides the depth at which the data sample was collected in meters
depth_id           | integer  | -       | Provides the depth level categorizied from -2 to 7; 1 represents 100% light, 2 represents 50% light, 3 represents 25% light; 4 represents 10% light, 5 represents 5% light, 6 represents 1% light, 7 means Hypolimnion, -1 means Epilimnion/PML, and -2 means Metalimnion
tpc                | numeric  | mg/L    | Provides the total particulate carbon
tpn                | numeric  | mg/L    | Provides the total particulate nitrogen
DIC_mg             | numeric  | mg/L    | Provides the dissolved inorganic carbon measured in milligrams per liter
DIC_uM             | numeric  | uM/L    | Provides the dissolved inorganic carbon measured in micro-mole per liter
air_pco2           | numeric  | uatm    | Provides the partial pressure of CO2 (pCO2) is the amount of free CO2 in air
water_pco2         | numeric  | uatm    | Provides the partial pressure of aqueous CO2 (pCO2) is the amount of free CO2 in water
doc                | numeric  | mg/L    | Provided the dissolved organic carbon concentration
absorbance         | numeric  | Au      | Provides the measure of the capacity of the water to absorb light of a certain wavelength in absorbance units

2. 'NTL-LTER_Lake_ChemistryPhysics_Raw.csv' file: This contains data relevant to physical and chemical variables (such as temperature, dissolved oxygen, and irradiance) that are measured at one central station near the deepest point of each lake. In most cases these measurements are made in the morning (8 to 9 am). Vertical profiles are taken at varied depth intervals. Chemical measurements are sometimes made in a pooled mixed layer sample (PML); sometimes in the epilimnion, metalimnion, and hypolimnion; and sometimes in vertical profiles. In the latter case, depths for sampling usually correspond to the surface plus depths of 50%, 25%, 10%, 5% and 1% of surface irradiance. (As noted in https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-ntl.352.3)

This dataset contains the below column names and their relevant details:

Column Name       | Class     | Units   | Relevant Dataset Information
------------------|-----------|---------|-----------------------------
lakeid            | factor    | -       | Provides the IDs of the lakes either in the form of capital letters or words; for example, L, R, T, E, Tbog, Roach, Ward, etc. 
lakename          | factor    | -       | Provides the names of the lakes; for example, Paul Lake, Peter Lake, Tuesday Lake, East Long Lake, etc.
year4             | integer   | -       | Provides the year in which its respective data was collected in four digits from 1984 to 2016
daynum            | integer   | -       | Provides the number of the day on which its data was collected from from 1 to 366
sampledate        | factor    | -       | Provides the date on which its data was collected in m/d/y format
depth             | numeric   | m       | Provides the depth at which the data sample was collected in meters
temperature_C     | numeric   | C       | Provides the water temperature in celcius
dissolvedOxygen   | numeric   | mg/L    | Provides the dissolved oxygen measurement in milligrams per liter
irradiancewWater  | numeric   | uE      | Provides the photosynthetically active radiation measured in the water column in micro-Einstein 
irradianceDeck    | numeric   | uE      | Provies the photosynthetically active radiation measured on the deck of the sampling boat in micro-Einstein
comments          | factor    | -       | Provides the comments noting departure from standard procedure 

3. 'NTL-LTER_Lake_Nutrients_Raw.csv' file: This contains the data relevant to physical and chemical variables (such as total nitrogen, total phosphorius, ammonia and ammonium, nitrite and nitrate, and phosphate concentrations) that are measured at one central station near the deepest point of each lake. In most cases these measurements are made in the morning (8 to 9 am). Vertical profiles are taken at varied depth intervals. Chemical measurements are sometimes made in a pooled mixed layer sample (PML); sometimes in the epilimnion, metalimnion, and hypolimnion; and sometimes in vertical profiles. In the latter case, depths for sampling usually correspond to the surface plus depths of 50%, 25%, 10%, 5% and 1%t of surface irradiance. The 1991-1999 chemistry data was obtained from the Lachat auto-analyzer. Like the process data, there are up to seven samples per sampling date due to Van Dorn collections across a depth interval according to percent irradiance. Voichick and LeBouton (1994) describe the autoanalyzer procedures in detail. Nutrient samples were sent to the Cary Institute of Ecosystem Studies for analysis beginning in 2000. The Kjeldahl method for measuring nitrogen is not used at IES, and so measurements reported from 2000 onwards are Total Nitrogen. (As noted in https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-ntl.351.3)

This dataset contains the below column names and their relevant details:

Column Name        | Class    | Units   | Relevant Dataset Information
-------------------|----------|---------|-----------------------------
lakeid             | factor   | -       | Provides the IDs of the lakes either in the form of capital letters or words; for example, L, R, T, E, Tbog, Roach, Ward, etc. 
lakename           | factor   | -       | Provides the names of the lakes; for example, Paul Lake, Peter Lake, Tuesday Lake, East Long Lake, etc.
year4              | integer  | -       | Provides the year in which its respective data was collected in four digits from 1991 to 2016
daynum             | integer  | -       | Provides the number of the day on which its data was collected from from 1 to 366
sampledate         | factor   | -       | Provides the date on which its data was collected in m/d/y format
depth_id           | integer  | -       | Provides the depth level categorizied from -2 to 7; 1 represents 100% light, 2 represents 50% light, 3 represents 25% light; 4 represents 10% light, 5 represents 5% light, 6 represents 1% light, 7 means Hypolimnion, -1 means Epilimnion/PML, and -2 means Metalimnion
depth              | numeric  | m       | Provides the depth at which the data sample was collected in meters
tn_ug              | numeric  | ug/L    | Provides the total nitrogen concentration in micrograms per liter
tp_ug              | numeric  | ug/L    | Provides the total phosphorus concentration in micrograms per liter
nh34               | numeric  | ug/L    | Provides the ammonia and ammonium concentration in micrograms per liter
no23               | numeric  | ug/L    | Provides the nitrite and nitrate concentration in micrograms per liter
po4                | numeric  | ug/L    | Provides the phosphate concentration in micrograms per liter
comments           | factor   | -       | Provides any additional comments

## Scripts and code

Code will be included in three seperate R markdown files in the folder 'Code':
1. 'Processing&Wrangling.Rmd': Code relevant to any processing and wrangling required to be done on the Raw files will be included in this file
2. 'Data_exploration.Rmd': Code relevant to any data exploration before the main data analysis stage will be stored in this file
3. 'Data_analysis.Rmd': Code relevant to the main data analysis aspect of the project will be inluded here

## Quality assurance/quality control

This readme file provides for a quality assurance/control plan. All stages of the project will be stores in the form of R markdown  files and named according to the conventions highlighted under *Folder structure, file formats, and naming conventions* above. Any potential errors or problems I may run into with the data will be recorded under a separate document (PDF or R markdown) that will reside in the 'Other' folder of this respository. Also, changes made to any files will be pushed to the git repository on daily basis for quality check purposes.
