---
title: Geoprocessing  # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 9  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Geoprocessing

<b>Geoprocessing</b> allows us to transform and analyze spatial data.

Geoprocessing tools in QGIS typically take one or more layers as an input and produce a new layer as an output.

QGIS includes many geoprocessing tools. More can be added via plugins.

<img src='{{ '/assets/images/geoprocessing-illustration.jpg' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

Image source:
<a href="https://commons.wikimedia.org/wiki/File:Example_of_Clip_Tool_process.gif" target="_blank">Wikimedia Commons</a>.
<a href="https://creativecommons.org/licenses/by-sa/4.0/deed.en" target="_blank">CC-BY-SA 4.0</a>.

We’ll use geoprocessing to analyze areas around each public library location.

To prepare for this, we will need to <b>reproject</b> the libraries layer.
<i>(This is because the spreadsheet data used latitude and longitude, which is an
angular unit of measurement. We need to change this to a linear unit - e.g., metres.)</i> 

## Reprojecting data

• Open the <b>Processing Panel</b> (View -> Panels -> Processing Toolbox) if
it’s not already open.

<img src='{{ '/assets/images/open-processing-toolbox.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Search for <b>reproject layer</b>. Double-click the <b>Vector general ->
Reproject layer</b> result to open the tool.

<img src='{{ '/assets/images/reproject-layer-tool.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• For the <b>Input layer</b>, select the libraries layer from the dropdown.

<img src='{{ '/assets/images/reproject-parameters-1.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• For the <b>Target CRS</b>, choose <b>Project CRS: EPSG:2958 - NAD83(CSRS) / UTM
Zone 17N</b> from the dropdown.

<img src='{{ '/assets/images/reproject-parameters-2.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

Save the output as a <b>shapefile</b>:

• Click the three dots next to the <b>Reprojected</b> box and choose <b>Save to
File</b>.

<img src='{{ '/assets/images/reproject-parameters-3.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Navigate to the data folder and save the output as <b>library_projected.shp</b>.
Click <b>Run</b>.

<img src='{{ '/assets/images/reproject-parameters-4.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

The result is a new version of the libraries layer that uses a different
coordinate reference system. <i>(Note that you can display the underlying CRS by
hovering over the layer name).</i>

<img src='{{ '/assets/images/reprojected-layer.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

## Buffering features
• Search for <b>Buffer</b> in the Processing Toolbox. Double-click 
the <b>Vector Geometry -> Buffer</b> result to open the tool.

<img src='{{ '/assets/images/processing-toolbox-buffer.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Specify the <b>reprojected libraries layer</b> as the <b>Input layer</b> and <b>1
kilometre</b> as the <b>Distance</b>.

<img src='{{ '/assets/images/buffer-parameters-1.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Save the output layer to the data folder as <b>library_buffer_1km.shp</b>.
Click <b>Run</b>.

<img src='{{ '/assets/images/buffer-parameters-2.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Result: A new polygon layer representing a 1-kilometre radius around each
library location.

<img src='{{ '/assets/images/buffer-result.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

## Summarizing data
We’ll use a geoprocessing tool to <b>summarize how many bike share stations are
within a kilometre of each library</b>.

• In the Processing Toolbox, search for <b>count points in polygon</b>.
Double-click <b>Vector analysis -> Count points in polygon to open the tool.</b>

<img src='{{ '/assets/images/count-points-tool.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Specify <b>library_buffer_1km</b> as the <b>Polygons</b> parameter and
<b>bike_share_stations</b> as the <b>Points</b>. Save the output as a shapefile
in the data folder. Click <b>Run</b>.

<img src='{{ '/assets/images/count-points-parameters.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• This will output a layer with the same geometry as the buffered layer, but
its attribute table will contain a new field summarizing the <b>number of libraries
found within each 1-kilometre radius of each library</b>.

<img src='{{ '/assets/images/count-points-results.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />