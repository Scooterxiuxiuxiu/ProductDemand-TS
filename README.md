# Product Demand Forecasting
#### Project5 for EECS 731

Project data could be found at <br>
https://www.kaggle.com/felixzhao/productdemandforecasting

To built time series model for demand of a particular product, I provided my prediction by following steps:
  
  * Load the data set into panda data frames and extract its data shape and statistic features
  
  * Convert product demand into numeric data 
  
  * Count for data size for each type of products and show the top 30 in bar chart; 
    Take demands for Product_1359 as target to predict
  
  * convert time index into standard form
  
  * Create train and test dataset: 75% for training
    
  * ARIMA model
     > Taking first, second and third differencing to detrend and get stationary data:
       Second differenciated data shows no big difference in trend with third differenciated data.
       So weekly total price data could be considered as stationary after first differenciating. 
     > Ploting acf and pacf to find ordes for auto regression and moving average
     > Invertibility was detected when using ARIMA model
     > Predition results were not closed to real data
     > Should deal with data invertibility or use another model to improve the predict performance
     
   * Prophet Time Series Forecasting
     >Monthly demand for Product_1359 was said to be decreasing slightly in the future. 
     >Most real data were fall within the confident interval.
   


More details and discussion could be found in code comments.
