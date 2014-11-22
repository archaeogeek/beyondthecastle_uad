## Spatial REST

Spatial RESTful services are provided by the [Dirt-Simple PostGIS HTTP API](https://github.com/tobinbradley/dirt-simple-postgis-http-api) and are exposed at [http://lancasteruad.oxfordarchaeology.com/pgrest/](http://lancasteruad.oxfordarchaeology.com/pgrest/).

See [http://lancasteruad.oxfordarchaeology.com/pgrest/index.html](http://lancasteruad.oxfordarchaeology.com/pgrest/index.html) for available functions.

### List of available tables

All spatial tables are in EPSG:27700 (British National Grid). Their geometry type is given below:

* cellars - point
* event_points - point
* event_polys - multipolygon
* listed_polys - multipolygon
* monsint_polys - multipolygon
* mons_point - point
* monspres_polys - multipolygon
* studyarea - multipolygon

The **ws_geo_listlayers** endpoint will provide you with this list in json format:

    http://lancasteruad.oxfordarchaeology.com/pgrest/v1/ws_geo_listlayers.php

### Getting information on a table

The **ws_listfields** endpoint will provide information on the fields/columns for a particular table in json format. Call it like so:

    http://lancasteruad.oxfordarchaeology.com/pgrest/v1/ws_listfields.php?table=tablename


