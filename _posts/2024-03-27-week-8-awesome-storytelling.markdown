---
layout: post
title:  "Desperation or Deception? Unveiling Crime Patterns During the 2008 Financial Crisis"
date:   2024-03-11 19:16:39 +0100
categories: week8
---
In the wake of the 2008 financial crisis, millions faced economic hardship, losing jobs and homes. This blog post explores the potential impact of these desperate times on crime rates in San Francisco. We will be analyzing data from the San Francisco's Open Data Portal' Police Department Incident Reports, spanning the years 2003 to 2018, to see if a correlation exists between the financial crisis and crime trends.

When examining any data set or historical event, it's crucial to consider potential precursors. In other words, were there any early warning signs that foreshadowed the event? In our case, we're investigating whether robbery rates might have served as a leading indicator of the approaching recession. When doing research on the topic we found an article [[1]](#ref) that suggested that growth in robbery is potentially highly correlated with the financial wellbeing of households. To investigate this phenomenon we started by visualizing the robbery committed between the time frame of 2005 - 2010 (note that we chose these starting and endpoints to have financially stable years to compare with.) 


![Calendar plot](/content/calplot.png)
<center style = "color:#808080; font-style: italic;" width="80%">Daily variations in Robbery rates are showcased in this calendar plot for San Francisco (2005-2010).</center>

<embed type="text/html" src="/content/bokeh.html" width="100%" height="600px">

<embed type="text/html" src="/content/heatmap.html" width="100%" height="600px">


<a id=#ref></a> ### References 
1. [Impact of economic crisis on crime](https://www.unodc.org/documents/data-and-analysis/statistics/crime/GIVAS_Final_Report.pdf)



