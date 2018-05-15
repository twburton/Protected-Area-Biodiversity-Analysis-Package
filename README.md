# Protected-Area-Biodiversity-Analysis-Package

-----------
Contact:
-----------
Derek Masaki (dmasaki@usgs.gov)

Theo Burton (twburton@usgs.gov)

Elizabeth Sellers (esellers@usgs.gov)

-----------
Collaborators:
-----------
Shayne Urbanowski (surbanowski@usgs.gov)

-----------
Purpose:
-----------
A Biogeographic Map Analysis Package that utilizes the BISON SOLR API and National Park Service GIS API, to query species occurrence data and generate summary analyses that help users better understand park biodiversity and species composition within the protected area.  

-----------
Details:
-----------
Inputs:

BISON data retrieved through SOLR API
https://data.usgs.gov/solr/occurrences/select?q=scientificName:(%22Pica%20hudsonia%22)&wt=geojson&indent=true&geojson.field=geo

Park Boundaries retrieved through API made available by NPS I&M API
http://irmaservices.nps.gov/v2/rest/unit/CODE/geography?detail=envelope&dataformat=wkt&format=json

or use of SFR:

https://beta-gc2.datadistillery.org/api/v1/elasticsearch/search/bcb/sfr/placenamelookup_poly/_search?q={%22from%22:0,%22size%22:15,%22_source%22:%22properties.*%22,%22query%22:{%22match_phrase_prefix%22:{%22properties.place_name%22:{%22query%22:%22canyons%22,%22max_expansions%22:100}}}}

Outputs:

Summary statistics report - total # occurrences; # unique species; breakdown by higher taxa (mammals, fish, herps, vascular plants, birds, insects, freshwater invertebrates, other)

Listed species report - total # of Federal listed T&E species; # state listed T&E species; # species of greatest conservation need

-----------
Audiences:
-----------
Managers and Biologists/researchers of protected areas (e.g. National Parks, Wildlife Refuges, etc.); State Natural Heritage programs; wildlife and botanical enthusiasts (e.g. birdwatchers).

-----------
Development Status:
-------------------
Software documented in this repository are unpublished and will be under continual development.  Collaborative efforts to help improve code and analyses are welcomed.

----------------------
Copyright and License:
---------------------
This USGS product is considered to be in the U.S. public domain, and is licensed under
[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).

Although this software program has been used by the U.S. Geological Survey (USGS), no warranty, expressed or implied,
is made by the USGS or the U.S. Government as to the accuracy and functioning of the program and related program
material nor shall the fact of distribution constitute any such warranty, and no responsibility is assumed by the
USGS in connection therewith.
