# Analyzing Uganda HIV service delivery data funded by U.S. agencies in Python and R and visualizing with Ggplot and Illustrator: [Story](https://annikamcginnis.github.io/uganda-hiv-usaid/)

## Goal
- To understand trends in HIV service delivery by U.S. funder and geographic area in Uganda, specifically to understand the impact of the dismantling of USAID on overall HIV service delivery in the country
- To explore utilizing statistical regressions in analysis to understand if USAID targeted more vulnerable groups than other U.S. PEPFAR funders
- To explore developing more creative data visualizations in Adobe Illustrator

## Main Findings
- In the last quarter before the Trump Administration came to power, USAID supplied funding for about 40 percent of Uganda’s core care and treatment services for people living with HIV. That money enabled over 550,000 patients to access antiretroviral (ARV) services, the daily medication people with HIV take to suppress the virus.
- Subcounties with antiretroviral funding from USAID, in comparison to subcounties funded by the other U.S. agencies, were already associated with a higher percentage of the population that accesses HIV treatment. This reveals that USAID tends to support areas that have fewer HIV clinics, where people from outside the subcounties travel to access treatment. It’s these same areas where the majority of clinics have now closed, increasing the burden on the few remaining centers.
- In comparison to subcounties with prevention services funded by the CDC or DOD, subcounties funded by USAID were also more likely to reach a higher percentage of the subcounties’ populations with prevention services. This, again, could show USAID’s targeting of areas with fewer HIV clinics that provide these services - which now have even fewer.
- National prevalence rates declined from about 18-30 percent at the height of the epidemic to just 5 percent in recent years.
- Before its dismantling, USAID led in funding programs that targeted communities with consistently higher levels of HIV, including fisherfolk and other mobile populations, sex workers, drug users, gay men and transgender people.
- Compared to the other U.S. agencies, USAID also used to fund a majority of services for drug users, including people who inject drugs.
- USAID was also key in PEPFAR’s efforts to prevent the spread of HIV, including distribution of condoms, community education campaigns, and supplies of medicine that prevents individuals from contracting the virus before and after exposure.
- USAID supplies HIV prevention medicine to major rural areas in northern, eastern and southwestern Uganda.


## Data Collection
I sourced data on HIV service delivery funded by the U.S. Agency for International Development (USAID), the Centers for Disease Control and Prevention (CDC) and Department of Defense (DOD) from the Uganda Partner-in-Country Reporting System, a national-level HIV data system funded by PEPFAR and managed by PEPFAR implementing partners. The data was available for each clinic reached by various PEPFAR-funded interventions for the quarter October-December, 2024: the final quarter of data reporting before the Trump administration assumed office. The data was provided by a staff member who asked for anonymity to protect their job. Data was provided for antiretroviral care and treatment for people living with HIV, prevention and care services for Priority Populations, and PREP (pre-exposure prophylaxis) medication provided by sub-group. 

I divided clinics into subcounties to aggregate subcounty-level data. I then merged in population data from the Uganda 2014 census available on the Uganda Board of Statistics on a subcounty level (available in the [regional parish-level datasets](https://www.ubos.org/explore-statistics/20/)). Because some subcounties had changed names, I manually merged in the populations for about a third of the data (over 700 subcounties). Since the more recent 2024 census data is not yet public at a subcounty level, but the overall [report](https://www.ubos.org/wp-content/uploads/2024/12/National-Population-and-Housing-Census-2024-Final-Report-Volume-1-Main.pdf) shows the population expanded by about 3% since 2014, I increased the 2014 subcounty population data by 3%. This is not meant to be a precise measurement but provides an estimate of the population differences between subcounties. 

I also sourced data on historical HIV and new infection rates in Uganda from UNAIDS. This data was published on the [World Bank data platform](https://data.worldbank.org/indicator/SH.DYN.AIDS.ZS?locations=UG) and the [Aidsinfo data map](https://aidsinfo.unaids.org/) run by UNAIDS, UNICEF and the World Health Organization.

Subcounty shapefiles were available for 2020 and downloaded from the Humanitarian Data Exchange, sourced from Uganda Bureau of Statistics.


## Data Analysis
I used the following languages, libraries, and applications in my data cleaning, analysis and visualization: 
- Python
- Pandas
- R
- ggplot
- TidyVerse
- DescTools
- Google Sheets
- ai2html
- Adobe Illustrator
- Datawrapper
- html & css

I conducted my data analysis in Python using the Pandas library, creating new variables and pivot tables to analyze the overall contribution of USAID to HIV service delivery in Uganda by geographic area, sub-group and type of service. 

Dividing the total number of people accessing antiretroviral (ART) services in a subcounty by these population estimates, I was able to determine the approximate percentage of each subcounty reached by ART services. As explained in the story, I did not interpret this as the actual percentage of the subcounty population that accessed HIV medication, because people frequently travel to neighboring subcounties to access HIV care. However, upon consultation with a staff member who works with this data, I interpreted the subcounties with higher percentages as areas where neighboring subcounties had fewer HIV clinics, making people travel to other subcounties for care.

I conducted statistical regressions in R to analyze the associations between the subcounties with higher percentages of ART and subcounties funded by USAID, CDC (Centers for Disease Control and Prevention) and DOD (Department of Defense). I also conducted regressions between the percentage of the subcounty population reached by prevention services and the three U.S. funding agencies. The presence of USAID was statistically significant with a positive coefficient with both increased percentage of ART and total number of people reached by prevention services, whereas the presence of CDC and DOD were not statistically significant with either variable.

I produced several exploratory data visualizations in R - ggplot. I ended up exporting and designing some of the choropleth maps in Adobe Illustrator that I used in the story. Using the UNAIDS data, I created a multiple line chart in Datawrapper that I designed further in Illustrator. I also created a multiple donut chart, where I sized each donut by total number of the priority population and rearranged the charts for a creative graphic. All graphics were designed for desktop, tablet and mobile versions and exported through ai2html for responsiveness.

I also modified the general styling of the page using HTML and CSS.


## Reflection

This project gave me the chance to combine several skills I am refining, including in-depth analysis and exploratory data visualization in Python and R, merging several data sources, cleaning data (using code and when necessary, manually), designing graphics in Adobe Illustrator and developing versions of graphics for various screens. It also allowed me to explore using statistical regressions in my analysis, which I am currently learning. I also tried out creating a more creative type of graphic in Illustrator (the Priority Populations multi-donut chart) where the overall shape of the visualization, the order of the charts, the size of the charts and the specific data visualized in the charts all had a specific meaning. 

It was important for me to continuously ask questions of my contact who works with this data to understand the meaning of the variables and inquire about the validity of some of the calculations I was doing, such as the percentage of subcounty reached by ART and prevention services. This contact provided important context that helped me avoid misrepresenting the findings. However, it was difficult to connect with a former USAID staff because most people feared to share information.

The data is very rich, and I hope to continue conducting further analysis on it - zeroing in on specific vulnerable populations and understanding where they are located and the share of their services that comes from USAID. As the funding situation, even among the other partners like CDC and DOD, is continuously shifting, getting additional data for comparison will also be important for the next story. Also, integrating data on HIV prevalence and/or new infections per subcounty and vulnerable population would allow me to further analyze the impact of loss of funding on specific hotspots that are seeing increases in new infections.  
 


