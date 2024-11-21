# Fishing Hotspots Analysis Project

## Outline

This project aims to analyze where to fish by leveraging data from public APIs and building a custom dataset tailored to my needs. By observing the geographical distribution and migration patterns of various fish species over the past three years, I aim to uncover insights into the movements and hotspots for fishing.

The key objectives of this project include:
- Fetching and processing fish species distribution data using Python APIs.
- Analyzing migration patterns for selected fish species over the last few years.
- Presenting results in a clear and interactive format for storytelling and data visualization.
---

## Sketches


## Data
I created my own dataset which is geographical location of certain fish species.  
The data for this project is sourced from the [GBIF API](https://www.gbif.org/developer/summary), which provides open access to biodiversity data, including species occurrences, distributions, and metadata. For this project, the API was queried to retrieve distribution data for five fish species:
- **Bigmouth Bass (Micropterus salmoides)**
- **Smallmouth Bass (Micropterus dolomieu)**
- **Rainbow Trout (Oncorhynchus mykiss)**
- **Walleye (Sander vitreus)**
- **Catfish (Ictalurus punctatus)**

The dataset includes geospatial coordinates (latitude and longitude), time of observation (year and month), and additional metadata such as the country of the record, the dataset source, and the basis of the record (e.g., observation, specimen).

My dataset is here:  


Change parameters down here you can create your own dataset! 
```python
# This is a Python code block
import requests
import pandas as pd
import datetime

species_scientific_names = [
    "Micropterus salmoides",  # Bigmouth Bass
    "Micropterus dolomieu",  # Smallmouth Bass
    "Oncorhynchus mykiss",   # Rainbow Trout
    "Sander vitreus",        # Walleye
    "Ictalurus punctatus"    # Catfish
]

current_year = datetime.datetime.now().year

years = [current_year - i for i in range(3)]

occurrence_search_url = "https://api.gbif.org/v1/occurrence/search"
def get_occurrences_by_scientific_name_and_month(scientific_name, year, month):
    params = {
        "scientificName": scientific_name,
        "limit": 50,          
        "hasCoordinate": "true", 
        "year": year,         
        "month": month         
    }
    response = requests.get(occurrence_search_url, params=params)
    if response.status_code == 200:
        return response.json().get("results", [])
    return []

all_monthly_data = []

for scientific_name in species_scientific_names:
    for year in years:
        for month in range(1, 13):  
            occurrences = get_occurrences_by_scientific_name_and_month(scientific_name, year, month)
            for record in occurrences:
                all_monthly_data.append({
                    "Scientific Name": scientific_name,
                    "Year": year,
                    "Month": month,
                    "Latitude": record.get("decimalLatitude"),
                    "Longitude": record.get("decimalLongitude"),
                    "Country": record.get("country"),
                    "Basis of Record": record.get("basisOfRecord"),
                    "Dataset": record.get("datasetKey")
                })

df_monthly = pd.DataFrame(all_monthly_data)
```

## Method and Medium
 - 1. [Shorthand](https://shorthand.com/)
 - 2. Tableau (For data visualizaiton)
 - 3. Python (For data fetching from the internet)
      
