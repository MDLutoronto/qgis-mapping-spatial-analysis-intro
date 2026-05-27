---
title: Symbology  # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 8  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Symbology

Symbology refers to the graphic design of a layer. It's useful for visualizing
data in a clear, aesthetically pleasing way.

We can also create <b>data-driven symbology</b> that reflects information
stored in a layer's attributes.

## Categorical symbology

• Right-click the neighbourhoods layer and choose <b>Properties</b>.
<img src='{{ '/assets/images/neighbourhood-layer-properties.png' | relative_url }}'
alt="Filtering data" width='70%' height='100%' />

• Click the <b>Symbology</b> tab. Currently, the layer is using <b>Single
symbol</b> - all neighbourhoods are drawn in the same way (the purple outline).

<img src='{{ '/assets/images/neighbourhoods-symbology.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click the dropdown and change the symbology type from Single Symbol to
<b>Categorized</b>.

<img src='{{ '/assets/images/neighbourhoods-symbology-categorized.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click the dropdown and choose <b>Category</b> from the list of available fields.

<img src='{{ '/assets/images/categorized-symbology.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click the <b>Classify</b> button. Each unique category found within the
layer's attribute table is assigned a different coloured fill. Fill colours can
be adjusted manually, or you can choose a colour ramp from the dropdown.
Click OK.

<img src='{{ '/assets/images/classify-results.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Result: Neighbourhood polygons have been styled according to their
designation as neighbourhood improvement areas or emerging neighbourhoods.

<img src='{{ '/assets/images/neighbourhood-polygons-categorical.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

## Graduated symbology
• Go back to the symbology settings for the neighbourhoods layer. Change
the symbology type from Categorized to <b>Graduated</b>.

<img src='{{ '/assets/images/neighbourhoods-graduated.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Choose the <b>socialhousing_units</b> field for the <b>Value</b>.

<img src='{{ '/assets/images/graduated-symbol-value.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click <b>Classify</b>

<img src='{{ '/assets/images/graduated-symbol-classify.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click <b>OK</b>. Neighbourhood polygons have now been symbolized to show
quantity (number of social housing units per neighbourhood).

<img src='{{ '/assets/images/graduated-symbol-result.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />