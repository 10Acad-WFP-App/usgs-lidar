**Geopandas**

This repo python module produce an easy to use, reliable and well designed module that domain experts and data scientists can use to fetch, visualize, and transform publicly available satellite and LIDAR data.

Python tools for geographic data

GeoPandas is a project to add support for geographic data to pandas objects. It currently implements GeoSeries and GeoDataFrame types which are subclasses of pandas.Series and pandas.DataFrame respectively. GeoPandas objects can act on shapely geometry objects and perform geometric operations.

GeoPandas geometry operations are cartesian. The coordinate reference system (crs) can be stored as an attribute on an object, and is automatically set when loading from a file. Objects may be transformed to new coordinate systems with the to_crs() method. There is currently no enforcement of like coordinates for operations, but that may change in the future.

Documentation is available at geopandas.org (current release) and Read the Docs (release and development versions).

**Install**

See the installation docs for all details. GeoPandas depends on the following packages:

pandas
shapely
fiona
pyproj
Further, matplotlib is an optional dependency, required for plotting, and rtree is an optional dependency, required for spatial joins. rtree requires the C library libspatialindex.

Those packages depend on several low-level libraries for geospatial analysis, which can be a challenge to install. Therefore, we recommend to install GeoPandas using the conda package manager. See the installation docs for more details.

Get in touch
Ask usage questions ("How do I?") on StackOverflow or GIS StackExchange.
Report bugs, suggest features or view the source code on GitHub.
For a quick question about a bug report or feature request, or Pull Request, head over to the gitter channel.
For less well defined questions or ideas, or to announce other projects of interest to GeoPandas users, ... use the mailing list.
Examples

>>> import geopandas
>>> 
>>> from shapely.geometry import Polygon
>>> 
>>> p1 = Polygon([(0, 0), (1, 0), (1, 1)])
>>> 
>>> p2 = Polygon([(0, 0), (1, 0), (1, 1), (0, 1)])
>>> 
>>> p3 = Polygon([(2, 0), (3, 0), (3, 1), (2, 1)])
>>> 
>>> g = geopandas.GeoSeries([p1, p2, p3])
>>> 
>>> 
>>> 
>>> POLYGON ((0 0, 1 0, 1 1, 0 0))

>>> POLYGON ((0 0, 1 0, 1 1, 0 1, 0 0))

>>>   POLYGON ((2 0, 3 0, 3 1, 2 1, 2 0))

>>> dtype: geometry

