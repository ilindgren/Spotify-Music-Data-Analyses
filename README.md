# Spotify-Music-Data-Analyses


## Background/Project Motivation <br/>
Spotify is a digital music, podcast and video streaming service that has gained enormous popularity in recent years. It allows people to access millions of songs and other audio content from all over the world in one convenient service. 
<br/><br/>

## Data Sources <br/>
The data used in these analyses was from two different sources:
1. **Kaggle** - 'Top Spotify Songs from 2010-2019 by year' link: https://www.kaggle.com/leonardopena/top-spotify-songs-from-20102019-by-year
<br/>
2. **Spotify** - My personal playlists: "Koala-ty Tunes", "Peaches", and "Rainy Days" obtained using the Spotify API. The code script is found in Notebook 2. "Spotify API Data Gathering" 
<br/><br/>

## Table of Contents
This project is separated into three jupyter notebooks:

1. **Top Spotify Songs 2010-2019 Data Analysis** 
> **Business Understanding** <br/>
> **Data Cleaning** <br/>
        - Removing irregular null values <br/>
        - Removing duplicates <br/>
        - consolidating genres <br/>
> **Exploratory Data Analysis** <br/>
        - Matplotlib <br/>
        - Seaborn <br/>
        - Plotly <br/>
> **Clustering Algorithms to make Ready-Made Playlists** <br/>
        - PCA <br/>
        - K Means Clustering <br/>
          - Elbow Plot <br/>
          - Dendrogram <br/>
        - Agglomerative Clustering <br/>
        - DBScan <br/>
        - Silhouette Score <br/>
> **Hypothesis Testing** <br/>

### 1. Top Spotify Songs 2010-2019 Data Analysis <br/>
> - Business Understanding <br/>
> - Data Cleaning <br/>
        - Removing irregular null values <br/>
        - Removing duplicates <br/>
        - consolidating genres <br/>
> - Exploratory Data Analysis <br/>
        - Matplotlib <br/>
        - Seaborn <br/>
        - Plotly <br/>
> - Clustering Algorithms to make Ready-Made Playlists <br/>
        - PCA <br/>
        - K Means Clustering <br/>
            - Elbow Plot <br/>
            - Dendrogram <br/>
        - Agglomerative Clustering <br/>
        - DBScan <br/>
        - Silhouette Score <br/>
> - Hypothesis Testing <br/>
        - Shapiro-Wilk Test <br/>
        - Levene Test <br/>
        - Welch's T-test <br/>
        - Tukey Multiwise Comparison <br/>

> **Multiple Linear Regression** to predict what song would be popular in 2020 <br/>

> - Multiple Linear Regression to predict what song would be popular in 2020 <br/>
        - K-Fold Cross Validation <br/>
        - Ridge Regression <br/>
        - Lasso Regression <br/>
        - GridSearchCV <br/>
        - K Nearest Neighbors <br/>
> **Future Work** <br/>
<br/>

### 2. Spotify API Gathering Data <br/>
> - Defining functions to pull playlist data from my personal spotify account <br/>
> - Manipulating the data into useful datasets containing the song features <br/>
> - Visualizing the differences in the song features between playlists <br/>
> - Exporting dataframes as excel .csv files <br/>
<br/>

3. **My Spotify Mood** <br/>
> **Clustering songs into my personal moods** <br/>
        - K Means Clustering <br/>
        - PCA <br/>
        - t-SNE <br/>
> **Machine Learning to Predict Mood Labels** <br/>

### 3. My Spotify Mood
> - Clustering songs into my personal moods <br/>
        - K Means Clustering <br/>
        - PCA <br/>
        - t-SNE <br/>
> - Machine Learning to Predict My Personal Mood Labels <br/>
        - Random Forest Classifier <br/>
        - K Nearest Neighbors Classifier <br/>
        - Decision Tree Classifier <br/>
        - XGBoost <br/>
        - Support Vector Model <br/>
        - Naive Bayes <br/>
        - MLP Classifier (Neural Network) <br/>
<br/>

## Technical Report 


### EDA
Using matplotlib and plotly we explored the relationships between the individual song features. Analysis included:
1. Profile Report of the Kaggle dataset <br/>
2. Number of Tracks in each genre <br/>
3. Number of songs by each artist <br/>
4. Tracks by year <br/>
5. Heatmap of correlations between continuous variables <br/>
6. Pairplot to show distributions and relationships between features <br/>
7. Lineplot of Acousticness vs. Energy of a track <br/>
8. Swarmplot of Liveness vs. Loudness(dB) <br/>
9. Boxplot Beats per minute by Year <br/>
10. Swarmplot Danceability by Year <br/>
11. kde plot Danceability vs. Popularity <br/>
12. kde plot Valence vs. Danceability <br/>
13. kde plot Valence vs. Popularity <br/>
14. kde plot Speechiness vs. Length <br/>
15. WordCloud of genres <br/>
16. Barplot Top 20 Most Frequent Artists <br/>
17. Barplot Top 20 Most Popular Tracks <br/>
18. Lineplot showing Number of Tracks by each Artist Per Year for the top 10 artists <br/>
19. Pie Plot of genres <br/>
20. Plotly scatterplot showing the beats per minute and valence of each track every year from 2010-2019. <br/> 
21. Seaborn PairGrid of each continuous feature over the years to visualize trends over time <br/>

