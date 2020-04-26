# Spotify-Music-Data-Analyses
## Background/Project Motivation <br/>
Spotify is a digital music, podcast and video streaming service that has gained enormous popularity in recent years. It allows people to access millions of songs and other audio content from all over the world in one convenient service. 
<br/><br/>
## Data Sources <br/>
**Kaggle**<br/>

**Spotify**<br/>

<br/><br/>
## Table of Contents
This project is separated into three jupyter notebooks:

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
> - Multiple Linear Regression to predict what song would be popular in 2020 <br/>
        - K-Fold Cross Validation <br/>
        - Ridge Regression <br/>
        - Lasso Regression <br/>
        - GridSearchCV <br/>
        - K Nearest Neighbors <br/>
> - Future Work
<br/>

### 2. Spotify API Gathering Data <br/>
> - Defining functions to pull playlist data from my personal spotify account <br/>
> - Manipulating the data into useful datasets containing the song features <br/>
> - Visualizing the differences in the song features between playlists <br/>
> - Exporting dataframes as excel .csv files <br/>
<br/>

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


For cross-validation,the cluster labeled dataset was split into training and testing validation sets. For each classifier, confusion matrices and accuracies were used to calculate the success. 

**Confusion Matrices**
For a given classifier, a confusion matrix could be constructed. The confusion matrix is used to show the number of:

True positives (TP): Track moods that the classifier labeled correctly
True negatives (TN): Track moods that the classifier labeled as one of the other moods
False positives (FP): Unrelated tweets that the classifier labeled as related
False negatives (FN): Related tweets that the classifier labeled as unrelated

**Accuracy**
Accuracy determines out of all the classifications, how many did we classify correctly? This is represented as: <br/>
Accuracy = (TP + TN) / (TP + TN + FP + FN)

