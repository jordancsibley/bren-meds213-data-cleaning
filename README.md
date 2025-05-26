# Cleaning the shorebird survey data 


## The data set

ARCTIC SHOREBIRD DEMOGRAPHICS NETWORK [https://doi.org/10.18739/A2222R68W](https://doi.org/10.18739/A2222R68W)

Data set hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository 

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

See `01_ASDN_Readme.txt` provided in the [course data repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-spring-2024-class-data) for full metadata information about this data set.


## Data & File Overview 

### File list 
The data used in this project is located in the folder `data/` is broken down into two subfolders: `raw/` and `processed/`. Here is the organization of these folders, along with a brief description of the file: 

```
data
|
├── raw/   # raw data files and metadata 
│    ├── 01_ASDN_Readme.txt  # README file for Arctic shorebird demographics network
│    ├── ASDN_Daily_species.csv  # species presence data file
│    └── ASDN_Snow_survey.csv  # snow survey data file 
│
├── processed/  # processed data files
│    ├── all_cover_fixed_SIBLEY.csv  # data file containing the cleaned version of ASDN_Snow_survey.csv
│    ├── snow_cover.csv  # data file with just the column Snow_cover cleaned of ASDN_Snow_survey.csv  
└──  └── species_presence.csv  # data file containing the cleaned version of ASDN_Daily_species.csv
```

### Additional data

There are many other related data files included in the [Arctic shorebird demographics network](https://arcticdata.io/catalog/view/doi:10.18739/A2222R68W) that are not included in this repository. Each data file is available on the ASDN page at the NSF Arctic Data Center (https://arcticdata.io) and is a .csv file with prefix "ASDN_"):

- Bird_captures
- Bird_eggs
- Bird_nests
- Bird_resights
- Bird_sexes
- Camp_info
- Camp_staff
- Daily_pred_lemm
- Daily_species
- Daily_species_effort
- Geodata
- Invert_biomass
- Lemming_counts
- Lemming_nests
- Lemming_trap
- Pred_nests
- Pred_point_counts
- Snow_survey
- Study_Plot	(KMZ file)
- Surface_water
- Weather_HOBO
- Weather_precip_manual
- Weather_snow_manual

### Other versions 

The data in the repository is a subset of the original dataset and was provided for the course [EDS 213 - Databases and Data Management](https://ucsb-library-research-data-services.github.io/bren-eds213/) to practice data cleaning and database querying.

## Data-specific information 

Here is more information relating to the data file data/processed/all_cover_fixed_SIBLEY.csv : 

**Number of variables**: 11

| Variable name | Description                                                | Unit(s) / Value type |
|---------------|------------------------------------------------------------|----------------------|
| Site          | Four-letter code of site at which data were collected      | string               |
| Year          | Year in which data were collected                          | integer              |
| Date          | Date on which data were collected                          | date                 |
| Plot          | Name of study plot on which survey was conducted           | string               |
| Location      | Name of dedicated snow-survey location, if applicable      | string               |
| Snow_cover    | Percent cover of snow, including slush                     | integer              |
| Water_cover   | Percent cover of water                                     | integer              |
| Land_cover    | Percent cover of exposed land                              | integer              |
| Total_cover   | Sum of the three cover columns - they should sum to 100%.  | integer              |
| Observer      | Person who conducted the survey                            | string               |
| Notes         | Any relevant comments on the survey                        | string              |


**Number of rows:** 42,829 

**Missing data codes**: NA

*Note*: Based on the methods of data cleaning, a `NA` value was given to any row where the column `Total_cover` did not equal 100 


## Sharing & Access Information 

### Licenses 

Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.

### Publications that cite this dataset 

https://onlinelibrary.wiley.com/doi/10.1111/gcb.17356
https://link.springer.com/article/10.1007/s10646-023-02708-w
[Additional publications listed here](https://arcticdata.io/catalog/view/doi:10.18739/A2222R68W)

### Data Access 

Data set hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository 

The original `ASDN_Snow_Survey.csv` can be found in the [bred-meds213-data-cleaning repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-data-cleaning/tree/main/data/raw), a repository for the EDS 213 course at the Bren School of Environmental Science and Management. This is a subset of the dataset hosted by the [NSF Arctic Data Center](https://arcticdata.io).

### Citation 

**The ASDN metadata encourages citing the project in this way**: 

Please acknowledge this dataset and the authors in any analysis, publication, presentation, or other output that uses these data. If you use the full dataset, we suggest you cite it as:

Lanctot, RB, SC Brown, and BK Sandercock. 2016. Arctic Shorebird Demographics Network. NSF Arctic Data Center. doi: INSERT HERE.

If you use data from only one or a few sites, we suggest you cite data for each site as per this example, using the corresponding site PIs as the authors:

Lanctot, RB and ST Saalfeld. 2016. Barrow, 2014. Arctic Shorebird Demographics Network. NSF Arctic Data Center. doi: INSERT HERE.

Note that each updated version of the full dataset has its own unique DOI.

