---
title: Loading data   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 6  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Loading Data

Data can be added to QGIS from many different sources, including:
<ul>
<li>Shapefiles</li>
<li>Esri geodatabase</li>
<li>Geopackage</li>
<li>Spreadsheet</li>
<li>Databases (PostgreSQL, SpatialLite, and others)</li>
<li>Image file (raster data)</li>
<li>Web service (WFS, WMS)</li>
</ul>

## Shapefiles
Shapefiles are one of the most common vector file formats used in GIS.

• Select <b>Layer → Add Layer → Add Vector Layer</b> from the menu.

<img src='{{ '/assets/images/add-vector-layer.png' | relative_url }}' alt="Add vector layer" width='100%' height='100%' />

• In the Data Source Manager, click the three dots next to the Vector
 Datasets(s) box.

<img src='{{ '/assets/images/data-source-manager.png' | relative_url }}' alt="Add vector layer" width='100%' height='100%' />

• Browse to the <b>Data → Shapefiles → Streets</b> folder. Select
<b>streets_utm_zone_17.shp.</b> Click <b>Open.</b>

<img src='{{ '/assets/images/streets-shp.png' | relative_url }}' alt="Add vector layer" width='100%' height='100%' />

• Click <b>Add</b>. Close the Data Source Manager.

<img src='{{ '/assets/images/streets-shp-add.png' | relative_url }}' alt="Add vector layer" width='100%' height='100%' />

