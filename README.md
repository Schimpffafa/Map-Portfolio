# Parker Schimpff's Map Portfolio

                    **Welcome to Parker Schimpff's Map portfolio!**
![Picture of myself](./good-picture.jpg)
Fig. 2: Picture of me in front of Lake One in the Boundary Waters Wilderness Areas

I am...
- A Sophomore at the University of Kentucky
- Majoring in Natural Resources and Environmental Science
- Minoring in GIS/Mapping and Jazz Piano Performance
- An intermediate Spanish speaker (may be an overestimation)
- A member of the Men's Acapella group on campus, acoUstiKats
- The pianist for Williamstown Christian Church
- An Eagle Scout
- A bookworm
- And, among many other things, an amatuer map maker

The goal of this webpage is simple: to present my work in ArcGIS Pro. From here down will be a display of many maps I have created for research, recreation, and coursework. There will be descriptions of why the map was created, what was found through the map, methodology of creating the map, data sources, and python code used (if any).

INSERT TOC

## Kentucky Landcover Map - February 2024

![Kentucky Landcover Splash](./maps/kyLandcover.jpg)
Fig. 2: [Kentucky Landcover PDF](./maps/kyLandcover.pdf)

This map was created for my Advanced GIS class (GEO 409) in the Spring of 2024. It was created to be put in this [website](https://schimpffafa.github.io/geo409-field-trip/) which was my first assignment in website creation through Github and Visual Studio Code (the same program being used to create this portfolio!). This map was created completely through python code.

The 2016 National Landcover Dataset and the Shaded Relief dataset were acquired from The National Map Download Service and MRLC respectively. 

The general python code flow was used:

1. Set input database, output database, environment workspace (same as input), spatial reference 3089 (KY FIPS).
2. Set area of interest variable to be the Kentucky State Polygon
3. Inside a *for* loop, use the *arcpy.analysis.Clip()* command to clip all feature classes in input database by the area of interest.  Do the same for all the raster layers. 