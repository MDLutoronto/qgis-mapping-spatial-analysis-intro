---
title: Exploring map layers   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 3  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Exploring map layers

This project contains a basemap (Esri Grey) and one polygon layer showing neighbourhood
boundaries within Toronto.

## Query a layer with the Identify Tool

• Left-click the NeighbourhoodsUTMZone17 item in the Layers panel to select it.
<img src='{{ '/assets/images/select-neighbourhoods-layer.png' | relative_url }}' alt="Selecting the neighbourhoods layer in the Layers Panel." width='100%' height='100%' />

• Click the <b>Identify Features</b> button on the toolbar.
<img src='{{ '/assets/images/identify-features-button.png' | relative_url }}' alt="The Identify Features Tool." width='100%' height='100%' />

• Click within any neighbourhood polygon in the map view. The feature will be
highlighted on the map and information about it will appear in a popup.
<img src='{{ '/assets/images/feature-popup.png' | relative_url }}' alt="Querying a feature using the Identify tool to see its popup." width='100%' height='100%' />

## View a layer's Attribute Table
• Right-click (or Control-click if using a Mac) the neighbourhoods layer.
Choose <b>Open Attribute Table</b> from the menu.
<img src='{{ '/assets/images/open-attribute-table.png' | relative_url }}' alt="Opening a layer's attribute table." width='100%' height='100%' />

• Each polygon within the layer is displayed as a row in the attribute table.
<img src='{{ '/assets/images/attribute-table.png' | relative_url }}' alt="The attribute table." width='100%' height='100%' />

• Click the row number of any record to select it. The attribute table row and
its corresponding map polygon will be highlighted. Click the <b>Zoom</b> button
(at the top of the attribute table) to zoom to the selected feature.
<img src='{{ '/assets/images/zoom-to-selection.png' | relative_url }}' alt="Zooming to a selected polygon from the attribute table." width='100%' height='100%' />

• Click the <b>Deselect</b> button to clear the selection.
<img src='{{ '/assets/images/deselect.png' | relative_url }}' alt="Zooming to a selected polygon from the attribute table." width='100%' height='100%' />
