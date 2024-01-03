# Traffic-Estimation-Model-with-hourly-traffic-dataset
A forecasting model based on the dataset of hourly traffic density in Istanbul City for a single month. Dataset covers the dates between 2020-01-01 and 2020-02-02 

EDA - Hypothesis Tests are held in 2 seperate files.
  - Exploratory_Data_Analysis_with_Hypothesis_Testing_and_Data_Preprocessing.ipynb includes information about EDA and hypothesis tests. Also, preprocessing is performed within the file.
  - Winsorization method is ready to be applied on the data. However, due to the nature of such dataset, it is left as string. Optionally, for a better model performance, winsorization can be applied to outliers and model(s) can be retrained.
2 model is proposed
  - A combined structure of 2 ensemble (random forest + gradientboost) and 1 linear regression model. Forecasting_Model_using_Ensemble_Methods.ipynb file includes the related model.
  - An LSTM architecture with 2 LSTM layers and 1 fully connected layer is implemented in pytorch. Forecasting_Model_using_LSTM_with_PYTORCH.ipynb file includes the related model.
  - Each file includes information about the evaluation of the models.
  - Insights and inferences obtained during EDA are indicated.

Dataset is the hourly traffic dataset that is taken from the official webpage of IBB (Istanbul Municipality). 
It can be accessed from the link: https://data.ibb.gov.tr/en/dataset/hourly-traffic-density-data-set

  Raw data consists of the following features.
  - Date : Given in the form of '2020-01-01 00:00:00'
  - Latitude and Longitude : gives the related geographical location
  - Geohash : Hashed value of geographical location ( optionally, it might be hard to one-hot encode all the geographical locations. So, sticking with the coordinates itself might be a better choice. )
  - Min, max and avg speed : Related speed that corresponds to the given particular coordinates.
  - Number of Vehicles (Target) : Total number of vehicles fall within the limit of given coordinates. 
