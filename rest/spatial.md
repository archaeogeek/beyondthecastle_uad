## Spatial REST

Spatial RESTful services are provided by the [Dirt-Simple PostGIS HTTP API](https://github.com/tobinbradley/dirt-simple-postgis-http-api) and are exposed at [http://lancasteruad.oxfordarchaeology.com/pgrest/](http://lancasteruad.oxfordarchaeology.com/pgrest/).

See [http://lancasteruad.oxfordarchaeology.com/pgrest/index.html](http://lancasteruad.oxfordarchaeology.com/pgrest/index.html) for available functions.

### List of available tables

All spatial tables are in EPSG:27700 (British National Grid). Their geometry type is given below:

* **cellars**: dataset of Lancaster Buildings showing presence or absence of cellars - point
* **studyarea**: study area boundary of Lancaster Urban Archaeological Database project - multipolygon
* **listed_polys**: boundaries of listed buildings - multipolygon
* **event_points**: dataset representing historic or archaeological events - point
* **event_polys**: dataset representing the outline of events such as archaeological digs - multipolygon
* **mons_point**: dataset representing historic or archaeological monuments - point
* **monspres_polys**: dataset representing definite monument outlines, eg extant or exposed by archaeological events - multipolygon
* **monsint_polys**: proposed outlines of monuments based on information from archaeological research, events and other information - multipolygon
* * **geophys**: contour lines from geophysical survey - line (note this data has no attributes so might be best as base mapping)

The **ws_geo_listlayers** endpoint will provide you with this list in json format:

    http://lancasteruad.oxfordarchaeology.com/pgrest/v1/ws_geo_listlayers.php

### Getting information on a table

The **ws_listfields** endpoint will provide information on the fields/columns for a particular table in json format. Call it like so:

    http://lancasteruad.oxfordarchaeology.com/pgrest/v1/ws_listfields.php?table=tablename

