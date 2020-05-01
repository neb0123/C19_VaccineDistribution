# 🦠🧪Covid-19 Vaccine Distribution 🧪🦠
Optimising a vaccine distribution plan for the UK in response to the Covid-19 virus.

## Plan:
**1.** Data reconnaissance:

- [x] Infected per region: [Gov link](https://coronavirus.data.gov.uk/#regions)
- [x] Deaths per region:
[ONS link](https://www.ons.gov.uk/peoplepopulationandcommunity/healthandsocialcare/causesofdeath/datasets/deathregistrationsandoccurrencesbylocalauthorityandhealthboard)
- [x] Population Densities: [Wikipedia link](https://en.wikipedia.org/wiki/List_of_English_districts_by_population_density)
- [ ] Vaccine distribution centre locations
- [ ] Vaccine amount available & timings

**2.** Data improvements:

- [ ] Go through polygons and make sure they are disjoint
- [ ] Go through hospitals and check coordinates and within correct polygon

**3.** Create notebook:

- [ ] Import data
- [ ] Merge data:

     - [ ] Infected
     - [ ] Deaths
     - [ ] Population Density
     - [ ] Population
      
- [x] Create UK visual
- [x] Get hospital regions

**4.** Voronoi death density diagram:

*Assumption*: People die in the hospital closest to their house.

*Idea*: Create the Voronoi diagram with hospitals as seeds. Then spread number of deaths out evenly in this space.

- [x] Create Voronoi diagram
- [x] Create coloured density plot based on uniform deaths in each region

**5.** Cluster regions based on regional metrics [Paper](/Papers/shsconf_cyhf2015_01004.pdf)

- [ ] Create regional metrics:

  - [ ] Mortality of Infected per Region
  - [ ] Morbidity
  
- [ ] Test various clustering methods and metrics
- [ ] Plot metrics on map to determine why clusters chosen

**6.** Test out distribution algorithms [Paper](/Papers/26618292662088.pdf)

- [x] Get Data: household estimate, supermarket locations: 
     [House Data](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/families/datasets/householdsbytypeofhouseholdandfamilyregionsofenglandandukconstituentcountries), [Shop Data](https://www.geolytix.co.uk/)
- [ ] Create UK network based on assumed interactions
- [ ] Apply EXPEXT-MAX algorithm

**7.** Test out Integer Programming for location/cost assignment [Paper1](/Papers/efficient_Vaccine_Distribution_Planning_using_IoT_TACTiCS_2015.pdf) [Paper2](2015MCM_paper.pdf)
