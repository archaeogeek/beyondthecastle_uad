# Web Mapping Services

The Web-Mapping Services (WMS) interface is supplied by a geoserver instance and can be reached at the following GetCapabilities URL:

    http://lancasteruadgeo.oxfordarchaeology.com/geoserver/uad/wms?service=WMS&version=1.3.0&request=GetCapabilities

This outputs data in the following coordinate systems:

* **EPSG:27700** (British National Grid)
* **EPSG:4326** (Global Latitude/Longitude)
* **EPSG:900913** (Spherical Mercator)

The following modern base maps are available:

* **osopen**: Ordnance Survey, based on Vector Map District
* **osopenbw**: Ordnance Survey grayscale, based on Vector Map District
* **osopenraster**: Ordnance Survey, based on Street View
* **osopenrasterbw**: Ordnance Survey grayscale, based on Street View

The following historic base maps are available:

* **Docton1684**: Kenneth Docton's map of Lancaster, 1684
* **Mackreth1778**: Stephen Mackreth's "Plan of the town of Lancaster", 1778
* **Clarke1807**: Christopher Clark's "A plan of the town of Lancaster", 1807
* **Baines1824**: Edward Baines' "Plan of Lancaster", 1824
* **OS_1_25**: Ordnance Survey 1st Edition 25 inch, 1893

There is also a small area of Geophysical survey available, which is very detailed line data but has no attributes, so may work better as WMS:

* **geophys**

LIDAR data is available as both unprocessed (with buildings) and unprocessed (without buildings) and in 25cm and 2m resolution:
* **lidar_processed_25cm**
* **lidar_processed_2m**
* **lidar_unprocessed_25cm**
* **lidar_unprocessed_2m**

Reference on using WMS can be found at:

    http://en.wikipedia.org/wiki/Web_Map_Service

A sample GetMap request is as follows (use the GetCapabilities request to find out the available layers and output formats):

    http://lancasteruadgeo.oxfordarchaeology.com/geoserver/uad/wms?service=WMS&version=1.1.0&request=GetMap&layers=uad:Clarke1807&styles=&bbox=347195.2852705703,460963.365584321,348158.27652011556,462471.0608549123&width=327&height=512&srs=EPSG:27700&format=image%2Fjpeg

