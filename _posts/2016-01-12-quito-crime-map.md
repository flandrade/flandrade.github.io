---
layout:     post
title:      Quito Crime Map
date:       2016-01-12 19:52:32
summary:    An interactive crime map that shows the crime rate of Quito as reported by Policía Nacional del Ecuador.
categories: projects
tags:       [maps, english, geojson, project, quito]
---

![Crime map]({{ site.url }}/assets/images/quitocrimemap.jpg)

<a href="http://flandrade.github.io/quito-crime-map/" class="button-sp button-sp-inverse wayra wayra-inverse mb1">Quito Crime Map</a>

Inspired by the [NYPD Crime Map](https://maps.nyc.gov/crime/), I created an [interactive crime map of Quito](http://flandrade.github.io/quito-crime-map/) using [Leaflet](http://leafletjs.com/). This map shows the crime rate by category and year, as reported to Policía Nacional del Ecuador. The administrative areas are shaded according to crime rate per 100,000 population.

Data was collected from [Datos Abiertos](http://datosabiertos.quito.gob.ec/), the official government site for open government. The crime categories represented here are the same categories used by the Police such as murders, motor vehicle theft, burglary and robbery.

### The GeoJSON Map

As far as I know, there aren't GeoJSON maps of Quito. so I [created a map](https://github.com/flandrade/quito-crime-map/blob/master/data/zonales_quito.geojson) based on a GIS file that is publicly available on [Datos Abiertos](http://datosabiertos.quito.gob.ec).  For this, [shp2geojson.js](http://gipong.github.io/shp2geojson.js/) is a great conversion tool.

[GeoJSON map of Quito](https://github.com/flandrade/quito-crime-map/blob/master/data/zonales_quito.geojson)
