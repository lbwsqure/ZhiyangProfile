# Fishing Hotspots Analysis Project

## Outline

This project aims to analyze where to fish by leveraging data from public APIs and building a custom dataset tailored to my needs. By observing the geographical distribution and migration patterns of various fish species over the past three years, I aim to uncover insights into the movements and hotspots for fishing.

The key objectives of this project include:
- Fetching and processing fish species distribution data using Python APIs.
- Analyzing migration patterns for selected fish species over the last few years.
- Presenting results in a clear and interactive format for storytelling and data visualization.
---

## Sketches
<div class='tableauPlaceholder' id='viz1732155173034' style='position: relative'>
    <noscript>
        <a href='#'>
            <img alt='Sheet 1' src='https://public.tableau.com/static/images/Fi/FishDistribution/Sheet1/1_rss.png' style='border: none' />
        </a>
    </noscript>
    <object class='tableauViz' style='display:none;'>
        <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' />
        <param name='embed_code_version' value='3' />
        <param name='site_root' value='' />
        <param name='name' value='FishDistribution/Sheet1' />
        <param name='tabs' value='no' />
        <param name='toolbar' value='yes' />
        <param name='static_image' value='https://public.tableau.com/static/images/Fi/FishDistribution/Sheet1/1.png' />
        <param name='animate_transition' value='yes' />
        <param name='display_static_image' value='yes' />
        <param name='display_spinner' value='yes' />
        <param name='display_overlay' value='yes' />
        <param name='display_count' value='yes' />
        <param name='language' value='en-US' />
        <param name='filter' value='publish=yes' />
    </object>
</div>
<script type='text/javascript'>
    var divElement = document.getElementById('viz1732155173034');
    var vizElement = divElement.getElementsByTagName('object')[0];
    vizElement.style.width = '100%';
    vizElement.style.height = (divElement.offsetWidth * 0.75) + 'px';
    var scriptElement = document.createElement('script');
    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
    vizElement.parentNode.insertBefore(scriptElement, vizElement);
</script>


## Data
I created my own dataset which is geographical location of certain fish species.  
The data for this project is sourced from the [GBIF API](https://www.gbif.org/developer/summary), which provides open access to biodiversity data, including species occurrences, distributions, and metadata. For this project, the API was queried to retrieve distribution data for five fish species:
- **Bigmouth Bass (Micropterus salmoides)**
- **Smallmouth Bass (Micropterus dolomieu)**
- **Rainbow Trout (Oncorhynchus mykiss)**
- **Walleye (Sander vitreus)**
- **Catfish (Ictalurus punctatus)**

The dataset includes geospatial coordinates (latitude and longitude), time of observation (year and month).
 - **I will try add some temperature data in the future.**

My dataset is here:  
[Download Dataset](./fishmonthly.csv)  

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
      
