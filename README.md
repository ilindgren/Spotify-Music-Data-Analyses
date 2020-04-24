# Spotify-Music-Data-Analyses

Spotify is a digital music, podcast and video streaming service that has gained enormous popularity in recent years. It allows people to access millions of songs and other audio content from all over the world in one convenient service. 
<br/><br/>
The data used in these analyses was from two different sources. The top songs from 2010-2019 dataset was from Kaggle and the mood analyses dataset was taken using the spotify API. 
<br/><br/>
This project is separated into three jupyter notebooks:

1. Top Spotify Songs 2010-2019 Data Analysis 
> - Business Understanding 
> - Data Cleaning
        - Removing irregular null values
        - Removing duplicates
        - consolidating genres
> - Exploratory Data Analysis
        - Matplotlib
        - Seaborn
        - Plotly
> - Clustering Algorithms to make Ready-Made Playlists
        - PCA
        - K Means Clustering
            - Elbow Plot
            - Dendrogram
        - Agglomerative Clustering
        - DBScan
        - Silhouette Score
> - Hypothesis Testing
        - Shapiro-Wilk Test
        - Levene Test
        - Welch's T-test
        - Tukey Multiwise Comparison
> - Multiple Linear Regression to predict what song would be popular in 2020
        - K-Fold Cross Validation
        - Ridge Regression
        - Lasso Regression
        - GridSearchCV
        - K Nearest Neighbors
> - Future Work
<br/>

2. Spotify API Gathering Data
> - Defining functions to pull playlist data from my personal spotify account
> - Manipulating the data into useful datasets containing the song features
> - Visualizing the differences in the song features between playlists
> - Exporting dataframes as excel .csv files
<br/>

3. My Spotify Mood
> - Clustering songs into my personal moods
        - K Means Clustering
        - PCA
        - t-SNE
> - Machine Learning to Predict Mood Labels
        - Random Forest Classifier
        - K Nearest Neighbors Classifier
        - Decision Tree Classifier
        - XGBoost
        - Support Vector Model
        - Naive Bayes
        - MLP Classifier (Neural Network)
<br/>

Finally, the .pdf file is the presentation and notes prepared for key stakeholders. 
