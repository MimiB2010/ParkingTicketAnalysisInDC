# Analysis of Parking Tickets in Washington, DC

Our team was interested in getting an insight to parking tickets issued in the District due to personal experiences with Parking. We used  five years' parking violation data (2014 to 2018) from OpenData.DC.gov to visualy represent the trends and information we were able to extract from the data. 

Questions:
Where do parking violations occur in the District?
When do parking violations occur in the District?
What are some general trends concerning parking violations in the District?
Can we predict how much money the DC government can collect in 2019?
Is parking in different areas of the District enforced disproportionately?

Analysis: 

We utilized Jupyter Notebook and modules such as pandas, Gmaps, Glob, os, numpy, matplotlib.pyplot, datetime, and dateutil to extract, read, clean, and visualize the data.

Findings: 

1. 2018 Heat Map 
![Heat map](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/2018_Heat_Map_Zoomed_Out.png)

Heat Map (large view) shows all of the heatmap data for 2018, including pockets in Anacostia, Friendship Heights, and Tenleytown.

![Heat map zoomed](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/2018_Heat_Map_Zoomed_In.png)

More zoomed in heatmap of downtown that shows specific ‘hot spots’ like the H street corridor, M street, Georgetown, Navy Yard, and near major landmarks. Research in budget information from DC Public Works (which encompasses Parking Enforcement) showed a commitment to hiring Full-Time Equivalents (employees) specifically to monitor the 20 busiest streets in DC which may account for fewer violations happening outside of the downtown areas we see here.

2. 2018 Parking Trends by Hour of Day

![tickets by hour of day](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/tickets_by_hour_18.png)

This graph does not include around 20% of the data which does not have a valid timestamp. In comparing with data from Fiscal Year 2017, there was something that changed in the data collection process which caused a much higher percentage of values without a valid time stamp. We recognized the issue when the chart showed a peak between midnight and 1AM which did not make sense. Because we were missing data points from 2 AM to 10 AM, we chose to represent the data from 10AM until 2 AM.

3. 2018 Parking Trends by Day of Week

![Trends by Day of Week](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/tickets_by_dayofweek_18.png)

The most popular days are Wednesdays and Thursdays. We suspected that this may be in part due to teleworking schedules or holidays on Mondays skewing the numbers down.

4. 2018 Parking Trends by Month

![Violations by Month](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/tickets_by_month_18.png)

We see spikes in August and October, both warmer weather months. August’s spike may be attributed to the school year starting, with schools being back in sessions and college students moving in to the many universities in the district.

5. 2018 Violations by State

![Violations by State](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/TopDMV.png)

State plates that showed DC, MD, & VA had the largest number of violations, which is to be expected.
Vehicles with Maryland plates had the largest number of violations, with DC second and you Virginia third.

6. DMV Violations by State Plate - Heat Map

![DMV Violations Heat Map](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/dmv_plates_heatmap_18.png)

With DC, Maryland & Virginia being the largest offenders, we wanted to see where the majority of tickets were being given for these states. Similar to the 2018 Heat Map, most of the 'hot spots' are Downtown, H Street Corridor, etc.; however, we did see many tickets given around the border between DC & MD. We think this is a good portion of the violations that make up the Maryland state plate violation count. 

7. Violations by State Plate - Not in DMV

![Violations by State Plate - Not in DMV](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/Top10DMV.png)

Even though DC, MD, & VA had the largest number of violations, we wanted to know which states, outside of the DMV, had the most violations (top 10)
Pennsylvania plates had the largest number of violations followed by Florida.
California plates were the last group in the top 10; however, with the distance between CA & DC being so large, we expected the number of violations for CA to be lower. We discussed that the tickets to TX and CA plates could be going to people moving into the area for jobs, knowing that both of those states have robust job markets.

8. Trend by year

![Trend by year](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/Five%20Year%20trend%20by%20Month.png)

The graph showed a general decrease in the number of tickets issued with exception of 2016. We believe that major events such as election-year related events that took place in 2016 contributed to the spike in total tickets issued. 

The downward trend in parking violations is consistent with [an article](https://wtop.com/dc-transit/2019/02/d-c-parking-ticket-revenue-declining/) we found on Washington’s Top news that showed parking ticket and towing revenue has been on decline for about a decade. 

9. Sample month to month comparisons

![Sample month to month comparisons](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/MOM%20Total%20Tcikets.png)

The sample months comparison was consistent with the general trend we saw in the five year graph. There was a spike in ticket issued in 2016 for the months we sampled.

10. 2018 Parking violation by type

![2018 Parking violation by type](https://github.com/MimiB2010/TeamMiriamProject1/blob/master/Output/2018%20Violation_Type.png)

After cleaning and the data and lumping in similar violation descriptions together we were able to find 19 categories. The top 3 violation types for 2018 were 
      1. Expired or unpaid meter
      2. Fail to display meter receipt 
      3. No parking


Limitation:

- Lacked budget data to see revenue from parking fines - WTOP had 2 articles, [one](https://wtop.com/dc-transit/2019/02/d-c-parking-ticket-revenue-declining/) of which referenced the data but did not include a source,  and the [other](https://wtop.com/dc/2018/09/aaa-fewer-and-fewer-parking-tickets-are-getting-issued-around-dc/) said the data was accessible through a Freedom Of Information Act (FOIA)  request
- Unsure of cause of tickets without a recorded time stamp
- Not able to translate all state abbreviations (“MM”, “XX”, ‘YY”) to a state
- Could not translate coordinates to zip codes to compare against census data

Further questions

- Fiscal year vs. calendar year
- Adjudicated tickets
- Repeat offenders 
