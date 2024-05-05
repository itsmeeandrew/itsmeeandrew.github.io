---
layout: post
title:  "NYC Restaurants"
date:   2024-05-02 11:16:39 +0100
categories: analysis
---
New York City is the most popolous city in the United States and one of the most influential in the world. Its cousine includes meals from all around the world, reflecting the cultural diversity of the city. From street side hot-dogs to Michelin stared restaurants, there is something to satisfy every palate and budget. As a visitor to the city --or even for locals--, the amount of optiions can be overwhelming. One need to consider several viewpoints to find their favourable restaurant including price and location. Apart from personal preferences, everyone must take into account the safety and sanity of a certain establishment. In this analysis, we are trying to answer whether there are some factors (e.g. location, type of food served) that can affect a restaurants overall safety and cleanliness. In addition, we try to answer whether one can make a safe choice without the need of checking a restaurant's reviews on websites for hours.

In our research, we used the [DOHMH New York City Restaurant Inspection Results](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j/about_data) dataset from the NYC OpenData database. This dataset contains every violation citation for restaurants up to three years prior to the most recent inspection. We can get information about a restaurant's inspection results, and date with location attributes (coordinates, neighborhood).

After a quick exploratory analysis we can see that 12,000 restaurants have received less than 7 violations. However, the number of establishments that received at least 7 violations, is even larger.

![Calendar plot](/content/dist_no_viol.png)

<center style = "color:#808080; font-style: italic;" width="80%">Number of violations per each resturant..
</center>

<div style="margin:35px"></div>

Examining the calendar plot the first thing we noticed is that the count of robbery committed correlates with the economic down turn. As the density of darker green days during the recession (2007 - 2008) is greater than the rest of the examined period. Furthermore, the growth in robberies can indicate and economic downturn as we can observe a hike in this type of crime preceding the crises in 2006.

Interpreting the daily crime occurrences is a good tool to understand trends over time, however, to obtain a deeper, higher level overview analyzing crime occurrences over a longer period might yield more concrete insights. Hence, the comparison of the monthly crime magnitudes for each year in the considered period can be seen below.

<embed type="text/html" src="/content/bokeh_nyc.html" width="100%" height="600px" style="margin-left:60px">
<center style = "color:#808080; font-style: italic;" width="80%">Number of robberies aggregated by months in San Francisco (2005-2010).
</center>

<div style="margin:35px"></div>

From this, we can see that there was an increasing trend in the number of robberies before the burst of the bubble in 2008. Interestingly, there were more robberies in 2006 than in 2007, but in both years there were significantly more robberies than in 2005. In 2008, when the financial bubble burst, the number of robberies reached its peak. After this, the crime rates went back to a more normal level in 2009, and reached its minimum in the considered period in 2010. The decrease probably can be explained by the normalization of the world economy and the daily lives of people in general.

By delving more deeply into the data and looking for geographical aspects, we can see which regions contributed to the peak in the number of robberies in 2008. Most of the western regions (Taraval, Park, Richmond) had stagnating crime rates in our focus period; however, some eastern regions (Bayview, Mission, Southern) had a big increase during the recession. Comparing these regions with the poverty rates for neighborhoods [[2]](#ref), we cannot notice any correlation between the poverty rates and the robbery-affected regions.

<embed type="text/html" src="/content/map_nyc.html" width="100%" height="600px">
<center style = "color:#808080; font-style: italic;" width="80%">Regional differences in robbery rates in San Francisco (2005-2010).
</center>

<div style="margin:35px"></div>

<embed type="text/html" src="/content/map_2_nyc.html" width="100%" height="600px">
<center style = "color:#808080; font-style: italic;" width="80%">Regional differences in robbery rates in San Francisco (2005-2010).
</center>

<div style="margin:35px"></div>

In this report, we investigated the effects of the Great Recession on the rates of robberies. We can conclude that during the considered period, there is correlation between the number of robberies and the timeline of the financial crisis (the lead up, the event, and the aftermath). On the other hand, we do not believe that the financial crisis could have been predicted based on the number of robberies, as correlation is not causation and it would be a classical example of hindsight bias. Rather, uncovering these insights is part of understanding the wider impact the Great Recession had on everyday people's lives.
### <a name="ref"></a>  References 

1. [Impact of economic crisis on crime](https://www.unodc.org/documents/data-and-analysis/statistics/crime/GIVAS_Final_Report.pdf)

2. [One in three homes in this San Francisco neighborhood lives below the poverty line](https://sfstandard.com/2022/12/08/san-francisco-neighborhood-new-census-data-maps/)

### <a name="ref"></a>  Contributions 

- András Bence Schin (s233084): Bokeh plot and text

- István László Mádi (s232971): Calendar plot and text

- Boldizsár Elek (s233085): Choropleth map and text


