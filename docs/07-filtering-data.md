---
title: Filtering data   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 7  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Filtering data

We can filter datasets in QGIS based on criteria we choose. This allows us to
work with a logically defined subset of a layer or table.

<img src='{{ '/assets/images/filter-example-illustration.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Right-click the <b>streets</b> layer and choose <b>Properties</b>.

<img src='{{ '/assets/images/streets-layer-properties.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• From the <b>Source tab</b>, click the <b>Query builder</b> button at the
bottom right.

<img src='{{ '/assets/images/source-query-builder.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

Build the query:
• Double-click <b>Roadclass</b> in the <b>Fields</b> window. The field name will
appear, in quotes, in the <b>expression box</b> below.

<img src='{{ '/assets/images/query-builder-1.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click the <b>NOT</b> button, then the <b>LIKE</b> button.

<img src='{{ '/assets/images/query-builder-2.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click the <b>All</b> button under the <b>Values window</b>. This will display
every unique value found within the Roadclass field.

<img src='{{ '/assets/images/query-builder-3.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Double-click <b>Local</b> to create the complete expression:
<b>"Roadclass" NOT LIKE 'Local'</b>. Click OK.

<img src='{{ '/assets/images/query-builder-4.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />

• Click OK to exit the Properties window. <b>Result: local roads are now hidden
from the display.</b>

<img src='{{ '/assets/images/filtered-roads.png' | relative_url }}'
alt="Filtering data" width='100%' height='100%' />