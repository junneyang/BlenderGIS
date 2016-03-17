Blender GIS
==========

[Wiki](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage) available for further information.

**Update 2016**, [new tool](https://github.com/domlysz/BlenderGIS/wiki/Terrain-analysis) to analyzing height, slope and aspect of a terrain.

**Coming soon** import georaster refactoring :
- Add support for float32 and negatives values
- Add abitity to read geotiff tags (no more need a worldfile for tiff raster)
- A new option to fill no data values
- More user friendly, discard some useless options


ESRI Shapefile import / export
--------------------

A [Shapefile](http://en.wikipedia.org/wiki/Shapefile) is a popular geospatial vector data format for geographic information system software.

This tool can import into Blender most of shapefile feature type. It can also uses attributes data to define Z elevation values or Z extrusion values.

Exporter script can export a mesh to pointZ, polylineZ or polygonZ shapefile.

Note that Blender cannot handle attribute data include in dbase file linked to the shapefile. So if you want import a shapefile for edit it into Blender and then re-export it, you will lose attribute data.


Georeferenced raster importer
--------------------

Import common image format associated with a [world file](http://en.wikipedia.org/wiki/World_file) that describes the location, scale and rotation of the raster in a geographic coordinate system.

You can import the raster as a plane mesh, as backgound image for orthographic view, as UV texture mapping on a mesh or as DEM for warp a mesh with the displace modifier.


Georeferenced render output
--------------------

This is a tool to create a new camera correctly setup for produce a map render. Georeferencing data (worldfile) are writing in text file accessible from the Blender text editor.


Delaunay triangulation & Voronoi diagram
--------------------

This script computes [Delaunay triangulation](http://en.wikipedia.org/wiki/Delaunay_triangulation) in 2.5D. This triangulation is suitable for create a 3D terrain mesh from [points cloud](http://en.wikipedia.org/wiki/Point_cloud) or [contour lines](http://en.wikipedia.org/wiki/Contour_line)

The script can also compute [Voronoi tessellation](http://en.wikipedia.org/wiki/Voronoi) in 2D which is the dual of delaunay triangulation. Voronoi diagram is suitable to make neighborhood analysis map.


Terrain analysis
--------------------

This part of Blender GIS is designed to assist in the analysis of the topography : height, slope and azimuth (aspect).

There are 2 tools, one to build materials nodes setup for Cycles engine, and a second to configure the color ramp as usual in common GIS software (reclassify values and apply color ramp presets).
