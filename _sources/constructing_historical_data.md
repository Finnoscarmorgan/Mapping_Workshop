# (Re)Constructing Historical Data: Colonial Australian Bushfires

### 1. Building Historical Bushfire Data from Trove

```{image} /images/Voronoi_Fire.png
:alt: map
:class: bg-primary mb-1
:width: 500px
:align: center
```

The historical bushfire dataset is derived from over 5000 newspaper 
articles mentioning bushfires harvested from Australian newspapers across the 19th century. Placenames in each article
that occur within a 200 character count of the word bushfire have been extracted and geo-located using the Australian 
National Survey of Australian Placenames.  This character proximity yields a strong, if unqualified, relationship between
place and disaster.  Accordingly, this dataset represents places associated with historical bushfires; whether they are 
directly affected or only proximate to the event. Further the temporal element of this dataset represents not the event
itself, but public response, given that the date ranges are extracted from date of publication.  While acknowledging the
heavily curated and conditional ontology of this dataset, the demonstrated relationship between place and event establishes 
a viable foundation for comparative analysis with other geospatial datasets.


**Approach**
1. Devise search strategy
2. Validate Search Strategy
3. Apply Data Pipe-Line
4. Visualise Results

 ### 2. Tools
1. **Retrieving Data from Trove:**
    * [Trove Harvester:](https://glam-workbench.net/trove-harvester/)
    Queries Trove API and formats results into a csv with relevent meta-data categories. Requires some familiarity with the command line and installation of Python.
2. **Processing Text to Extract Named Entities:**
    * [Recogito:](https://recogito.pelagios.org)
    Wonderful web application that encompasses an entire geospatial pipe-line. Recogito extracts Named Entities from text, and geo-codes LOCATION entities using a diversity of different Gazeteers. Unfortunately, Gazeteers privelige European historical research and are not much use for the Australian context. Recogito outputs data in handy csv that you can update yourself. 
    * [Australian Text Analytics Platform Geolocation Notebook:](https://github.com/Australian-Text-Analytics-Platform/geolocation-tools-workshop)
    A Jupyter notebook that identifies LOCATION  entities in Marcus Clarke's novel For the Term of his Natural Life. This text can be substituted for any other text by user, however, will require some rudimentary familiarity with Python language, Jupyter Notebooks. 

3. **Generating Location Coordinates for Australia**
    * [Gazeteer of Historical Australian Placenames:](https://www.tlcmap.org/ghap/)
    Most comprehensive online Australian location database. Recently an API was added. Mostly requires you to manually look up locations. 

### 3. Limitations and Considerations

- What and who isn't represented?
- Whose story is being told?
- How 'complete' is the data?



