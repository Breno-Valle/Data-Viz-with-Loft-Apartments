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
    
   NUMBER OF ROOMS:
   
   A good example to visualize the distributions of rooms on the Loft apartments. Here we can see a pick of apartments with two or three rooms.
    That kind of property could be great for families or couples, but maybe not the best choice for a single person like an academic student.  
   
   ![image](https://user-images.githubusercontent.com/80376071/115778933-b6f29700-a38d-11eb-8f83-051e4f70ed78.png)


   NUMBER OF PROPERTIES PER DISTRICT:
   
   Here i plotted the distribution of apartments in one district,with a pick is between 100 and 150. 
   So if an district have great prices but is under the mean we could think that district it has being UNDERUSED and in the future it could be a good place to invest.
   
   ![overview_distribution](https://user-images.githubusercontent.com/80376071/115736084-636a5400-a361-11eb-92ac-16a3f922f317.PNG)


   PROPERTIES LOCATION:
   
   Here we have a interactive HeatMap, where the red regions are the most concentraded ones, followed by orange, yellow, green and finally blue.
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
   
   RENT- ROOMS AND PRICE: 
   
   As you can see this plot represents the number of apartments per number of rooms in the peoperties have a strong relations with Price.
   As the number of rooms increases the apartments price tends to increase to. But when we look at the apartments with one and two rooms something interesting shos up.
   Apartments with two rooms are, in general, cheaper than that ones with just one room. If you want to recommend an apartment to a potencial client in Loft's website
    maybe could be a good idea display properties with two rooms in place of one when you want low when your client is looking for a low cost purchase.

   ![image](https://user-images.githubusercontent.com/80376071/115779393-51eb7100-a38e-11eb-95b3-e3ed8b5f0d73.png)

   TOP 10 MORE EXPENSIVE DISTRICTS:
   
   High prices per square meter apartments for rent are around 50 and 80 Reais per square meter, and are mainly located in rich and central districts like Iguatemi, Itaim Bibi and Vila Olimpia.
    
   ![rent_top10](https://user-images.githubusercontent.com/80376071/115736567-c4922780-a361-11eb-96fe-ec1ccf154d64.PNG)

   PERCENTAGE OF APARTMENTS WITH ELEVATOR:
   
   ![image](https://user-images.githubusercontent.com/80376071/115780970-308b8480-a390-11eb-8529-a7f52802610b.png)
   
   
   HEATMAP FOR RENT:
   
   On this HeatMap we can we that Loft apartments for rent have a homogeneous distribution acroos the São Paulo city space. This tell us that Loft has a better and secure utilization of the urban space with properties for sale.
   
   ![rent_heatmap](https://user-images.githubusercontent.com/80376071/115736570-c52abe00-a361-11eb-94bb-1320fd4b717c.PNG)
   
   SIX MOST POPULATED DISTRICS AND THE THEIR RESPECTIVE MEAN PRICES
   
   From that graph we can see the districts that have a lot of Loft apartments, the exactly number of properties on them, and their mean prices. From this plot we can figure out which districts generate higher incomes.
   
   ![image](https://user-images.githubusercontent.com/80376071/115745283-aa5c4780-a369-11eb-88ab-6efc2fa16a37.png)

   FEATURE IMPORTANCE:
    
   On that point i used a Machine Learning model to predict the price of the apartments based on the properties features. I used a simple Decision Tree algorithm to do that and then extract wich features had more ipact in the prediction of the price. 
   To do that we needed to cut some outliers from the data, as you can see on those boxplots:
    
   
   Before cut:
    
   
   ![image](https://user-images.githubusercontent.com/80376071/115782034-93315000-a391-11eb-8d48-db5356918a5b.png)

   
   After cut:
    
   
   ![image](https://user-images.githubusercontent.com/80376071/115782099-a7754d00-a391-11eb-9666-ca0cabe95979.png)

   
   Then i trained the a very simple model,  and our predictions tended to get values around 1300 Reais more or less than the real price.
   However with this we could find that the most relevant features that impact on price are the size of the apartments, the condominium price and the features on geographical localization, like Longitude and Latitude.
    

   ![rent_feature_import](https://user-images.githubusercontent.com/80376071/115736642-cf4cbc80-a361-11eb-925f-90f0dc92187c.PNG)


  3-	"Saleable Loft's Location"
      
      The idea here is the same from the above topic, but the main point here is to figure it out the main differences
      between the apartments for sale and apartments for rent. Sales apartments have their own feature characteristics
      and space location.

   NUMBER OF PROPERTIES PER PARKING SPACES ON THEM AND RESPECTIVE PRICES:
    
   The interessant point here is the exponential increases of the prices while the number of parking spaces incresases too.

   ![image](https://user-images.githubusercontent.com/80376071/115744363-e3e08300-a368-11eb-8fd5-4416e2c36ad4.png)
   
   HEATMAP FOR SALE:
   
   In oposition to the Rent HeatMap, i can clearly see the geographical concentration of properties in the center of the city, on consolidated neighbourhood for the Housing Market. That mean the peripheral areas are has a great and untapped potential to be explored.

   ![image](https://user-images.githubusercontent.com/80376071/115784399-6e8aa780-a394-11eb-918d-9d19cd461b30.png)
   
   SIX MOST POPULATED DISTRICS AND THE THEIR RESPECTIVE MEAN PRICES:
   
   ![image](https://user-images.githubusercontent.com/80376071/115784869-12745300-a395-11eb-89e8-ada6bc47b2e5.png)
   
   ALL THE PROPERTIES IN SÃO PAULO:

   On this graph i plotted all the Loft properties in the urban zone of the city acording with their Latitudes and Longitudes. Than, each property were mapped based on the price per area of those apartments. As you can see there is a high number of apartments with high prices in the center of the city, attracting a specific type of client. 
  
   ![image](https://user-images.githubusercontent.com/80376071/115785940-89f6b200-a396-11eb-8e8e-6a1f8145016e.png)

  
  4-	"FINAL"
      
      On this short and final topic we just get the overview about the potencial gain in Reais (local money) that each type of 
      property could be owned by Loft in the next five years.

   ![image](https://user-images.githubusercontent.com/80376071/115746188-81888200-a36a-11eb-8a81-ffd6ede74544.png)

4- Final Thoughts:

   This project can provide a benefit the to business with a better understanding of the Loft situation in São Paulo and providing insights to the future steps of the company.
   Of course there is a lot of good explorations that could be done and an infinity of ideas that could come from it.
   If you get interested by this dataset, project or ideas contact me, i will be glad to help you, and feel free to use all the notebook if you want.


