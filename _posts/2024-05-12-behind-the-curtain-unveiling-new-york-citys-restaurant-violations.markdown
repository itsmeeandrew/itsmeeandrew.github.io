---
layout: post
title:  "Beneath the Chef's Hat: Unveiling New York City's Restaurant Violations"
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

Based on cousine types, we can see that Bangladeshi has the highest violation score and Chimichurri has the lowest. One can argue that these scores can be interpreted as outliers if the number of restaurants in this dataset is low. Even though the number of chimichurri selling restaurants are low we can still say that if a person goes into this type of restaurant, he/she can expect an overall good quality. The low score of the hotdog oriented establishments is also interesting, considering the large amount street-food styled hotdog vendors in NYC.

![Barplots](/content/image.png)

<center style = "color:#808080; font-style: italic;" width="80%">Top 10 and bottom 10 cousine types based on its average violations score.
</center>

<div style="margin:35px"></div>

To have a deeper understanding about the relation between a restaurants location and its food served, we combined these two features to check whether we can make assumptions about a certain restaurant based on these properties. Interestingly, even though french food is in the top 25, no french restaurant can be found in Staten Island and Bronx.

Staten Island contains both two extremities regarding the average violation score. This means the Thai food is the least safe to eat in New York City in Staten Island, and the safest food to eat is Jewish/Kosher. Furthermore, it seems to be a safe bet to eat at Korean and Frozen Dessert places in Staten Island. It is also interesting to note that there seems to be a notable difference in food safety between Bronx and Manhattan when it comes to Chinese and Mediterranean food. Some other places to avoid are: Indian and Latin American places in Queens, Indian places in Brooklyn, Thai and Korean places in Bronx, Indian places in Manhattan, Bakery products in Staten Island.

<div style="margin:35px"></div>
<embed type="text/html" src="/content/bokeh_nyc.html" width="100%" height="600px" style="margin-left:60px">
<center style = "color:#808080; font-style: italic;" width="80%">The 25 most common cousine types' average violation score by neighborhoods.
</center>


After investigating the restaurants by geolocations and cousine types served, we can see that Brooklyn has the highest average violation score and Manhattan has the lowest, although the difference is less than one / not significant, and therefore we can not say that a restaurant is safe based solely on its location.

<embed type="text/html" src="/content/map_nyc.html" width="100%" height="600px">
<center style = "color:#808080; font-style: italic;" width="80%">Average violation score, based on location.
</center>

To get an even more in-depth understanding of the inspection scores relation to the restaurants whereabouts, we extended our previous analysis, to see if the various types of restaurants have higher quality in different boroughs. We found that overall Latin-American cousine has the highest validation scores, especially in Brooklyn it might not be the wisest choice. Middle-Eastern cousine has record low violation score on Staten Island. Altogether we can say that some locations are better when it comes to certain kinds of restaurants. 

<div style="margin:35px"></div>

<embed type="text/html" src="/content/map_2_nyc.html" width="100%" height="600px">
<center style = "color:#808080; font-style: italic;" width="80%">Regional violation scores based on cousine type.
</center>

<div style="margin:35px"></div>

To determine how descriptive the location, cousine type and the count of violation committed for the overall violation scores we conducted machine learning based analysis. We found out that is is an exceptionally good predictor as with our machine learning model we achieved 98% accuracy.  

![MLPLOT](/content/output.png)

<center style = "color:#808080; font-style: italic;" width="80%">Predictive performance based on location, cousine types and violation counts 
</center>

In summary, our analysis of NYC restaurant violations highlights the importance of considering factors like cuisine type and location when dining out. While some links between location and safety were found, we could not find conclusive connections visible to the naked eyes. However to show the level of connections between the aforementioned factors not visible for our eyes we applied our machine learning model and showed high accuracy, meaning that in fact location and cousine types highly correlate with the given violation scores. 

### <a name="ref"></a>  Contributions 

- András Bence Schin (s233084): Bokeh plot and text

- István László Mádi (s232971): Map based visualizations, text, ml model

- Boldizsár Elek (s233085): Choropleth map and text


