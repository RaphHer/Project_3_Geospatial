# Project_3_Geospatial

Hi you! 

Welcome to my GeoSpatial Data Project or my third project at Ironhack. 

In this challenge, I am looking for an office for a newly created company. To approach the problem, I chose option A and decided to "steal" the current venue of an existing company. 

Ah... and yes, before I forget, the country I chose to look for an office in is France.

#startup_nation 

![](images/beret_baguette_wine_dog.jpg)

You will find 5 Jupyter Notebooks that are divided as follow:
1. Mongo Queries - I used a company database to find gaming companies from which I could steal their offices, but also start-ups that raised above $1m and advertising companies (as no design companies were in the DB)
2. Foursquare API - I did multiple Foursquare queries to find locations close to the companies, namely kindergarten, Starbucks, vegan restaurants, dog hairdressers, basketball court, music venues and airports
3. Visualisation - Once I retrieved information from the database and Foursquare, I plotted everything on a map
4. Finding the perfect office - this is where it got nasty. Based on the visualisation I made, I chose four companies, namely: 
   - Weird 
   - Media Stroika
   - Betklub 
   - Yoowalk  
  Then I looked at the distance of these companies to the different interest points mentioned above and applied some weight to find the company I wanted
5. Finally, I plotted a map based on the company I chose for the different points. 


**Mongo Queries**

Creation of 3 data frames: 
- Gaming Companies in France 
- Advertising Companies in France
- Successful startups (raised amount: above $1m)

What I founded after having a closer look is that an important part of the companies are located in the Paris. Therefroe, I will make my Foursquare API on the Paris location.

**Foursquare API**

Creation of multiple data frames using the Foursquare API. 
-  Kindergardens
-  Starbucks
-  Vegan restaurants
-  Dog Hairdressers 
-  Basketball courts 
-  Music venues 

My first big mistake is here as I based on the queries on the Paris location. This way, I add only things located close to the centre of Paris and not centred on the gaming companies. In addition, I should have enlarged the number so that I don't automatically receive o
nly ten results 

**Visualisation**


To begin with, a beautfiul empty map  
![](images/01.%20Empty%20Map%20.png)


And now with some gaming companies with a focus on Paris (as this is where they are concentrated)

![](images/02.%20Gaming%20companies%20.png)

Adding the successful startups and advertising companies (final image with the Mongo DB)

![](images/03.%20View%20from%20Paris%20end%20of%20Mongo%20queries%20.png)

Adding the different locations retrieved from Foursquare

![](images/04.%20Final%20view%20.png)

And final view with the two international airports located close to Paris 

![](images/04.%20Final%20view%20with%20Airports.png)

**Finding the perfect office**
Based on the visualisation above I took 4 companies and tried using a math formula to solve the problem and find the best possible location ![](images/witches%20meme.jpg)

The companies that I choosed are: 
- Wevod
- Media Stroika 
- Betklub 
- Yookwalk 
  
  ![](images/05.%20Final%20score.png)

  To calculate the final score I calculated the distance between the nearest place of each category and a company. Then I applied weight to each of the category (applying a low weight being positive as I want to minimize the final score).

  => AND THE WINNER IS Media Stroika 

  ** The Perfet Office ** 


Finally, I plotted the office and the point of interest on a map. Based on the visualisation above, I took four companies and tried using a math formula to solve the problem and find the best possible location 
![](images/06.%20Media%20Stroika.png)