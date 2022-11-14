# (Re)Constructing Historical Data: Colonial Australian Bushfires

### Building Historical Bushfire Data from Trove


```{figure} /images/Bushfire_Map_Pipeline.png
---
width: 500px
align: center
name: directive-fig-fire-pipeline
---
Link from URL to newspaper article in Trove
```
1. Devise search strategy
2. Validate Search Strategy
3. Apply Data Pipe-Line
4. Visualise Results

### Tools
1. **Retrieving Data from Trove:**
    * [Trove Harvester](https://glam-workbench.net/trove-harvester/)
    Queries Trove API and formats results into a csv with relevent meta-data categories. Requires some familiarity with the command line and installation of Python.
2. **Processing Text to Extract Named Entities:**
    * [Recogito](https://recogito.pelagios.org)
    Wonderful web application that encompasses an entire geospatial pipe-line. Recogito extracts Named Entities from text, and geo-codes LOCATION entities using a diversity of different Gazeteers. Unfortunately, Gazeteers privelige European historical research and are not much use for the Australian context. Recogito outputs data in handy csv that you can update yourself. 
    * [Australian Text Analytics Platform Geolocation Notebook](https://github.com/Australian-Text-Analytics-Platform/geolocation-tools-workshop)
    A Jupyter notebook that identifies LOCATION  entities in Marcus Clarke's novel For the Term of his Natural Life. This text can be substituted for any other text by user, however, will require some rudimentary familiarity with Python language, Jupyter Notebooks. 

3. **Generating Location Coordinates for Australia**
    * [Gazeteer of Historical Australian Placenames](https://www.tlcmap.org/ghap/)
    Most comprehensive online Australian location database. Recently an API was added. Mostly requires you to manually look up locations. 
