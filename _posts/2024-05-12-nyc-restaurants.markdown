---
layout: post
title:  "Desperation or Deception? Unveiling Crime Patterns During the 2008 Financial Crisis"
date:   2024-04-02 11:16:39 +0100
categories: analysis
---
In the wake of the 2008 financial crisis, millions faced economic hardship, losing jobs and homes. This blog post explores the potential impact of these desperate times on crime rates in San Francisco. We will be analyzing data from the San Francisco's Open Data Portal' Police Department Incident Reports, spanning the years 2003 to 2018, to see if a correlation exists between the financial crisis and crime trends.

When examining any data set or historical event, it's crucial to consider potential precursors. In other words, were there any early warning signs that foreshadowed the event? In our case, we're investigating whether robbery rates might have served as a leading indicator of the approaching recession. When doing research on the topic we found an article [[1]](#ref) that suggested that growth in robbery is potentially highly correlated with the financial wellbeing of households. To investigate this phenomenon we started by visualizing the robbery committed between the time frame of 2005 - 2010 (note that we chose these start and endpoints to have financially stable years to compare with.) 

![Calendar plot](/content/calplot.png)

<center style = "color:#808080; font-style: italic;" width="80%">Daily variations in Robbery rates are showcased in this calendar plot for San Francisco (2005-2010).
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


