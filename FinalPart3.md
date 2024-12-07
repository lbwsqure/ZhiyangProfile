# Final Project: Fishing Analysis
This project focuses on analyzing fishing hotspots by using fish distribution data to uncover geographical patterns, seasonal trends. Through this data-driven approach, I aim to provide beginner anglers, nature enthusiasts, and casual learners with insights to optimize their fishing experiences. I took Walleye as an example, telling my audiences how to catch your first fish, there are definitely many things I didn't cover during my presentation, I didn't mention how to rent a rod, I made this assumption which I will definitely avoid in the future.

---

## Overview
### Goals:
1. **Leverage data** from public APIs to analyze fish species distribution
2. Develop interactive visualizations to help anglers:
   - Identify fishing hotspots.
   - Choose the most effective bait.
   - Understand how weather and time influence fishing success.
---

## Changes Since Part II
Based on feedback from Part II, I made the following changes to enhance the accessibility and value of my project:

### Audience-Focused Adjustments
1. **Added visual aids:**
   - Created visualizations like bite time analysis and bait recommendations.

2. **Improved technical depth:**
   - Integrated more data points, such as how water temperature and weather affect fish activity.
   - Enhanced interactivity by allowing map filters for seasonal trends.

3. **Balanced content for a broader audience:**
   - Included "top insights" like pairing baits with weather and bite-time strategies. Make sure everyone can understand my presentation.  

---

## Methodology
### Tools and Platforms:
1. **Data Fetching and Processing:**
   - Used the GBIF API to gather data on fish distribution and species occurrences.
   - Developed a Python script to process data into a custom dataset, including:
     - Fish species.
     - Geographical coordinates (latitude, longitude).
     - Observation times (year, month).

2. **Data Visualization:**
   - Built interactive maps and visualizations in Tableau.
   - Build Bitetime analysis and temperature comparasion using excel visualization. Exported the charts to png and include them in the   
   shorthand.  
   - Created visual stories using Shorthand to enhance narrative flow and audience engagement.

### Final Dataset:
The dataset includes:
- Fish species: **Bigmouth Bass, Smallmouth Bass, Rainbow Trout, Walleye, Catfish**.
- Geospatial data: **latitude, longitude, country**.
- Temporal data: **year, month**.
- Temperature data: I chose a specific day in Decemeber and compare the bite probability with temperature. This is a seperate dataset.

---

## User Research
### Target Audience:
1. **Beginner Anglers:** Need guidance on where and how to fish.
2. **Nature Enthusiasts:** Curious about fish species and distribution patterns.
3. **Casual Learners:** Interested in how data can provide insights.  

### Feedback Summary:
#### From Interviews (3 Participants):
1. **Beginner Accessibility:**
   - Request for visual aids like photos of fish and simplified bait recommendations. Thats why I included the fish I caught during summer 
   time.  
   - Interest in clear, actionable insights for beginners. I started from bait selection, and where is the fish(Walleye live in deep water 
   during daytime while come to shallow water to find food when they fell temperature drops down.)  
2. **Technical Depth:**
   - Advanced users appreciated maps and suggested seasonal trends.
3. **General Feedback:**
   - "Interactive tools like filters would improve engagement."
   - "Add bite-time analysis and connect it with weather conditions." Thats why I added two extra visualizations.

### Key Takeaways:
- Ensure clarity for beginners without overwhelming them with technical data.
- Balance actionable insights, engaging storytelling.

---

## Reflections
### Key Design Decisions:
1. **Visual Enhancements:**
   - Added bite-time analysis and bait-weather pairing visualizations to link data with actionable insights.
   - Focused on balancing visuals and text for better narrative flow.

2. **User Feedback Implementation:**
   - Included photos and simplified content to make the story accessible to beginners.

3. **Challenges:**
   - Collecting water temperature data, I selected few good day to catch walleye and get data from apple weather, type temperature data into 
   excel sheet to visualize it.  
   - Filtering and selecting actionable insights required balancing technical depth with audience needs.

### Lessons Learned:
- **Storytelling:** At first, you have to come up with something engaging to attract audiences, topic must be interesting or they will lose their attention.  
- **Technical Integration:** Combining Python, Tableau, Excel, and Shorthand allowed me to merge technical insights with storytelling tools.

---

## References
1. **Data Sources:**
   - GBIF API for fish distribution data. [GBIF API](https://www.gbif.org/developer/summary)  
   - Temperature data is from apple weather.  
   - Bitetime analysis data is from FishBrain app.  
   - Images are from unsplashed, in the shorthand they are tagged and well-referenced.  
   - Other images are photos took by myself.  
2. **Tools:**
   - Tableau, Excel for visualizations.
   - Shorthand for storytelling.
   - Python for data processing.

---

## Links:
1. **Shorthand Story:** [Start your Fishing Journey in the U.S.](https://preview.shorthand.com/OBOUmkTFhGY8A7yq)


