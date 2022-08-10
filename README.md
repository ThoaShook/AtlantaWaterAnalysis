# AtlantaWaterAnalysis
### I. Introduction:

A superior quality of water is crucial to the health and social well- being of the people.
Water analysis,based on social vulnerability index, helps to identify regions and groups of vulnerable people that tend to receive inadequate water in terms of quality and quantity supplied.
In this notebook, we'll analyze water quality based on the social vulnerability index. Our datasets at hand contains underprivileged groups of people, water distribution, and the quality of water based on Gerogia geographical region. We get some insights into the water vulnerability index by
   * Identifying the counties that are most vulnerable in terms of Scocio-economic Status
   * Identifying water sources, locations where water are located and their distribution to Atlanta Region
   * Visualizing the effects of water distribution and contamination over the past 5 years.

###### Terminologies
*  SVI  - Social Vulnerability Index. 
What is svi? SVI uses US. Census data to help local officials identify communities that may need support during natural disasters. SVI is categorical into four themes based on   
     * Socioeconomic status (below poverty, unemployed, income, no high school diploma)
     * Household composition & disability (aged 65 or older, aged 17 or younger, older than age 5 with a disability, single-parent households)
     * Minority status & language (minority, speak English “less than well”)
     * Housing type & transportation (multi-unit structures, mobile homes, crowding, no vehicle, group quarters)

###### Calculation Method:
* Rankings:
     * Percentile Rank = (Rank-1)/(N-1) 
          * N = total number of data point
          * Percentile ranking values range from 0-1
          * Higher percentile ranking indicates greater vulnerability
* References:                            
1. https://svi.cdc.gov/A%20Social%20Vulnerability%20Index%20for%20Disaster%20Management.pdf#:%7E:text=A%20Social%20Vulnerability%20Index%20for%20Disaster%20Management%201,loss%20estimates%20for%20buildings%20and%20infrastructure”%20%28FEMA%202009a%29
   
2. https://atlantaregional.org/atlanta-region/about-the-atlanta-region

### A. Identify relationship between SVI variables


![](Images/svi_Corr.png)


* The scale bar ranks from -1 to 1, with 1(darkgreen)is the strongest postive relationship and -1 (darkred) is the most negative relationship, and 0 indicates no relationship at all. White color bar on the graph indicates no data is available
* There're some strong correlation between no high school diploma and minority status,poverty and minority, no high school diploma and the number of household unit, strong negative relationship between the age of 65 with per capita income. For example, the relationship between poverty and unemployment is absolutely high with the correlation coef of 0.99 (the pop-up on the graph) 

### B. Identify SVI per theme in Atlanta Region


![](Images/svi_AtlantaRegion.png)



* Vulnerability index ranking from 0 -1, with 1 is the most vulnerable and 0 is the least vulnerable
* Clayton ran high all four categories even though its population isn't that high indicate population isn't correlation with socioeconomic status


### C. SVI Ranking In Atlanta Region


![](Images/svi_Ranking.png)



* Clayton is the county that has the highest vulnerability index on THREE THEMES and FINAL RANKING THEMEM. Surprisingly Fulton - County that houses Atlanta City - is the most vulnerable county in term of HOUSING TYPE & TRANSPORTATION
* Clayton, Gwinnett, and DeKalb have highest vulnerability index in term of MINORITY and LANGUAGES, Fulton, Rockdale, and Cobb slightly trail behind. Minority groups are likely to reside in counties with big cities 
* Douglas, Rockdale, and Henry are the second - after Clayton in term of HOUSEHOLD COMPOSITION and DISABILITY, althought the index ~ 0.4
* Rockdale also sits second - after Clayton - in term of POVERTY and SCOCIAL ECONOMICAL STATUS
* DeKalb County is the SECOND highest vulnerability index in ALL THEMES




### D. Quantify Public Supply Ground Water & Surface Water in Atlanta Region



![](Images/G_S_WaterSupply.png)



* Atlanta regional water supply systems supplied mostly surface-water (lakes, rivers, streams..) for its citizens
* Fulton is the county with highest use of surface-water compare to ground water, which is comprehensible. It's housing Atlanta City and city area with highest population in the region
* From the map location above, Fayette and Rockdale are rural counties, their use of ground water is almost 2/3 of surface-water


### E. Quantify Public Water Supply to Domestic



![](Images/WaterSupply_Domestic.png)



### F. Quantify Water Use Per Capita



![](Images/WaterUsePerCapita.png)



* Interesting findings! Clayton and DeKalb are the two most vulnerable counties in term of socio-economic vulnerability, but they are the least received public water supply.



### G. Identify the locations of Ground Water in Atlanta Region


![](Images/GroudWaterDistribution.png)


* There are a total of 412 wells locate across Atlanta Region, mostly in Cobb, Fulton and DeKalb County




### H. Idendtify Water Supply In 2015



![](Images/watersupply2015.png)



* Ground Water didn't show up because the data values are relative very small (ratio: 1/20000) compare to other columns values, normalize data wouldn't reflect its true values
* DeKalb and Gwinnett County doesn't have 2015 data for ground and surface water
* Fulton received high water volumns due to its population, Capital City, and its geographical location



### I. Ground Water Withdrawals In 2015



![](Images/2015GroundWaterWithdrawals.png)



* There are no ground water data for both Cobb and DeKalb County
* Cherokee, Fayette, Henry, and Gwinnett County are the most using ground water. These are rural areas, it could be used for household or for plantation purposes



### J. Water Use Per Capita In 2015



![](Images/2015WaterPerCapita.png)



* Clayton, DeKalb, and Gwinnett have a very low number of water use per capita/person/gal/day.
* These counties also have high vulnerability index in term of socioeconomic status.


### K. Water Contaminants



![](Images/WaterContaminants.png)



* HAA6Br, HAA5, and HAA9 are the three contaminants that frequently present in the water, followed by anatoxin-a, cylindrospermopsin, total microcystin, manganese, germanium, 1-butanol, and 2-methoxyethanol



### L. Water Type


![](Images/WaterType.png)



* Majority of the water supply for Atlanta Regional Area is Surface Water (SW). This finding is inlight with previous findings. Ground Water (GW) and other type (MX) are singificantly small. 
