# Applied-DataScience-Capstone
<h1>Description</h1>

Data practitioners are in high demand since one of the hottest occupations nowadays is data science. Anyone who is interested in gaining knowledge and expertise to pursue a career in data science or machine learning should obtain this professional certificate from IBM.

This program's Ten courses cover a wide range of data science topics, including open source tools and libraries, methods, Python, databases, SQL, data visualisation, data analysis, and machine learning. These courses will equip you with the most recent job-ready skills and approaches. You will get hands-on practise utilising actual data science tools and real-world data sets in the IBM Cloud.



<h1>Executive Summary</h1>

<b>Summary of methodologies</b>
1. Data Collection through API
2. Data Collection with Web Scraping
3. Data Wrangling
4. Exploratory Data Analysis with SQL
5. Exploratory Data Analysis with Data Visualization
6. Interactive Visual Analytics with Folium
7. Machine Learning Prediction

<h1>Project background and context</h1>
Space X advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because Space X can reuse the first stage. Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against space X for a rocket launch. This goal of the project is to create a machine learning pipeline to predict if the first stage will land successfully.

<h1>Methodology</h1>

<h1>DATA COLLECTION METHODOLOGY:</h1>

1. Data was collected using SpaceX API and web scraping from Wikipedia. 

2. Perform data wrangling

    a. One-hot encoding was applied to categorical features
    
3. Perform exploratory data analysis (EDA) using visualization and SQL

    a. The table was created on Ibm-db2 database and was connected to Jupyter notebook
    
4. Perform interactive visual analytics using Folium and Plotly Dash

5. Perform predictive analysis using classification models

    a. How to build, tune, evaluate classification models

<h1>DATA COLLECTION</h1>
The data was collected using various methods:

1. Data collection was done using get request to the SpaceX API.

2. Next, I decoded the response content as a Json using .json() function call and turn it into a pandas dataframe using .json_normalize().

3. It was then cleaned, checked for missing values and fill with missing values where necessary.

4. In addition, I performed web scraping from Wikipedia for Falcon 9 launch records with BeautifulSoup.

5. The objective was to extract the launch records as HTML table, parse the table and convert it to a pandas dataframe for future analysis.

<h1>DATA COLLECTION WITH SPACEX API</h1>

1. I used the get request to the SpaceX API to collect data, clean the requested data and did some basic data wrangling and formatting.
<h1>DATA COLLECTION WITH WEBSCRAPPING</h1>

- I applied web scrapping to webscrap Falcon 9 launch records with BeautifulSoup

- I parsed the table and converted it into a pandas dataframe.

<h1>DATA WRANGLING</h1>

- I performed exploratory data analysis and determined the training labels.

- I calculated the number of launches at each site, and the number and occurrence of each orbits

- I created landing outcome label from outcome column and exported the results to csv.

<h1>EDA WITH DATA VISUALIZATION</h1>

1. I explored the data by visualizing the relationship between flight number and launch Site, payload and launch site, success rate of each orbit type, flight number and orbit type, the launch success yearly trend.

<h1>EDA WITH SQL</h1>

- I loaded the SpaceX dataset into IBM-db2 database and later connected it to jupyter notebook

- I applied EDA with SQL to get insight from the data. I wrote queries to find out for instance:

  a. The names of unique launch sites in the space mission.

  b. The total payload mass carried by boosters launched by NASA (CRS)

  c. The average payload mass carried by booster version F9 v1.1

  d. The total number of successful and failure mission outcomes

  e. The failed landing outcomes in drone ship, their booster version and launch site names.

<h1>BUILD AN INTERACTIVE MAP WITH FOLIUM</h1>

1. I marked all launch sites, and added map objects such as markers, circles, lines to mark the success or failure of launches for each site on the folium map.

2. I assigned the feature launch outcomes (failure or success) to class 0 and 1.i.e., 0 for failure, and 1 for success.

3. Using the color-labeled marker clusters, I identified which launch sites have relatively high success rate.

4. calculated the distances between a launch site to its proximities to answered some questions for instance:

    a. Are launch sites near railways, highways and coastlines.

    b. Do launch sites keep certain distance away from cities.

<h1>BUILD A DASHBOARD WITH PLOTLY DASH</h1>

1. I built an interactive dashboard with Plotly dash

2. I plotted pie charts showing the total launches by a certain sites

3. I plotted scatter graph showing the relationship with Outcome and Payload Mass (Kg) for the different booster version.

<h1>PREDICTIVE ANALYSIS (CLASSIFICATION)</h1>

1. I loaded the data using Numpy and pandas, transformed the data, split our data into training and testing.

2. I built different machine learning models and tune different hyperparameters using GridSearchCV.

3. I used accuracy score as the metric for our model, improved the model using feature engineering and algorithm tuning.

<h1>CONCLUSION</h1>
From the datasets We can conclude that:

1. The larger the flight amount at a launch site, the greater the success rate at a launch site.

2. Launch success rate started to increase in 2013 till 2020.

3. Orbits ES-L1, GEO, HEO, SSO, VLEO had the most success rate.

4. KSC LC-39A had the most successful launches of any sites.

5. The Decision tree classifier is the best machine learning algorithm for this task.

For the predictive analysis we found that Logistic Regression, SVM, Decision Tree and KNN have similar results, both in training and test datasets, so their use is equivalent
