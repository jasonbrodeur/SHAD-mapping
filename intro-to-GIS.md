---
layout: default
title: Intro to GIS
nav_order: 3
---

*Before starting this section, make sure you've completed all tasks in the [Preparation](preparation) page.*

# Introduction 
In this first lesson, you will get a quick introduction to the QGIS interface. QGIS is the world's most popular open source GIS software. It is incredibly powerful and can do all sorts of interesting visualizations and analyses. The primary challenge with this much functionality is that you have to learn what the buttons do and understand the terminology. We'll work on that here. 

## Task 0: Download your data  
In this exercise, we'll learn how to use QGIS by using data that is available from the City of Hamilton [Open Data Portal](https://www.hamilton.ca/city-initiatives/strategies-actions/open-data-program). The open data portal has a wide variety of numeric and geospatial data sets that are free and open to use. Many cities and regions now have similar kinds of open data portals, so be sure to check if you're ever doing analyses on your local area!

To download the data: 
- Download ```hamilton-data.zip``` from the [workshop GitHub repository](https://github.com/jasonbrodeur/SHAD-2022/blob/main/data/hamilton-data.zip), or click [this link](https://github.com/jasonbrodeur/SHAD-2022/raw/main/data/hamilton-data.zip) to download it directly.
- Download the data into the directory that you want to use for this workshop (i.e. know where you saved the file and use a folder where you can read/write data)
- **UNZIP THE FILE**. This is very important--otherwise, weird things are going to happen for you.   

## Task 1: Learn the interface; Add and explore data
**Objective**: Explore the user interface 
- Open QGIS. 
- Listen to Jay as he introduces the important buttons and panels of the QGIS interface. 
- Go to ```Project>Properties``` and set your project Coordinate Reference System (CRS) to ```NAD83 / UTM zone 17N [EPSG:26917]```. 
	- Check the box to “Enable on-the-fly CRS transformation”
- Find your downloaded and unzipped data using the **Browser panel**.
- Add a number of vector layers from the downloaded City of Hamilton data by dragging the shapefile (.shp) into the data frame (large window). Be sure to include at least the ```Street_Centreline```, ```Buildings```, and ```Educational_Institutions``` layers. Add some more!
- Explore the attribute tables of these layers (Right-click on a layer in the **Layers panel** and select ```Open attribute table```.
- Save your project: >Project>Save As… [this saves a project file with an extension .qgs]. Give your project file a meaningful name.
	- Note that project files do not resave your layers--it simply preserves the links to the loaded layers, as well as any custom layer styling you’ve used.

## Task 2: Style vector layers 
**Objective**: Style your vector layers to create a map of a neighbourhood or area of Hamilton. 
- Add/remove layers from the Open Hamilton Data folder as necessary or desired. Keep ```Street_Centreline``` and ```Buildings```, and be sure to add all other relevant layers. 
- Move layers up and down in the **Layers panel**, note how it effects the drawing order.
- Style the layers by navigating to the **Style** tab of the Properties dialog box (double click the layer or right click and select ```Properties```).
- Follow along with Jay’s instruction on styling vector layers. Then, experiment on your own. 
- See [this YouTube video](https://goo.gl/MEyCrD) and some other videos by Klas Karlsson for ideas on custom vector styling.

## Task 3: Add labels to layers
- Select the ```Street_Centreline``` layer and click on the **Layer Labeling Options** button 
- In the top dropdown menu, select ```Single Labels```
- In the ```Value``` dropdown menu, select the ```STREET_NAM``` field. Click **Apply**.
- Explore the tabs for labeling options
	- In the **Text** tab, adjust the font type, size, colour (if desired).
	- If interested, experiment with the options in the **Formatting** tab.
	- In the **Buffer** tab, check to turn on ```Draw text buffer```.
	- In the **Rendering** tab, reduce the number of labels on the map by checking ```Merge connected lines to avoid duplicate labels```.
- Use a rule to more finely control which road labels are shown: 
	- In the **Rendering** tab, go to the ```Data defined``` section and select the dropdown beside ```Show label```. In the dropdown, select ```Edit```
	- In the ```Expression``` box, enter: ```ROAD_TYPE like 'Major'```. Click OK.
	- Note that the labels are now only applied to the major roads. 
	- Keep this setting, or remove it by reclicking the dropdown and selecting ```Clear```.

## Task 4: Save your project file 
- Click the **Save** button to save your changes. 

**All done?** Let's move on to your [second lesson](mapping-our-data), where we will map our newly-collected data!
