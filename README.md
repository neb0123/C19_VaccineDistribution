# 🦠🧪Covid-19 Vaccine Distribution 🧪🦠
Optimising a vaccine distribution plan for the UK in response to the Covid-19 virus.

## Plan:
**1.** Data reconnaissance:

- [x] Infected per region
[https://www.gov.uk/government/publications/covid-19-track-coronavirus-cases]
- [x] Deaths per region
[https://www.england.nhs.uk/statistics/statistical-work-areas/covid-19-daily-deaths/]
- [x] Population Densities
[https://en.wikipedia.org/wiki/List_of_English_districts_by_population_density, https://en.wikipedia.org/wiki/Regions_of_England]
- [ ] Vaccine distribution centre locations
- [ ] Vaccine amount available & timings

**2.** Data improvements:

- [ ] Go through polygons and make sure they are disjoint
- [ ] Go through hospitals and check coordinates and within correct polygon

**3.** Create notebook:

- [x] Import data
- [ ] Merge data 
- [x] Create UK visual
- [x] Get hospital regions

**4.** Voronoi death density diagram:

*Assumption*: People die in the hospital closest to their house.

*Idea*: Create the Voronoi diagram with hospitals as seeds. Then spread number of deaths out evenly in this space.

**5.** Cluster regions based on regional metrics [Paper](/Papers/shsconf_cyhf2015_01004.pdf)

- [ ] Create regional metrics:

  - Mortality of Infected per Region
  - Morbidity
  - Population Density
  - Population Mortality
  
- [ ] Test various clustering methods and metrics
- [ ] Plot clusters in the 6 2D planes

**6.** Test out distribution algorithms [Paper](/Papers/26618292662088.pdf)

**7.** Test out Integer Programming for location/cost assignment [Paper1](/Papers/efficient_Vaccine_Distribution_Planning_using_IoT_TACTiCS_2015.pdf) [Paper2](2015MCM_paper.pdf)