### Clustering for Top Spotify Songs from 2010-2019 Dataset
We used three different clustering algorithms for our Top Popular Songs dataset. <br/>
<br/>
**K-Means** clustering is one of the most popular unsupervised machine learning techniques which groups similar data points together to discover underlying patterns.<br/>
<br/>
**DBScan** stands for Density-Based Spatial clustering of applications with noise and it groups together points that are close to each other based on a distance measurement (usually Euclidean distance) and a minimum number of points. It also marks as outliers the points that are in low-density regions.<br/>
<br/>
**Agglomerative Clustering** is a bottom-up hierarchal algorithm. Bottom-up algorithms treat each document as a singleton cluster at the outset and then successively merge (or agglomerate) pairs of clusters until all clusters have been merged into a single cluster that contains all documents.<br/>
<br/>
To determine the success of each clustering algorithm we used the silhouette score. Wikipedia describes the silhouette score as a measure of how similar an object is to its own cluster (cohesion) compared to other clusters (separation). The silhouette ranges from −1 to +1, where a high value indicates that the object is well matched to its own cluster and poorly matched to neighboring clusters. <br/>
<br/>

![](KMeans_TopSpotifySongs.png) 

![](Dbscan_Clusters_TopSpotifySongs.png) 

Each cluster label was its own playlist. By clustering songs with similar attributes together, we can get a better understanding of our users' music choice. If a user tends to have a preference for the 'signature sounds' of one cluster, we can recommend similar songs in order to keep the user engaged and improve their overall experience with our platform. <br/>
<br/>

### Hypothesis Testing for Top Spotify Songs from 2010-2019 Dataset
In order to gain and retain Spotify premium users, it is important to continually generate analytical insights to improve the listening experience of Spotify customers. We used statistical analysis and hypothesis testing to answer the following questions:
>**1. Does valence have a statistically significant effect on the popularity of a song?** <br/> <br/>
>**2. Does danceability have a statistically significant effect on the popularity of a song? At what levels of danceability?**
<br/>

For the first question, we broke it down into the following null hypothesis and alternative hypothesis:
 - H<sub>0</sub>: Valence has no effect on the popularity of a song.
 - H<sub>1</sub>: Valence does have an effect on the popularity of a song. 

For the second question, we broke it down into the following:
 - H<sub>0</sub>: Danceability has no effect on the popularity of a track.
 - H<sub>1</sub>: Danceability has a significant effect on the popularity of a track. 

**Conclusions:**
We found that neither valence or energy seemed to influence the popularity of a song. <br/><br/>
This may have to do with outside features that are not included in our data - such as the artist’s popularity or their social media presence, if the artist appeared in any major events (coachella, super bowl, grammy’s, etc), the influence of the record company of the artist, what age group is the majority of our listeners? More information is needed to determine an answer to our original question – What makes a song popular? These are things we may want to consider in order to better cater to our user base and also expand our user base. 

### Multiple Linear Regression to make a prediction for 2020 
We used multiple linear regression to determine what song features would be most popular for 2020. We compared the Root Mean Squared Error for multiple models and found that our K-fold Cross Validation MLR model performed the best with the smallest error value (0.1697). <br/>

We found that the track features that would most popular in 2020 are features similar to the track 'Blah, Blah, Blah' by Kesha.<br/>

### Data Gathering using Spotify API
I specified songs that were different moods so I could get a wide variety of song features. <br/>

![](playlist_comp_2.png)

I transformed the data into a useable dataset that I saved into a .csv file for analysis in notebook 3. <br/>

### Clustering using Personal Spotify Data
Music is a medium that conveys emotion or a mood. People usually listen to songs that align with the mood that they are feeling. Using Kmeans clustering, I classified my tracks into 3 distinct clusters based on the key emotions that I associate with the majority of songs in a particular cluster: Energetic, Chill, and Cheerful. <br/>

For cross-validation, the cluster labeled dataset was split into training and testing validation sets. For each classifier, confusion matrices and accuracies were used to calculate the success. We also looked at the feature importances of the continuous variables we used in our model. Energy, Valence and Tempo were dropped from our features due to data leakage in our model. <br/>

![](Model_Accuracies_PersonalSpotifyData.png)

<br/>

For cross-validation,the cluster labeled dataset was split into training and testing validation sets. For each classifier, confusion matrices and accuracies were used to calculate the success. 

**Confusion Matrices**
For a given classifier, a confusion matrix could be constructed. The confusion matrix is used to show the number of True positives (TP), True negatives (TN), False positives (FP), False negatives (FN).<br/>
<br/>
**Accuracy**
Accuracy determines out of all the classifications, how many did we classify correctly? This is represented as: <br/>
Accuracy = (TP + TN) / (TP + TN + FP + FN)

<br/>

### Business Recommendations:
- Create ready-made playlists based on the users' personal preferences.<br/>
- Provide Song Recommendations that are similar to the users' current songs.<br/>
- Create personal playlists catered to the users' mood.<br/>

### Future Work:
- Time Series analyses to see what genres are growing in popularity.<br/>
- Include Artist popularity ranking and social media presence in the data.<br/>
- Create a neural network that would recommend songs and continually recommend relevant content as the users' taste changes over time. <br/>


