# Building A Comprehensive Preserved Lands Index Layer for New Jersey State

## Introduction

There are many different groups working in New Jersey to preserve lands for recreational use, ecological integrity and climate resilience planning. Due to my unique position working alongside many involved in the conservation community, I am aware of a need for a parcel-based, statewide preserved lands index. The goal of this index layer is to bring together a large number of disparate datasets from agencies that preserve lands throughout the state. This will allow each agency to work in conjunction with each other, helping to provide information about preservation status, which will help the preservation process for connecting habitat.

Due to the nature of non-uniformity of these datasets, i.e. survey grade versus satellite digitization, tying these datasets together with the comprehensive State parcel database will allow each organization to achieve a level of uniformity that will help with the preservation of New Jersey lands.

This project is tangential to the research work I am undergoing with the Rowan Geolab. Although this work could be performed in the realm of ESRI using shapefiles, merges, dissolves and other aggregation techniques, this would create several intermediate datasets. I am choosing to create a spatial relational database management system (RDMS), PostGIS workflow so that the entire process is reduced to a single query with the only output being a single table.

After collecting all relevant datasets, I plan to create a comprehensive SQL function that will UNION all datasets together, including a new field for their source and date of preservation (if applicable). I then plan to INTERSECT this dataset with the best parcel centroid (which will account for any oddly shaped parcels), then join this dataset back to the full parcel geometry so that it is uniform with the State parcel database.

Issues that I anticipate encountering include collecting relevant datasets, data that does not include proper spatial reference or resolution, and SQL querying methodology that will need to be tweaked and improved along the research process.

## Datasets:

Highlands Council - open space
New Jersey Conservation Foundation - open space
New Jersey Department of Environmental Protection - open space
NRCS Easements
Pinelands Commission - open space
The Nature Conservancy - open space
US Fish and Wildlife - open space
National Park Service - open space
New Jersey State Agricultural Development Committee - preserved farmland
