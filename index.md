---
title       : Malicious Hosts Visualization
subtitle    : Coursera Developing Data Products
author      : Do Hoang Giang
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Product Overview

A Shiny application is develped to visualize and summarize the geo-location of malicious hosts in cyber world.

A snapshot data is taken from the Alient Vault website (http://reputation.alienvault.com/reputation.data). The dataset consists of 258626 records, each of the records have 8 features: IP address, Reliability, Risk, Type, Country. Locale, Coordination, and x. 

In this project, we focus on Risk, Type, Country and Coordination features.

* Country represents the source country of a malicious event.
* Coordination represents the geo-location of the even in the world map.
* Type represents the type of malicious event (i.e. Scanning, Spamming, Control and Command, etc.)
* Risk represent the risk level of the events.

--- .class #id 

## Alien Vault Data
The raw data of this project can be viewed [here](https://raw.githubusercontent.com/hgiang/CourseraDevelopingDataProduct/master/data/reputation.data). This dataset is used in the book **Data-Driven Security: Analysis, Visualization and Dashboards** written by  Jay Jacobs and Bob Rudis.

```
##               IP Reliability Risk          Type Country     Locale
## 1 222.76.212.189           4    2 Scanning Host      CN     Xiamen
## 2 222.76.212.185           4    2 Scanning Host      CN     Xiamen
## 3 222.76.212.186           4    2 Scanning Host      CN     Xiamen
## 4    5.34.246.67           6    3      Spamming      US       <NA>
## 5  178.94.97.176           4    5 Scanning Host      UA     Merefa
## 6    66.2.49.232           4    2 Scanning Host      US Union City
##                         Coords  x
## 1   24.4797992706,118.08190155 11
## 2   24.4797992706,118.08190155 11
## 3   24.4797992706,118.08190155 11
## 4                   38.0,-97.0 12
## 5  49.8230018616,36.0507011414 11
## 6 37.5962982178,-122.065696716 11
```

--- .class #id 

## Summary and Visualization
User input is taken from three dropdown menu.To interact with the map and the summary table, user have the following options: 

* change the color of the displayed maps
* chose the activity type to display
* chose the risk level of the events

A map of geo-location malicious event is displayed for each attack type and risk levels (or the combination of all attack classes and risk levels). The map is drawed by **ggplot2** and **maps** library.

A table describes to top countries for each attack type and risk levels (or the combination of all attack classes and risk levels) is also presented. 

The map and the summary table is intereactively change respected to user input.

--- .class #id 

## Final Product

<img src="app.png" alt="Application Screenshot" style="width: 500px;" align="right"/>

<br/>
<br/>
The application can be view at:

* Shiny server link: [Shiny Malicious Hosts Visualization](https://hgiang.shinyapps.io/RDataProduct)

* Github link: [Gihub Malicious Hosts Visualization](https://github.com/hgiang/CourseraDevelopingDataProduct)





