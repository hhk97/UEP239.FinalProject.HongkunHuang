# UEP239.FinalProject.HongkunHuang
## Name: Hongkun Huang
## Time Spend: 10-12 hours

## Summary of Project
The theme of my project was to explore the most suitable areas for new libraries in the Boston area. Each ZCTA was scored by suitability analysis, and the area with the highest score was the most suitable ZCTA for new libraries. And compare the number of existing libraries in the region to determine the final result.

I utilized a total of six weighting factors, and the areas with the highest scores had the following characteristics: far from existing libraries, mear to universities and general schools, near to bus stops, and a land category of Developed space. 

All coordinate systems are adjusted to EPSG:6491

In this analysis, I chose a total of six indicators in BostonMPO area: 
1. distance to existing libraries; 
2. distance to universities; 
3. distance to general schools; 
4. distance to bus stops; 
5. land coverage category; 
6. number of existing libraries in each ZCTA

## Data 
1. tl_2010_25_zcta510.shp: A shapefile with all zctas in MA. 
2. MPO_Boundaries.shp: A shapefile with MPO in MA.
3. LIBRARIES_PT.shp: A shapefile with points of libraries in MA.
4. COLLEGES_PT.shp: A shapefile with points of colleges in MA.
5. SCHOOLS_PT.shp: A shapefile with points of schools in MA.
6. MBTA_Bus_Stops.shp: A shapefile with points of bus stops in Boston.
7. NLCD_2016_Land_Cover_Boston.tif: Raster file of land cover in Boston.

## Method
1. Cilp for Boston Region ZCTAs
2. Rasterize all points
3. Calculate Euclidean Distance to points to get raster files
4. Reclassify all distance and landcover
5. Weighted Raster calculater to get final scores
6. Zonal statitics to get scores in all ZCTAs, then find the highest score of suitability.
7. Attribute join to get library density in ZCTA
8. Compare the existing number of library in ZCTA and our scores to ensure that the most suitable are does not have enough libraries right now.

## Packages
  - scipy
  - numpy
  - pandas
  - shapely
  - geopandas
  - geopy
  - geojson
  - bokeh
  - matplotlib
  - seaborn
  - folium
  - mplleaflet
  - networkx
  - osmnx
  - rasterio
  - richdem
  - rasterstats
  - contextily
