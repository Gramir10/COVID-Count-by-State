# COVID-Count-by-State
Calculating the Death Count per 1000 Cases of COVID-19

This project is focused on cleaning data sets and editing FIPS data to create county unique identifier codes to allow merging of several data sets. The data sets merged include population statisics, hospital infrastructure statisics, and COVID-19 cases/fatalities.

This is all done in an effort to identify which places in the US require more resources, this project highlights key data that can be used as metrics to find which locations may be vulnerable (as in the cases of the bubble_u18_o60 charts) or that are suffering from increased mortality rates (as in the bubble_deaths charts).

# What was conserved
Geographic Areas, Total populations, Population statisics over 60 and under 18, ratios of prior variables.

# Data Analysis: Pinpointing the affected population
 </br>
 
 We note that Charlotte County, FL has a large proportion of over 60 population (49.6%) so quarantine measures should be strictly enforced in that area. The area highest in need of assistence was Nassau County, NY, where of 21.5 thousand cases, 890 have resulted in fatalities, which is a rate of 41.4 deaths per 1000 cases. The county only has 4,343 hospital beds and requires significant assistance. 2nd on the list is Wayne County, MI, where 10.5 thousand cases has resulted in 609 deaths, a rate of 57.8 deaths per 1000. There are 6,079 beds. This indicates that higher hospital bed capacity may not be what keeps people from dying. The correlation heatmap indicates a low-medium correlation between the two variables. Further study should be conducted between these two locations, but possible explainations could be number of trained medical professionals, availablity of ventilators, or possibily a more severe strain of the virus. A conclusion was not possible from current data sources.
 
 What should be highlighted is that if one where to draw line from zero, to the Nassau County data point (furthest up and right) any data points below that line are suffering higher mortality rates, and any data points above that have lower mortality rates. This offers two groups to study to find correlations of why the mortality rates are so different.
 
#bar_total_pop
![alt text](https://github.com/Gramir10/COVID-Death-Count/blob/master/bar_total_pop.png)
 </br>
 Top 20 most populous US counties

#bubble_u18_o60
![alt text](https://github.com/Gramir10/COVID-Death-Count/blob/master/bubble_u18_o60.png)
 </br>
Identifies counties with large proportions of Over 60 or Under 18 populations, thus vulernable populations.

#bubble_u18_o60_beds
![alt text](https://github.com/Gramir10/COVID-Death-Count/blob/master/bubble_u18_o60_beds.png)
 </br>
Previous graph, standardized per 1000 hospital beds.

#county_covid19_heatmap
![alt text](https://github.com/Gramir10/COVID-Death-Count/blob/master/county_covid19_heatmapv2.png)
 </br>
Notes the correlations between several variables.

#bubble_deaths
![alt text](https://github.com/Gramir10/COVID-Death-Count/blob/master/bubble_deaths.png)
 </br>
This graphic keeps track of number of cases, deaths, the size of the bubbles dictate the number of deaths per 1000 cases. Addititional information keeps track of which counties and size of their hospital capacity (in beds) is.

# Edits/Repairs of the Data
Unneccessary columns of data was editted out (such as Margins of Error).
Beds, Name, Deaths_x, and Cases_x were renamed to hospital_bed_count, hospital_count, Death_count, and Number_of_cases respectfully for clarification of purpose.
per1000 variables were calculated based on variables being divided by total population in census tract, multiplied by 1000.
Some variables were converted from objects, to integers, to floating numbers for calculations.
</br>

# Conclusion
Further research should look into differences between counties where low mortality rates exist and high mortality rates. Some areas with less hospital capacity are dealing better than ones with smaller populations and more capacity. Counties can be tracked over time using this project to determine where emergency resources should be allocated. There is little difference in the correlation between mortality rates of the two vulnerable populations, as such both must be monitored with equal importance.

# Data Sources
(Johns Hopkins University Center for Systems Science and Engineering!https://github.com/CSSEGISandData/COVID-19)
This data set lists global counts of COVID-19 cases, deaths, recovered patients as reported by county.
(New York Times!https://github.com/nytimes/covid-19-data)
This data set is similar to the JHU CSSE COVID-19 US county-specific data but works for graphing purposes.
(American Community Survey!https://data.census.gov/cedsci/table?q=United%20States&g=0100000US,.050000&tid=ACSST5Y2018.S0101&hidePreview=false&vintage=2018&layer=VT_2018_050_00_PY_D1&cid=DP05_0001E&t=Populations%20and%20People)
This data set (also available in the GitHub repository here) gives us in-depth reporting for US county-level population in 2018.
(US Census!https://www.census.gov/geographies/reference-files/2018/demo/popest/2018-fips.html)
These data sets from the US Census give us geographic information (FIPS codes) for US states and counties, which allows the data from all sources to be merged by location.
(Homeland Infrastructure Foundation-Level!https://hifld-geoplatform.opendata.arcgis.com/datasets/hospitals)
Where we retrieved hospital beds data.

