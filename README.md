# iSpotify - Spotify Audio Feature Analysis
Clustering my top played tracks in Spotify using Spotify's Audio Features to create custom spotify playlists

## Table of Contents
* [Tools](#tools)
* [Description](#description)
  * [spotify_api](#spotify_api)
  * [eda](#eda)
  * [pca](#pca)
  * [component_selection](#component_selection)
  * [clustering](#clustering)

## Tools
* Python
* Spotify API
#### Libraries
* Spotipy
* Pandas
* Json
* Plotly
* Scikit-learn
* Numpy

## Description
### spotify_api
A function to get data from Spotify API 
1. Set up your Spotify developer account. You can Learn from [here](https://medium.com/@maxtingle/getting-started-with-spotifys-api-spotipy-197c3dc6353b).
2. Insert the following:
* **Client ID** in *client_id* (text)
* **Client Secret** in *secret* (text)
* **Username** in *username* (text)
3. You can save the dataframe you get.

### eda
Explore the data from Spotify.
*Noted: I have to change the scales of Loudness and Tempo data to be easy to visualize.*

**An example of interactive box plot**

[![pic1.png](https://i.postimg.cc/sDYXg2Td/pic1.png)](https://postimg.cc/MvGxszkd)

### pca
Reduce dimensionality with Principal Component Analysis (PCA) to be able to perform k-mean clustering, [FYI](https://medium.com/@dmitriy.kavyazin/principal-component-analysis-and-k-means-clustering-to-visualize-a-high-dimensional-dataset-577b2a7a5fe2).
1. Import the data.
2. Insert the following:
* **DataFrame** in *data* (dataframe)
* **Number of Dimensions** in *n* (integer, default=2)

*Noted: In this case, the highly dimensional dataset is reduced into 2 features in order to plot in 2D. If you want to conduct principal component selection, please see [component_selection](#component_selection).*

### component_selection
Principal component selection
1. Import the data.
2. Insert the following:
* **DataFrame** in *data* (dataframe)
* **Number of Your Data's Features** in *n_features* (integer)
3. Save your new dataframe.

### clustering
Perform K-Mean clustering.
1. Import the data.
2. K selection: [FYI](https://www.geeksforgeeks.org/elbow-method-for-optimal-value-of-k-in-kmeans/)

Insert the following:
* **DataFrame** in *data* (dataframe)
* **Minimum k** in *min_k* (integer, default=2)
* **Maximum k** in *max_k* (integer, default=10)

3. K-mean: [FYI](https://medium.com/@dilekamadushan/introduction-to-k-means-clustering-7c0ebc997e00)

Insert the following:
* **DataFrame** in *data* (dataframe)
* **Selected K** in *k* (integer, default=3)

[![pic2.png](https://i.postimg.cc/XYK5Gbkm/pic2.png)](https://postimg.cc/Wd3zCxKw)
