---
layout: post
title: Louisville Property Tax and Tree Cover by Parcel Map
description: "Louisville Property Tax and Tree Cover by Parcel Map Using Metro Open Data and Mapbox"
created: 2015-06-09
modified: 2015-06-09
tags: [louisville,parcel,property,tax,tree,canopy,mapbox,open data]
comments: true
image:
  feature: banner-parcel-tree.png
  credit: CDA/Mapbox/OSM
  creditlink: http://data.civicdataalliance.org/dataset/property-tax-tree-cover-parcel
---
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

The city of Louisville's Sustainability Office [commissioned a tree canopy study](https://louisvilleky.gov/government/sustainability/tree-canopy-assessment) from [Davey Resource Group](http://www.davey.com/davey-resource-group/) and created a [detailed report](https://louisvilleky.gov/sites/default/files/sustainability/pdf_files/louisvilleutcreport-24march2015.pdf) of the results.  Louisville needs more trees to combat its [urban heat island problem](https://louisvilleky.gov/government/sustainability/urban-heat-island-project), which shows the city having the fastest growing problem in the nation. 

[![Heat Island](https://louisvilleky.gov/sites/default/files/sustainability/site_images/urban_heat_island_top_20_most_rapidly_growing_cities.png)]

The city took that information and created a [tree canopy online map](https://www.cartotronics.com/UTC_Viewer_Louisville/), but the CDA wanted to look at the data in a different way, showing it more granularly (by property parcel at higher zoom levels), adding interactivity, and also merging property taxes.

So CDA took the parcels tree estimates from the 2012 Tree Canopy data on Louisville's Open Data Portal and merged it with the Sheriff's department's 2014 Tax File open data to create a tree coverage and property tax maps for all of Jefferson County.  For each parcel you can get information like tree coverage, acres, tax value, and tax dollars per acre.

Here are maps we made using this data:

[Tree Canopy Map](http://bit.ly/TreeCanopyVille)

[![Tree Map](/images/screenshot-canopy-tree.png)](http://bit.ly/TreeCanopyVille)

- Bright Green = Many trees
- Dark green = Few trees
- Black = No trees


[Property Tax Map](http://bit.ly/PropertyTaxVille)

[![Tax Map](/images/screenshot-canopy-tax.png)](http://bit.ly/PropertyTaxVille)

- Red = High Tax
- Orange = Mid Tax
- Yellow = Low Tax
- Black = No tax collected (gov, non-profit, infrastructure)


[Property Tax Per Acre Map](http://bit.ly/TaxPerAcreVille)

[![Acre Map](/images/screenshot-canopy-acre.png)](http://bit.ly/TaxPerAcreVille)

- Dark blues = $100 to $10,000+ per acre.
- Mid range = $70 to $25.
- Light greens/white < $10 per acre.
- Black = No tax collected (gov, non-profit, infrastructure)

**Raw Data**

Visit our open data portal to get the full Shapefiles and CSV data that we created to build our maps, and create your own visualizations.  We hope these tools can inform the public about the importance of tree coverage in their neighborhood, trees affect on property values, and the value of having detailed [open data](http://data.louisvilleky.gov/).

[CDA Open Data Downloads](http://data.civicdataalliance.org/dataset/property-tax-tree-cover-parcel)

Each parcel has these fields:

- **Parcel** (Parcel) - unique ID, can be used to merge with other datasets.
- **Tree Canopy Percentage** (CanP) - percent tree coverage in this parcel.
- **Tree Canopy Acreage** (CanA) - total tree acreage covered in parcel.
- **Total Acreage** (Acres) - size of parcel.
- **2014 Taxed Property Value** (2014Tax) - Property tax due, in dollars.
- **Tax Per Acre** (TaxAcre) - 2014Tax/Acres: to get the cost per acre in dollars.
- **Canopy Value Factor** (CanVal) - TaxAcre*CanP: formula for looking at impact of tree data across property value.

Tax Value comes from the Sheriff's Department [online tax roll for 2014](http://www.jcsoky.org/download/taxfiledownloads.htm).

Tree Coverage and parcel outlines come from [Louisville Metro's open data portal](http://portal.louisvilleky.gov/dataset/utcdata).
