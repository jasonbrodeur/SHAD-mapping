---
layout: default
title: Mapping our data
nav_order: 4
---

*Before starting this section, make sure you've completed all tasks in the [Preparation](preparation) page and completed [lesson 1: Intro to GIS](intro-to-GIS).*

# Introduction 
In this lesson, you will build on the skills gaimed during [lesson 1], to create a map that shows the outcome of our outdoor spaces assesment. 

## Task 1: Open a new project, add a plugin and a web base map
- Open a new project. Set the project CRS to ```EPSG 3857: WGS84 - Pseudo Mercator projection```
- In this next step, we want to add a web map as a base map upon which to show our data. To do this, we need to install a plugin from the built-in plugin manager
	- As an open-source project QGIS has a lot of community-contributed Plugins that extend its functionality. Over time, many of these plugins find their way into the core software.
- Install the QuickMapServices plugin:
	- In the top menu bar, click on ```Plugins > Manage and Install Plugins```.
	- In the Plugins dialog box, search for and install the **QuickMapServices** plugin. 
<img src="assets/img/quickmap-plugin.png" alt="QGIS Plugin window" width="500" style="border: 1px solid darkgrey">
	- To allow us to add additional web layers, on the top menu, click ```Web > QuickMapServices > Settings```. Go to the **More Services** tab and click **Get contributed pack**. Close the window.
<img src="assets/img/get-contributed-pack.png" alt="QMS settings dialog box" width="300" style="border: 1px solid darkgrey">
	- While the Plugin window is open, also install the **qgis2web** plugin.
	- Once the plugins are installed, close the plugins window.
- Add a web base map to your data frame: 
	- In the top menu bar, click on ```Web > QuickMapServices```.
	- Explore and add a base map of your liking. 
Choose a web map for your base map (e.g. check out the OSM, Stamen, and CartoDB maps)
	- Be sure to right-click and ```Remove Layer``` for any layer you don't want to use. 


