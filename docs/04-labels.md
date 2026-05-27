---
title: Adding and customizing labels   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 4  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Labels

Add labels to the neighbourhoods layer:

• Right-click the layer in the Layers panel. Choose <b>Properties</b>.
<img src='{{ '/assets/images/layer-contextual-menu.png' | relative_url }}' alt="Layer popup menu." width='100%' height='100%' />

• Select the <b>Labels</b> tab.
<img src='{{ '/assets/images/properties-labels.png' | relative_url }}' alt="Properties window opened to the Labels tab." width='100%' height='100%' />

• From the dropdown, select <b>Single Labels</b>.
<img src='{{ '/assets/images/single-labels.png' | relative_url }}' alt="'Single labels' option." width='100%' height='100%' />

• Click OK. Labels will appear within each neighbourhood polygon. The label information
is being pulled from the attribute table.
<img src='{{ '/assets/images/labelled-polygons.png' | relative_url }}' alt="Labels displayed on the map view." width='100%' height='100%' />


