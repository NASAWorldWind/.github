Important notice: Official NASA WorldWind development is suspended, beginning April 5th, 2019. Issues will not be attended by the maintainers in the foreseeable future, your are welcome to raise this issue anyway for the benefit of the community for the benefit of the community.

More information about the suspension and general guidance into alternative geospatial data services that may be used by WorldWind at the following link:
 
https://worldwind.arc.nasa.gov/news/2019-03-21-suspension-faq/

This suspension also applies to the WorldWind geospatial data web services that operated at NASA Ames Research Center (ARC), which are configured by as the default for layers and elevation models in the WorldWind 3D globe (imagery, elevations and place names). If your WorldWind-based application is not retrieving imagery or elevations, it may be that it's attempting to access services from a *.worldwind.arc.nasa.gov server (you can use a network traffic monitoring tool to determine whether or not that's the case).

Your WorldWind-based application can be modified to retrieve from other geospatial web services in order to continue operating without relying on NASA ARC geospatial data services. Throughout the source files you can look for references to URLs in the form of https://worldwind\d\d.arc.nasa.gov (in regex notation) in order to find which features of WorldWind make use of NASA ARC services. For instance, any elevations layer points either towards  https://worldwind26.arc.nasa.gov or https://data.worldwind.arc.nasa.gov/elev.
