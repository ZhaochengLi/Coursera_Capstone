## Capstone Project Report
### On clustering and exploring the neighborhoods of *Toronto* and *New York city*
#### Name: Zhaocheng Li

### 1. Introduction
#### 1.1 Interests
Toronto and New York city are ones of most modern and international cities in the world, and their population and scales grow rapidly. They are all the economical capitals of their respective contries(CANADA/USA). However, the distance between them are suprisingly closer than most people think. It taks only an hour flight to arrive from one to another.

But, it is not common to have two world-class metropolises that are close to each other like Toronto and NYC, in terms of closegeographical distance. Which makes me wonder, is it possible for Toronto and NYC to have more similarities? The similarities/dissimilarities can be discussed in fields of population distribution, personal wealth distribution, shops distribution, and race distribution, etc..

#### 1.2 Business problems
Many business problems will rise after this problem. Once we understand the similarities/dissimilarities of neighborhoods of  Toronto & of NYC, we can reveal some very important characteristics such as multiculture(races/languages), population distribution and income per capital differential. The stakeholders can decide the optimized location for business based on these factors.
For example, if we want to open a chinese restaurant, we want to choose a location not just in a business district, but most importantly, a location with a high asian population, and maybe with big asian markets.

### 2. Data acquisition and cleaning
#### 2.1 Data acquisition
To accomplish this project, we acquire datasets from many sourses:
1. [Foursquares API](https://foursquare.com/), where are scrape accurate location data of vanues for exploration.
2. [List of postal codes of Canada: M from Wikipedia](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M), where we obtain the info about boroughs and neighborhoods of Toronto. This dataset will be converted into pandas dataframe and used for exploring neighborhoods around Toronto.
3. [NYC geo location data from IBM](https://cocl.us/new_york_dataset). Similarly, we will use this JSON file to load NYC boroughs/neighborhoods dataset and explore it.

These are all start-up datasets we collect online. As the project going through we will generate more datasets used for research. They will be mentioned and explicitly explained during the project.

#### 2.2 Data cleaning
After acquiring the datasets, we clean and format the datasets into the *pandas* dataframes. 
- `df_toronto`, the source dataset for the location data of Toronto, including columns:
![df_toronto](./data/df_toronto.png)
 - `Borough`, borough name
 - `Neighbourhood`, the neighbourhood name
 - `Latitude`, the latifude of the the neighbourhood location 
 - `Longitude`, the longitude of the neighbourhood location
 
- `df_nyc`, the source dataset for the location data of New York city, including columns:
 ![df_nyc](./data/df_nyc.png)
 - `Borough`, borough name
 - `Neighbourhood`, the neighbourhood name
 - `Latitude`, the latifude of the the neighbourhood location 
 - `Longitude`, the longitude of the neighbourhood location

- `dft`, the source dataset population details and economy information of Toronto.
![dft](./data/dft.png)

- `dfn`, the source dataset population details and economy information of NYC.
![dfn](./data/dfn.png)

### 3. Methodology
Using the **Foursquare API** we can careate maps of neighborhoods for both Toronto and NYC:  

**Toronto**
![map_toronto](./data/map_toronto.png)

**NYC**
![map_nyc](./data/map_nyc.png)

And we can also get the top ten vanues for each neighborhood for both cities:  
**Toronto**
![top_ten_venues_toronto](./data/top_ten_venues_toronto.png)

**NYC**
![top_ten_venues_nyc](./data/top_ten_venues.png)

And our main focus is by applying **machine learning: clustering**, and k-means cluster, we want to get the clusters of neighborhoods of two cities.

**Toronto clusters**
![toronto_clusters](./data/map_toronto_clusters.png)

**NYC clusters**
![nyc_clusters](./data/map_nyc_clusters.png)

And another topic we interested is the information about multiculture, income, population.

We can accomplish this by cleaning and formatting datasets `dfn`, `dft`:

**Toronto data**
![toronto_data](./data/toronto_data.png)

**NYC data**
![nyc_data](./data/nyc_data.png)

### 4. Results & Discussion
Based on all kinds of analysis plots, we can have varioud observations by comparing the performance of neighborhoods of Toronto and NYC

1.  It can be noticed that Toronto has one big cluster and a smaller one, while others are insignificant compared to them. As for NYC, there are two big and one mid size clusters, while other two clusters are insignificant compared to them. Therefore, we see Toronto seems to have more uniform neighborhood type.  New York has much more varieties. So, the two cities are different in terms of segmentation.

2. NYC and Tronto are similar in population, around 7 million, more or less, and the race ratios are also similar.

3. for the incomes, there are realtively big differential between boroughs for each city. In toronto, the people working in central toronto areas has 2 or 3 times more income than incomes of prople from other boroughs. Meanwhile, in NYC, prople in Manhattan earn dramatically more than people from other area. For example, people in Manhattan earn round 320,000 USD per capital, while people in Brooklyn earn 30,000 USD per capital.

### 5. Conclusion
Therefore, from my research, Toronto and NYC are different in segmentation, but they are similar in multiculture, population and income distributions.

**This research still need more work to be done. Thank you very much for reviews and advices!**
