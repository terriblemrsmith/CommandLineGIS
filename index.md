## American Housing Co-op Landscape

Here's a test run at this website

<iframe src="UHAB_Coops.html" height="855" width="95%"></iframe>

You can explore this map [as its own web page here](UHAB_Coops.html).


  This map seeks to do a few things
  * Geocode addresses compiled into the UHAB database
  * Provide background on geocoding reliability through icon design
  * Show clustering
  * Show target variables in the contexts that the Housing Coops exist in, as a proxy for the coops themselves (UHAB's concept)


### Tell us where you found your dataset, where you found it and why you're interested in geocoding it.

In the summer I worked with a few others under Professor DeFilippis on a Shared Equity Housing Landscape analysis. Part of this utilized UHAB's database of housing cooperatives across North America. In a meeting, they mentioned they wanted more demographic information outside of NYC for granting/funding purposes. Hence, I'm interested in tying up this loose end and returning some labor in exchange for their data.

### What format were they in? Who prepared them?
UHAB's data base is a list of addresses for American and Canadian housing co-operatives. Let's geocode it! 
[See code here](https://colab.research.google.com/drive/1jj0DgActHHLM-YTbtqb7WYdccLrBhnIj?usp=sharing)


### Were there any issues with data quality that you had to address?

The column "data source" expresses that it has been sourced by multiple partners. As such the data was not standardized. I began by standardizing the data - creating  After running it through the geocoder, I used the ESRI_Quality field to parse out which rows I had to manually clean. I then reuploaded the data, geocoded it again to ensure that the data being used was as good as possible


### Did you have to do anything to make the data mappable?

In addition to geocoding the points, in order to achieve UHAB's objective we had to gather census tract and blockgroup level data. Two big objectives with this


1.   As an output item the UHAB database with census fields. Because there were no GEOID features associated with the original dataset, to do this we had to do a spatial join of tract & block polgygons to housing coop points. Once this spatial join was achieved, we could do table joins by GEOID feature class
2.   A set of maps showing neighborhood variables of interest with housing coop location points over laid ontop of them. 




![2019 Percentage Black Population In Hennepin County MN by Tract](2019 Percentage Black Population In Hennepin County MN by Tract.png?raw=true)
![2019 Median Income In Hennepin County MN by Tract](2019 Median Income In Hennepin County MN by Tract.png?raw=true)
