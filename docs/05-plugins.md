---
title: Plugins   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 5  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Plugins

Plugins are add-ons for the QGIS software, usually developed by a third party
(not the QGIS organization itself). Plugins are immensely helpful in adding
functionality to the core QGIS application.

We'll add two plugins to our installation of QGIS:

## QuickMapServices
Easily search for and add basemaps and other data layers from the web.

• Click <b>Plugins</b> on the QGIS menu. Choose <b>Manage and Install Plugins</b>.
<img src='{{ '/assets/images/plugins.png' | relative_url }}' alt="Plugins -> Manage and Install Plugins." width='100%' height='100%' />

• In the Plugin Manager window, click the <b>All</b> tab. Search for
<b>quickmapservices</b>.
<img src='{{ '/assets/images/quickmapservices-search.png' | relative_url }}' alt="Searching for quickmapservices." width='100%' height='100%' />

• Select the <b>NextGIS QuickMapServices</b> item from the results.
<img src='{{ '/assets/images/quickmapservices-search-result.png' | relative_url }}' alt="Selecting the quickmapservices plugin." width='100%' height='100%' />

• Click <b>Install Plugin</b>.
<img src='{{ '/assets/images/quickmapservices-search-install.png' | relative_url }}' alt="Installing the plugin." width='100%' height='100%' />

## MMQGIS
This plugin contains a suite of various useful tools. We'll use it to perform geocoding in the next section.

• From the <b>All</b> section of the Plugin Manager, search for <b>mmqgis</b>.
<img src='{{ '/assets/images/search-mmqgis.png' | relative_url }}' alt="Searching for MMQGIS." width='100%' height='100%' />

• Select the <b>mmqgis</b> item from the results and click <b>Install Plugin</b>. Close the Plugin Manager.
<img src='{{ '/assets/images/install-mmqgis.png' | relative_url }}' alt="Searching for MMQGIS." width='100%' height='100%' />