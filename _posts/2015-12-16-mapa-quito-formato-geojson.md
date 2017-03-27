---
layout:     post
title:      Mapa del cantón Quito en formato GeoJSON
date:       2015-12-16 21:30:00
summary:    Mapas de Quito en formato GeoJSON con límites de parroquias y administraciones zonales.
categories: projects
tags:       [maps, spanish, geojson, project, quito]
---

Comparto a continuación dos mapas del cantón Quito en formato GeoJSON:

### Parroquias

Este archivo incluye los límites de las parroquias con información de la superficie, número de habitantes y la densidad de la población.

<script src="https://embed.github.com/view/geojson/flandrade/quito-crime-map/master/data/parroquias_quito.geojson"></script>

[DESCARGAR](https://raw.githubusercontent.com/flandrade/quito-crime-map/master/data/parroquias_quito.geojson)


### Administraciones zonales

Este archivo incluye los límites de las administraciones zonales con información del número de habitantes y densidad de la población

<script src="https://embed.github.com/view/geojson/flandrade/quito-crime-map/master/data/zonales_quito.geojson"></script>

[DESCARGAR](https://raw.githubusercontent.com/flandrade/quito-crime-map/master/data/zonales_quito.geojson)

## Desventajas de la información oficial disponible

El proceso de recopilación de información, sin embargo, estuvo lleno de contratiempos. Si bien el Municipio del Distrito de Quito ha compartido algunos datos a través del portal [Datos Abiertos](http://datosabiertos.quito.gob.ec/), todavía queda un largo camino por recorrer. No basta con agregar información, sino que además es necesario verificar su formato de publicación.

Por otro lado, no hay información geográfica detallada de la ciudad. Bastaría, de hecho, con un mapa sencillo, pero revisé todo el catálogo y no encontré ningún mapa que pueda ser utilizado directamente para una aplicación web.

Lo cierto es que no encontré un mapa de Quito en formato GeoJSON en ningún sitio.

## Recopilación de información

Este [proyecto ArcGIS](http://datosabiertos.quito.gob.ec/index.php/descargas) es el único mapa disponible de las administraciones zonales en [Datos Abiertos](http://datosabiertos.quito.gob.ec/). Fue necesario, por tanto, convertir estos archivos a GeoJSON a través de [shp2geojson.js](https://github.com/gipong/shp2geojson.js).

Para el mapa de las parroquias, utilicé la información de [OpenStreetMap](http://wiki.openstreetmap.org/wiki/WikiProject_Ecuador) a partir de las relaciones OSM. Los polígonos (GeoJSON) fueron creados con [esta herramienta](http://polygons.openstreetmap.fr/index.py).

Finalmente, los datos de población y superficie fueron recopilados de [Ecuador en cifras](http://www.ecuadorencifras.gob.ec/informacion-censal-cantonal/) y [Datos Abiertos](http://datosabiertos.quito.gob.ec/).