• Result: A new spatial layer, representing Toronto's street network, has been
added to the map. (<i>Note: This dataset was obtained from the City of Toronto's
Open Data website here:
<a href="https://open.toronto.ca/dataset/toronto-centreline-tcl/">
https://open.toronto.ca/dataset/toronto-centreline-tcl/</a>)

<img src='{{ '/assets/images/streets-layer-added.png' | relative_url }}' alt="Add vector layer" width='100%' height='100%' />

## Spreadsheets
Data can be imported into GIS from spreadsheets (.csv, .xlsx, etc.) Spreadsheets
can be automatically transformed into spatial layers if they contain
geographic information (coordinates). Spreadsheet data can also be <b>joined</b>
to spatial layers based on common attribute values, or converted from
written text using a process called geocoding.

### Add a spreadsheet containing geographic coordinates
• On your computer, navigate to the <b>Data → Tables</b> folder within the data folder.
Double-click <b>bike_share_stations.csv</b> to open it in Excel or other
software that can view spreadsheets.

<img src='{{ '/assets/images/bike-share-file.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Note that each bike share station has <b>latitude and longitude</b> coordinates
associated with it, in columns called 'lat' and 'lon', respectively.
Close the spreadsheet.

<img src='{{ '/assets/images/bike-share-spreadsheet.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• In QGIS, click <b>Layer → Add Layer → Add Delimited Text Layer.</b>

<img src='{{ '/assets/images/add-delimited-text-layer.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Click the three dots next to the <b>File name</b> box.

<img src='{{ '/assets/images/data-source-delimited-text.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Navigate to <b>bike_share_stations.csv</b> and click <b>Open.</b>

<img src='{{ '/assets/images/open-bike-share-csv.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Under the <b>Geometry definition</b> heading, click <b>Point coordinates</b>.
Make sure <b>lon</b> has been selected for the <b>X field</b>, and <b>lat</b>
has been selected for the <b>Y field</b>.

<img src='{{ '/assets/images/geometry-definition-points.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Click <b>Add</b>. Close the Data Source Manager.

<img src='{{ '/assets/images/add-delimited-2.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Result: a point layer showing bike share station locations has been
added to the map.

<img src='{{ '/assets/images/bike-share-points.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

### Add data from a spreadsheet with geocoding
<b>Geocoding</b> attempts to match natural language street addresses to a
physical location on the earth's surface.

<b>Example:</b> 130 Saint George Street, Toronto ON M5S 0C2 = Lat: 43.664,
Long: -79.399.

• Navigate to the data folder and open <b>toronto_public_libraries.csv</b> in
Excel or another spreadsheet viewer.

<img src='{{ '/assets/images/libraries-spreadsheet-file.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Note the columns containing street address information. Close the spreadsheet.

<img src='{{ '/assets/images/libraries-spreadsheet-columns.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• In QGIS, select <b>MMQGIS → Geocode → Geocode CSV with web service</b>.
<i>(If you don't have this option, install the MMQGIS plugin as described in
the <a href="../05-plugins">Plugins</a> section.)</i>

<img src='{{ '/assets/images/geocode-with-web-service.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Navigate to and select <b>toronto_public_libraries.csv</b> as the <b>Input
CSV File</b>.

<img src='{{ '/assets/images/csv-geocode.png' | relative_url }}'
alt="Viewing spreadsheet data" width='70%' />

• Select the <b>StreetAddress, City</b>, and <b>Province</b> columns for the Address, City,
and State parameters (if QGIS hasn't already done this automatically).

<img src='{{ '/assets/images/geocode-address-fields.png' | relative_url }}'
alt="Viewing spreadsheet data" width='70%' />

• Choose <b>OpenStreetMap/Nominatim</b> for the Web Service.

<img src='{{ '/assets/images/geocoding-web-service.png' | relative_url }}'
alt="Viewing spreadsheet data" width='70%' />

• Save the geocoding results in the data folder as <b>library_geocode.shp</b>.
Save the <b>Not Found Output Last</b> in the data folder as
<b>library_geocode_errors.csv</b>. Click <b>Apply.</b>

<img src='{{ '/assets/images/geocode-outputs.png' | relative_url }}'
alt="Viewing spreadsheet data" width='70%' />

• QGIS may be unresponsive for a few moments while the plugin queries the
web service. Once it has completed, however, a results message will be 
displayed. Click <b>Close</b>.

• Result: a new point layer showing public library locations has been added to
the map. The layer’s attribute table contains the information from the csv.

• Records for which the geocoder couldn't figure out a location are recorded in
the <b>library_geocode_errors.csv</b> file.

### Attribute joins
Attribute joins append columns from one table (layer) to another, based on a
<b>common matching field</b>.

Joining data in this way is very common in GIS and in working with databases.

<img src='{{ '/assets/images/table-join-example.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' />

• Navigate to the Tables folder and open <b>socialhousing.csv.</b> This dataset
shows the number of social housing units (including those that are rent geared
to income) in Toronto, by neighbourhood. Note that there are 127 total
records.

<img src='{{ '/assets/images/social-housing-csv.jpg' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' />

• Each neighbourhood in the spreadsheet is signified by an ID number that the
City has designated. This number is stored in the <b>Neighbourhood</b> column.

<img src='{{ '/assets/images/social-housing-csv-ids.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' />

• The Neighbourhoods polygon layer in QGIS also has this ID number in its 
attribute table. It is stored in the <b>Neighbourhood ID</b> field.

<img src='{{ '/assets/images/neighbourhood-id-qgis.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' />

We'll use a join to attach the spreadsheet data to the polygon layer.

First, we'll add the CSV to the QGIS project:

• Select <b>Layer → Add Layer → Add Delimited Text Layer</b>.

<img src='{{ '/assets/images/add-delimited-text-layer.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Navigate to and select <b>socialhousing.csv</b>. Choose no <b>Geometry
(Attribute only table)</b>.

<img src='{{ '/assets/images/delimited-text-no-geometry.png' | relative_url }}'
alt="Viewing spreadsheet data" width='100%' height='100%' />

• Click <b>Add</b>. Close the Data Source Manager. The csv will be added to the
project as a table. It will be listed in the Layers panel, but nothing will be
added to the map.

<img src='{{ '/assets/images/layers-tables.png' | relative_url }}'
alt="Viewing spreadsheet data" width='60%' height='100%' />

### Create the join:

• Right-click (Control-click on Mac) the neighbourhoods layer. Select
<b>Properties</b>.

<img src='{{ '/assets/images/neighbourhood-layer-properties.png' | relative_url }}'
alt="Viewing spreadsheet data" width='60%' height='100%' />

• Click the <b>Joins</b> tab. Click the <b>+ (plus sign)</b> button.

<img src='{{ '/assets/images/add-join.png' | relative_url }}'
alt="Viewing spreadsheet data" width='60%' height='100%' />

• Choose <b>socialhousing</b> as the <b>Join layer</b>, <b>Neighbourhood</b>
as the <b>Join field</b> and <b>ID</b> as the <b>Target field</b>. Click <b>OK.</b>

<img src='{{ '/assets/images/join-parameters.png' | relative_url }}'
alt="Viewing spreadsheet data" width='60%' height='100%' />

• Note that the join is now listed in the layer properties. Click OK to close
the layer properties window.

<img src='{{ '/assets/images/layer-properties-window.png' | relative_url }}'
alt="Viewing spreadsheet data" width='60%' height='100%' />

• Open the attribute table of the neighbourhoods layer. The social housing
columns are now part of this table.

<img src='{{ '/assets/images/joined-table-results.png' | relative_url }}'
alt="Viewing spreadsheet data" width='60%' height='100%' />