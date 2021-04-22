# Data-Viz-with-Loft-Apartments
Data visualization from São Paulo Loft Properties (Housing Market)  


1-IDEA OF THE PROJECT
  
  Loft is a digital plataform that uses tecnology to simplify the 
  purchase and the sale of properties fast and easy. Above it, i 
  created these project to analyze and brings the Loft data to our eyes.
  In that way i imagine two problems that could apper into their busness.
  
  Those questions are:
        
        1-What are the features that compose the Loft properies?
        2-How those Loft properties are distributed in São Paulo city
          and how the apartment's price are related to that ?
  
  So let's take a look on how we could answer those issues with data visualization
  (using python)


2-ABOUT THE DATASETS

- sao-paulo-properties-april-2019:

  This dataset was taken from kaggle and you can find it here:
  
  https://www.kaggle.com/argonalyst/an-lise-business-case-ds-loft/notebook?select=sao-paulo-properties-april-2019.csv
  
  Or you can download it from this repository: "sao-paulo-properties-april-2019.csv"

  The data contained in that dataset is pretty clean, and do not need to much data cleaning. 
  Also it hasn't missing values. In fact that dataset is pretty easy to use and a great oportunity to focous on the Data Viz
  (if you want to see a lot of Data Cleaning you can go to this notebook: 
  
  https://github.com/Breno-Valle/LowCostAirbnb)

- sp_metrop.geojson
  This Dataset, on GeoJSON format, is the collection of the geographical coordenates of São Paulo urban zone boundaries.
  It Saves each point acording to Latitude and Longitude.  
  It was taken of this Repository:
  
  https://github.com/nucleo-digital/sp-mapas
  
  who extract São Paulo public data from the São Paulo City Hall website.
  He did a great job.


3-ABOUT THE PROJECT
 
  For purpose of turn this project into a simple way to understand the Loft properties in São Paulo city
  i divided my notebook in four main blocks:
      
      (those pictures are only a small part of the hole process. Go to the notebook for more graphs, insights and workflow process)
      
  1-	"Overview by all the Loft properties"
    
    Here we can go through an overview of all the Loft properties. Their distribution across the spaces of the city,
      the number of properties in each district and some important features to discribe those apartments.
    
   A good example to visualize the distributions of rooms on the Loft apartments. Here we can see a pick of apartments with two or three rooms.
    That kind of property could be great for families or couples, but maybe not the best choice for a single person like an academic student.  
   ![overview_parking](https://user-images.githubusercontent.com/80376071/115735904-39189680-a361-11eb-9b17-b4d7a480e134.PNG)

   Here i plotted the distribution of apartments in one district,with a pick is between 100 and 150. 
   So if an district have great prices but is under the mean we could think that district it has being UNDERUSED and in the future it could be a good place to invest.
   ![overview_distribution](https://user-images.githubusercontent.com/80376071/115736084-636a5400-a361-11eb-92ac-16a3f922f317.PNG)

   
   Here we have a HeatMap, where the red regions are the most concentraded ones, followed by orange, yellow, green and finally blue.
   The red regions are located in the center of the city, where there is a very competitive market, in neighbourhoods like Santa Cecília and República.
   In the other hand, there is few Loft properties in the periferical zone of the city, we're going to dive deeper in those districts after, that could be 
   a potential market.
   
   ![overview heatmap](https://user-images.githubusercontent.com/80376071/115736203-7b41d800-a361-11eb-8eb7-8663946e2421.PNG)


  2-	"Rentable Loft's Locations"
      
      As you can imagine, apartments for sale and the ones for rent have a really different characteristics,
      with the main one being the price. Here we dive into the main features of the apartments for rent. 
      Their spacial location, relationship between Geographic location and price and top 10 districts 
      with most apartments and their mean price, top 10 more expensive districts and top 10 cheaper districts
      by price/m2. 	
      
   ![rent_suite](https://user-images.githubusercontent.com/80376071/115736406-a62c2c00-a361-11eb-8b14-d55354d2e582.PNG)

   ![rent_top10](https://user-images.githubusercontent.com/80376071/115736567-c4922780-a361-11eb-96fe-ec1ccf154d64.PNG)

   ![rent_per_elev](https://user-images.githubusercontent.com/80376071/115736439-ac220d00-a361-11eb-8bcd-147ec00af362.PNG)

   ![rent_heatmap](https://user-images.githubusercontent.com/80376071/115736570-c52abe00-a361-11eb-94bb-1320fd4b717c.PNG)
   
   ![image](https://user-images.githubusercontent.com/80376071/115745283-aa5c4780-a369-11eb-88ab-6efc2fa16a37.png)

   ![rent_feature_import](https://user-images.githubusercontent.com/80376071/115736642-cf4cbc80-a361-11eb-925f-90f0dc92187c.PNG)


  3-	"Saleable Loft's Location"
      
      The idea here is the same from the above topic, but the main point here is to figure it out the main differences
      between the apartments for sale and apartments for rent. Sales apartments have their own feature characteristics
      and space location.

   ![image](https://user-images.githubusercontent.com/80376071/115744363-e3e08300-a368-11eb-8fd5-4416e2c36ad4.png)
   
   ![image](https://user-images.githubusercontent.com/80376071/115744578-112d3100-a369-11eb-9294-b9ae18bb1302.png)

   ![image](https://user-images.githubusercontent.com/80376071/115744735-37eb6780-a369-11eb-9b76-7ca168fe697b.png)

   ![image](https://user-images.githubusercontent.com/80376071/115744877-55203600-a369-11eb-9fff-cf63d7466d30.png)

   ![image](https://user-images.githubusercontent.com/80376071/115745426-cbbd3380-a369-11eb-8d03-633aeac3ab27.png)
   
   ![image](https://user-images.githubusercontent.com/80376071/115745776-222a7200-a36a-11eb-85e7-214ddf624aeb.png)

   ![image](https://user-images.githubusercontent.com/80376071/115746085-69186780-a36a-11eb-809b-30a3b2a6a228.png)

  
  4-	"FINAL"
      
      On this short and final topic we just get the overview about the potencial gain in Reais (local money) that each type of 
      property could be owned by Loft in the next five years.

   ![image](https://user-images.githubusercontent.com/80376071/115746188-81888200-a36a-11eb-8a81-ffd6ede74544.png)



