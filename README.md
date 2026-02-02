**Green Supply Chain Analysis: Western Europe
An End-to-End Project on Sustainability & Logistics Reliability**

**Why this project exists**
In modern logistics, there is a constant tug-of-war between speed and sustainability. I wanted to see if I could identify specific patterns where our shipping methods were unnecessarily high-carbon without actually improving delivery times.

By focusing on the Western Europe market, I analyzed over 27,000 rows of data to build a model that flags "wasteful" shipments and suggests greener alternatives.

**How I built it**
**1. Data Wrangling & Engineering (Python)**
The raw data was messy—dealing with specific encoding issues and unnecessary columns. I used Pandas to:

Filter the dataset down to the Western European region.

Standardize shipping modes (First Class, Second Class, Standard, and Same Day).

The Carbon Model: Since the dataset didn't have a "CO2" column, I engineered a custom metric. I assigned carbon weights to different transport methods and multiplied them by sales volume to estimate the environmental footprint of every single order.

**2. Geospatial Intelligence**
Using Folium, I mapped out the coordinates of these shipments. This allowed me to see "High-Carbon Hotspots"—areas where we are pumping out the most emissions. It’s one thing to see a number in a spreadsheet; it’s another to see a giant red bubble over a city on a map.

**3. Business Intelligence (Power BI)**
I moved the cleaned data into Power BI to create an executive-level dashboard. My goal was to make the data "clickable." You can filter by country to see:

Total Carbon Impact: Which regions are the "heaviest" emitters.

Late Delivery Risk: Are our greenest routes also our slowest? (Usually, the answer is no, which is a huge win for the business).

**Key Insights & Recommendations**
The "Low Hanging Fruit": I identified 4,107 orders that were shipped via high-emission methods but arrived late anyway. By shifting these to rail or consolidated ground shipping, we could reduce carbon impact by ~15% without affecting the customer experience.

Risk Mitigation: The data showed that certain cities in France and Germany have higher "Late Risk" scores regardless of the shipping mode, suggesting infrastructure issues rather than carrier issues.

**📁 What’s in this Repo?**
Green_Supply_Chain_Analysis.ipynb: My full Python workflow (Data cleaning -> Modeling -> Geospatial).

Green_Logistics_Dashboard.pbix: The interactive dashboard file.

Optimized_Green_Supply_Chain.csv: The final "Engineered" data.

supply_chain_map.html: The standalone interactive map.

**How to use this**
To see the interactive map, simply download the .html file and open it in any browser. To explore the data logic, check out the Jupyter Notebook.
