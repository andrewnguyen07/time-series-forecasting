# Time Series Forecasting

This project shows multiple Jupyter Notebooks which demonstrate a variety of LSTM models built and tuned to forecast time-series data for the [Weather Dataset](https://www.bgc-jena.mpg.de/wetter/), which has around 14k observations and 22 feature variables. The notebooks aim to study weather-related data as a whole and then forecast future values, in either single or multiple timesteps. 

## List of different RNN Models:

* Univariate - Single-step Output: utilized temperature variable and split into sequences of 24-hour interval timestep to predict temperature value for the next hour and so on. Vanilla LSTM and Stacked LSTM performed pretty similarly to each other, with MAE of train/test at 0.02/0.03, given that data has been scaled to the range of (0,1). 
* Multivariate - Single-step Output: utilized all variables and split into sequences of 24-hour interval timestep to predict next-hour value for each variable and so on. While Vanilla LSTM and Stacked LSTM performed not so well, Bidirectional LSTM achieved a relatively better result, with MAE of train/test at 0.25/0.29, given that the data has been standardized to the mean and standard deviation of the entire dataset.
* Multivariate - Multi-step Output: the same as multivariate model, but split into sequences of 24-hour timestep input and produced 24-hour timestep output. Stacked LSTM (Encoder-Decoder) and Bidrectional both achieved MAE of train/test at 0.29/0.45, , given that the data has been standardized to the mean and standard deviation of the entire data.


## Requirements

* pandas
* numpy
* matplotlib
* seaborn
* sklearn
* tensorflow
