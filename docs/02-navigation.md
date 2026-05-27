---
title: Navigation (and a quick look at projections)   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 2  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Navigating the QGIS Interface (and a quick look at projections)
## Panning and zooming
Use the <b>Pan</b> tool to shift the map extent (alternatively, click and hold the 
middle mouse button or press the Spacebar).
<img src='{{ '/assets/images/pan-tool.png' | relative_url }}' alt="The Pan Tool." width='100%' height='100%' />

Use the <b>Zoom tools</b> or the mouse wheel to zoom in and out on the map view.
<img src='{{ '/assets/images/zoom-tools.png' | relative_url }}' alt="Zoom in or out using the zoom tools." width='100%' height='100%' />

The map <b>scale</b>, found in the status bar on the bottom of the interface, can also
be adjusted to zoom in or out.
<img src='{{ '/assets/images/map-scale.png' | relative_url }}' alt="Map scale." width='100%' height='100%' />

## Bookmarks
<b>Bookmarks</b> let us save map locations and scales.

Go to <b>View -> Show Spatial Bookmarks</b>.
<img src='{{ '/assets/images/show-spatial-bookmarks.png' | relative_url }}' alt="Spatial bookmarks." width='100%' height='100%' />

Expand the <b>Project Bookmarks</b> heading.
<img src='{{ '/assets/images/project-bookmarks.png' | relative_url }}' alt="Project bookmarks." width='100%' height='100%' />

Double-click the <b>Southern Ontario</b> bookmark. The map view will be automatically updated to a 
pre-configured scale and extent.
<img src='{{ '/assets/images/southern-ontario.png' | relative_url }}' alt="'Southern Ontario' bookmark." width='100%' height='100%' />

Double-click the <b>World</b> bookmark. Once it loads (it may take a moment),
the map view will be adjusted to show the entire world. At this scale, the map
looks quite distorted - this isn't a bug, it's because the QGIS project is
using a <b>projection</b> that's well-suited for displaying the Toronto area, but
not intended for a global extent.
<img src='{{ '/assets/images/world.png' | relative_url }}' alt="'World' bookmark." width='100%' height='100%' />

## Projection/Coordinate Reference System Settings

A project's projection/coordinate system is indicated by the EPSG number on the
 status bar. Click the ‘EPSG:2958’ text in the lower-right of the interface to
 see the coordinate system settings.
<img src='{{ '/assets/images/epsg.png' | relative_url }}' alt="Coordinate system/projection options." width='100%' height='100%' />

Type 4326 in the search bar (don't press enter). Select WGS84 from the results.
Click OK.
<img src='{{ '/assets/images/4326.png' | relative_url }}' alt="4326." width='100%' height='100%' />

Result:
<img src='{{ '/assets/images/4326.png' | relative_url }}' alt="Entire world in WGS84." width='100%' height='100%' />

Now click the coordinate system text again and change the projection back to
UTM Zone 17 (EPSG: 2958).
<img src='{{ '/assets/images/2958.png' | relative_url }}' alt="Changing the CRS to UTM Zone 17." width='100%' height='100%' />

If you'd like to learn more about coordinate reference systems in GIS,

