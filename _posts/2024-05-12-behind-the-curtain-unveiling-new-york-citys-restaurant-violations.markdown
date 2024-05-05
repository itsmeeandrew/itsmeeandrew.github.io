---
layout: post
title:  "Behind the Curtain: Unveiling New York City's Restaurant Violations"
date:   2024-05-02 11:16:39 +0100
categories: analysis
---
New York City is the most popolous city in the United States and one of the most influential in the world. Its cousine includes meals from all around the world, reflecting the cultural diversity of the city. From street side hot-dogs to Michelin stared restaurants, there is something to satisfy every palate and budget. As a visitor to the city --or even for locals--, the amount of optiions can be overwhelming. One need to consider several viewpoints to find their favourable restaurant including price and location. Apart from personal preferences, everyone must take into account the safety and sanity of a certain establishment. In this analysis, we are trying to answer whether there are some factors (e.g. location, type of food served) that can affect a restaurants overall safety and cleanliness. In addition, we try to answer whether one can make a safe choice without the need of checking a restaurant's reviews on websites for hours.

In our research, we used the [DOHMH New York City Restaurant Inspection Results](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j/about_data) dataset from the NYC OpenData database. This dataset contains every violation citation for restaurants up to three years prior to the most recent inspection. We can get information about a restaurant's inspection results, and date with location attributes (coordinates, neighborhood). Based on this, we created a violation score metric. For each <b>Not Critical</b> violation the restaurants received 0.5 points, while for each <b>Critical</b> violation the restaurant received 1 point.

After a quick exploratory analysis we can see that 12,000 restaurants have received less than 7 violations. However, the number of establishments that received at least 7 violations, is even larger, raising the concern whether it is safe to eat-out in New York.

![Histplot](/content/dist_no_viol.png)

<center style = "color:#808080; font-style: italic;" width="80%">Number of violations per each resturant. Many restaurants have more than 7 violations in New York City which makes it not obvious where it is safe to eat.
</center>

<div style="margin:35px"></div>

After investigating the restaurants by geolocations and cousine types served, we can see that Brooklyn has the highest average violation score and Manhattan has the lowest, although the difference is less than one / not significant, and therefore we can not say that a restaurant is safe based solely on its location.

Based on cousine types, we can see that Bangladeshi has the highest violation score and Chimichurri has the lowest. One can argue that these scores can be interpreted as outliers if the number of restaurants in this dataset is low. Even though the number of chimichurri selling restaurants are low we can still say that if a person goes into this type of restaurant, he/she can expect an overall good quality. The low score of the hotdog oriented establishments is also interesting, considering the large amount street-food styled hotdog vendors in NYC.

![Barplots](/content/image.png)

<center style = "color:#808080; font-style: italic;" width="80%">Left: Average violation score by neighborhoods. Right: Top 10 and bottom 10 cousine types based on its average violations score.
</center>

<div style="margin:35px"></div>

To have a deeper understanding about the relation between a restaurants location and its food served, we combined these two features to check whether we can make assumptions about a certain restaurant based on these properties. Interestingly, even though french food is in the top 25, no french restaurant can be found in Staten Island and Bronx.

Staten Island contains both two extremities regarding the average violation score. Thai food has the highest and jewish/kosher has the lowest. The second cousine type with the highest score is Indian food in Bronx.

<embed type="text/html" src="/content/bokeh_nyc.html" width="100%" height="600px" style="margin-left:60px">
<center style = "color:#808080; font-style: italic;" width="80%">The 25 most common cousine types' average violation score by neighborhoods.
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


