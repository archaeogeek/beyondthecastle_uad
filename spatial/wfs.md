# Web Feature Services

The Web Feature Services (WFS) interface is provided by Geoserver, and the GetCapabilities URL can be found at the following URL:
    
    http://lancasteruad.oxfordarchaeology.com:8080/geoserver/uad/wfs?service=WFS&version=1.1.0&request=GetCapabilities

This outputs data in the following coordinate systems:

* **EPSG:27700** (British National Grid)
* **EPSG:4326** (Global Latitude/Longitude)
* **EPSG:900913** (Spherical Mercator)

The available output formats are listed in the GetCapabilities response.

An example request, to download the mons_point layer in excel format would be as follows:

     http://lancasteruad.oxfordarchaeology.com:8080/geoserver/uad/ows?service=WFS&version=1.0.0&request=GetFeature&typeName=uad:mons_points&outputFormat=excel

The following layers are available:

* **cellars**: point data of Lancaster Buildings showing presence or absence of cellars
* **studyarea**: study area boundary of Lancaster Urban Archaeological Database project
* **listed_polys**: polygon boundaries of listed buildings
* **event_points**: point dataset representing historic or archaeological events
* **event_polys**: polygon dataset representing the outline of events such as archaeological digs
* **mons_point**: point dataset representing historic or archaeological monuments
* **monspres_polys**: polygon dataset representing definite monument outlines, eg extant or exposed by archaeological events
* **monsint_polys**: proposed outlines of monuments based on information from archaeological research, events and other information
* **geophys**: contour lines from geophysical survey



