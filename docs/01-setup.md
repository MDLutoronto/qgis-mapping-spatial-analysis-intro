---
title: Setup   # Title of the page, which will be displayed in the navigation and the browser title.
parent: An Introduction to Mapping and Spatial Analysis with QGIS
layout: default  # Layout type, usually 'page' for standard pages.
nav_order: 1  # Order in the navigation menu.
maintainer:
    - name: Cole White
      link: https://library.utoronto.ca/staff/cole-white
created_date: 2026-05-25 # Date when the page was created. Should be in YYYY-MM-DD format.
---

# Setup
<b>If you'd like to follow along with the examples, please download and unzip the
sample data from the Map and Data Library: <a href="https://uoft.me/qgis">QGISEssentials.zip</a></b>

## Opening the project file

Launch QGIS3. From the menu at the top of the interface, choose <b>Project → Open...</b>

<img src='{{ '/assets/images/launch-qgis.png' | relative_url }}' alt="Choosing Project → Open" width='100%' height='100%' />

Navigate to the location of the unzipped sample data. Select the project file (<b>qgis.qgz</b>) and click
 the <b>Open</b> button.

<img src='{{ '/assets/images/open-project-file.png' | relative_url }}' alt="Selecting and opening the project file." width='100%' height='100%' />

The project file will be loaded into QGIS and a map showing Toronto's
neighbourhood boundaries will be displayed.

<img src='{{ '/assets/images/project-initial-view.png' | relative_url }}' alt="Initial view of the QGIS project." width='100%' height='100%' />

## QGIS Interface: Panels
If they're not already open by default, add the <b>Browser</b>, <b>Processing Toolbox</b>, and <b>Layers</b> panels.

• Click <b>View → Panels → Browser</b>.

The <b>Browser</b> panel allows us to view and work with all the components of our QGIS Project.

<img src='{{ '/assets/images/browser-panel.png' | relative_url }}' alt="The QGIS Browser Panel." width='100%' height='100%' />

• Click <b>View → Panels → Processing Toolbox</b>.

The Processing Toolbox gives us access to tools that can analyze and transform our data.

<img src='{{ '/assets/images/processing-toolbox-panel.png' | relative_url }}' alt="The QGIS Processing Toolbox Panel." width='100%' height='100%' />

• Click <b>View → Panels → Layers</b>.

The Layers Panel shows us all data that’s been added to the project. test

<img src='{{ '/assets/images/layers-panel.png' | relative_url }}' alt="The QGIS Layers Panel." width='100%' height='100%' />