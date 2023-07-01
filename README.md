# Data-Science-Challenge-2023
EY Data Science Challenge 2023 Level 1

Team: Devashish Mahajan

Steps:
1) Data gathering
2) Data visualization (pictures and graphs)
3) Data gathering on proper hyper parameters (box size, time window)
4) Feature extraction and feature engineering
5) Model building
6) Model hyperparameters tunning
7) submission

1) Data gathering:
+ Crop_Location_Data_20221201.csv  --- Document provided for training data


2) Data visualization (pictures and graphs):
+ Hyperparameter tuning for Data Gathering From Landsat.ipynb
- Tunning hyperparameter "box_size_deg" to enclose only required area around the logitude and latitude location.
(initial=0.10,  final=0.010) **add photo
- Tunning hyperparameter "time_window" to cover the crop cycles. (final ="2021-11-01/2022-05-30") **add graph
- Tunning hyperparameter "resolution" to get good quality image resolution. (initial=30, final=10) **add photo
- Study the graph patterns generated from NDVI for Rice. 
- Presence of rice shows hills and valleys in the scatter plot.
- Non rice region (river, road, Jungle) shows smooth and flattened NDVI scatter plot.


3) Data gathering on proper hyper parameters (box size, time window):
+ RVI Data Gathering From Sentinel 1.ipynb
RVI parameters:
-satellite= "sentinel-1-rtc"
-box_size_deg= 0.0004
-time_window= "2021-12-01/2022-08-30"
-resolution= 10

+ NDVI Data Gathering From Landsat.ipynb
NDVI parameters:
-satellite= "landsat-8", "landsat-9"
-box_size_deg=0.010
-time_window="2021-11-01/2022-05-30"
-resolution=10

4) Feature extraction and feature engineering:
+ Imputing missing values: 
>>>vh_vv_data.interpolate(method='linear',axis=1, inplace=True)
>>>vh_vv_data.interpolate(method='linear',limit_direction='backward',axis=1, inplace=True)

5) Model building:
6) Model hyperparameters tunning:
+ select features_BaggingWithVoting_checked_clean_pending.ipynb

7) submission:
+ submission_clf_final_20230329.csv