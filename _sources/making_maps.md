# Making Maps in Kepler.gl

Today we'll learn how to build three different kinds of maps that answer different research questions:
* A time-series map 
* A network map
* A cluster map

We will use our bushfire dataset to build these maps. 

## 1. Getting the data

Today we'll work with the bushfire dataset. This can be downloaded using the following link: [Link to bushfire dataset](https://drive.google.com/file/d/1F6hGmtRJ9ZTbqq7cgcwbXeUJFNvkU8AG/view?usp=sharing)

* Click on the download icon at the top-right hand corner of your screen. You should see **'Bushfire_Dataset.csv'** in your downloads folder. 
* Open a web-browser and navigate to [Kepler.gl](https://kepler.gl/demo) 
* Click **'get started'** and click on the **'browse your files'** link once you see the pop-up below. Navigate to your Downloads folder and upload **'Bushfire_Dataset.csv'** to Kepler.gl.

```{image} /images/Add_Data_to_Map.png
:alt: map
:class: bg-primary mb-1
:width: 500px
:align: center
```
* Kepler will automatically read the csv document to identify information about latitude and longitude and then visualise these points on the map canvas. Your map should look like the screenshot below.

```{image} /images/Kepler_upload.png
:alt: map
:class: bg-primary mb-1
:width: 500px
:align: center
```

`````{admonition} Getting Used to the Mapping Interface
:class: tip
You're probably familiar with other mapping interfaces such as Google Maps. Take a moment to familiarise yourself with the functionality of Kepler.gl. Trying zooming in and out. Try hovering over one of the points, what information is shown?
`````

## 2. Making a Time-Series Map
The first map we wils make is a time-series map, we will also enable some functionality to improve the legibility of the data. 

* **Step One:** First, let's explore our dataset. 
    * Click on the **Layers icon** in the toolbar (it's the icon with the stacked diamonds). 
    * Hover over the item **'Bushfire_Dataset.csv'** underneath the **'Datasets' heading**. You should see see two icons appear: a trash-can on the right and another icon that says **'Show data table'** Click on this icon. 

```{image} /images/Explore_Kepler_Datatable.png
:alt: map
:class: bg-primary mb-1
:width: 500px
:align: center
```
*  **Step Two:** In the first map that we make we want to be able to visualise incidence of bushfires over time, and provide some additional contextual material so the viewer can navigate back to the original newspaper article. The fields that are relevent for our pruposes are:
    * Placename
    * Longitude and Latitude
    * Newspaper
    * Title
    * Date
    * URL

```{image} /images/Data_Table.png
:alt: map
:class: bg-primary mb-1
:width: 500px
:align: center
```

`````{admonition} Data Types
:class: tip
You will notice that Kepler.gl has assigned different colours to the column names.  This is an indication that it is recognising different data-types. Importantly, the 'Date' column is green, this indicates that the data is in the correct date format for visualisation.  Kepler.gl is very fussy about the format the format of the time data. Preferably the format should be 'YYYY-MM-DD 0:00'

`````
* **Step Three:** If we navigate back to the map interface you will see that Kepler.gl has already generated some options for visualisation in the Layers Section.  
    * Navigate to the 'Interactions' tab at the top of the toolbar. We can now change what information is displayed on the map by adding and removing variables from the 'Tooltip' section. Add the variables: Placename, Newspaper, Date, Title and URL

```{image} /images/Tooltip.png
:alt: map
:class: bg-primary mb-1
:width: 500px
:align: center
```
* If you hover over the points on the map you will now see our chosen information displayed. The URL has automatically been rendered as a hyper-link and can be used to navigate back to the source material. 

```{figure} /images/Tooltip_Interaction.png
---
width: 500px
align: center
name: directive-fig
---
Image of pop-up on map
```

```{figure} /images/Bushfire_Article_Link.png
---
width: 300px
align: center
name: directive-fig
---
Link from URL to newspaper article in Trove
```

* **Step Four:** 
    * To add a time-line to our map, click on the **'Filters'** icon at the top of the Kepler.gl toolbar. 
    * Then click on the button that says **'Add Filter**. 
    * Scroll down and select **'Date'** in the **'Select Field'** drop- down menu. Once selected you should now see a time-line appear at the bottom of the screen. 
    * To animate the time-line select the play button 

```{figure} /images/Timeline.png
---
width: 500px
align: center
name: directive-fig
---
Timeline
```

## 3. Saving and Sharing Our Map

`````{admonition} Downloading and Sharing your Map
:class: Warning!
Kepler.gl is a client-side application, meaning it is running locally on your computer. In order to save and share our maps we are required to take a few extra steps. Kepler.gl allows you to download your map in the following formats as a JSON file or an HTML file.  


`````

### 3.1 Saving our Map 

Click on the **Share** icone at the top of the toolbar then click on **Export Map**
* **Download JSON**: Selecting this option saves bothe the data and the configuration settings of the map. If we wish to make further changes to our map we can load this file directly back into Kepler.gl
* **Download HTML**: Selecting this option converts our map to HTML meaning it can be embedded directly on a website. Once you download the map as HTML you will not be able to make any further changes. 
* **Export Images**: Kepler also allows you to take high quality pictures of your map using the **Export Image** functionality. 

`````{admonition} Capturing Images of your Map
:class: Tip!
If you are interested in sharing images your map it is advisable to also download a JSON copy of your map so you can reproduce and make any future alterations as needed.  
`````

### 3.2 Sharing our Map using Dropbox
We can use [Dropbox](www.dropbox.com) to temporarily host our map and generate a URL to be shared with others. 
* Sign in to your Dropbox account on the web
* In Kepler.gl download a copy of your map as an HTML document
* Upload this document to your Dropbox account
* Click on **'Copy Link'** within your Dropbox account. This should generate a unique URL.
 

## 4. Making a Network Map

`````{admonition} Starting a New Map
:class: Tip!
You may want to delete and re-load the dataset at this stage as generating multiple layers with different functionalities can become very computationally expensive!  
`````

The second map we will make is a a network map.  

* Navigate back to the **Layers** tab on the Kepler.gl dashboard. You will notice a number of **Layers** have already been identified by Kepler.gl. 
* The third layer down should be titled **'point -> newspaper arc'**. Click on the **layer settings** icon (small arrow pointing down).
* Click on the **eye icon** to show the layer. 

## 5. Making a Cluster Map

The last map we will make is a cluster map. 

* You may wish to begin a fresh map by deleting and re-loading the bushfire dataset. Then click **add layer** from the **Layers** tab. A new layer will appear down the bottom of the tool-bar. 
* Click on **layer setting** (the little downward pointing arrow) and select **Cluster** from the first drop-down menu.
* Set the **latitude** and **longitude** columns from the dataset as the **lat** and **lon** column inputs for the map. Some cluster should now appear!

`````{admonition} Can't see your data?
:class: tip
If you can't see your data make sure the layer is visible in the map settings. There's a little icon of an eye that should not be crossed out. 

`````
* Play around with the radius settings for the clusters. To challenge yourself add a time-series to the map.

```{figure} /images/Bushfire_Cluster.png
---
width: 500px
align: center
name: directive-fig-bushfirecluster
---
Bushfire Cluster Map
```



