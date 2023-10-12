# Discussion topics part 3

## The AWS-lesson

1. What is the difference between univariate and multivariate data?
    A: Univariate data analysis focuses on a single variable or attribute at a time. Multivariate data analysis involves multiple variables or attributes simultaneously. This means you are examining and summarizing data related to one specific aspect or characteristic.  This means you are considering the relationships and interactions between two or more variables.

1. What is the difference between cyclical and seasonal data?
    A: Seasonal patterns occur when there are regular, predictable fluctuations in data over a fixed period of time, typically within a year. These patterns are often associated with natural or calendar-driven factors such as seasons, months, quarters, or days of the week.Cyclical Data:
    A: Cyclical patterns are characterized by longer-term, periodic fluctuations in data that are not tied to a fixed calendar cycle. These patterns typically extend over several years or even decades and are often associated with economic, business, or industry cycles.

1. Time series data tends to be correlated. What does this mean?
    A: it means that there is a statistical relationship or association between data points at different time steps. In other words, the values in the time series are not independent; they are influenced by past or future values.

1. What data augmentation would have been useful in the bike-highway data? (The exercise on grouping data, 2.4)
    A:
1. What meta data would have been useful in the bike-highway data? (The exercise on grouping data, 2.4)
    A:
1. There are four ways of filling in missing data in time-series data (Forward fill, backward fill, moving average an interpolation). Explain them with an example.
    A: Forward Fill: This method replaces missing values with the most recent observed value before the missing data point. For example, if you have daily temperature data and a missing value on June 3, you would fill it with the temperature recorded on June 2.

    A: Backward Fill: Backward fill replaces missing values with the next observed value following the missing data point. Using the same example, if June 3 is missing, it would be filled with the temperature recorded on June 4.

    A: Moving Average: This method calculates the average of neighboring data points and fills the missing value with this average. For instance, if you have hourly stock prices and a missing value at 2:00 PM, you can use the average of the prices at 1:00 PM and 3:00 PM to fill the gap.

    A: Interpolation: Interpolation estimates missing values based on the trend or relationship between adjacent data points. For instance, if you have monthly sales data with a missing value for May, interpolation would use the sales in April and June to estimate May's sales based on the data trend.

1. What is the lookahead risk when using backward fill?
    A: Lookahead risk in the context of using backward fill for filling missing data in time series refers to the potential problem of incorporating future information into past data. When you fill a missing data point with a value observed after the missing point in time, you are essentially using information that wouldn't have been available at that point in time. This can lead to a misleading analysis and forecasting results because it violates the principle of causality and can introduce bias into your analysis.

    For example, if you have a financial time series and use backward fill to fill a missing data point with a future price, it may make it appear as if you could have predicted the future, which is not accurate or realistic.

1. What is the big problem with an out of stock-problem?
    A: In the context of data science, the major problem with an "out of stock" issue is that it can lead to inaccurate forecasting and modeling. When historical data includes periods of out-of-stock items, it can distort statistical patterns and relationships, making it challenging to build reliable predictive models. This can result in poor demand forecasting, inefficient inventory management, and suboptimal decision-making.

1. What is downsampling? And when is it a good idea?
    A: Downsampling is the process of reducing the number of data points in a dataset. It's a good idea when dealing with large datasets to save storage and processing time, reduce noise, balance imbalanced data, or improve visualization and model training. However, it should be done carefully to retain data quality and representativeness.

1. What is smoothing in the context of outliers in time series data? Why are we handling outliers differently in time series data?
    A: Smoothing, in the context of outliers in time series data, refers to the process of reducing or minimizing the impact of extreme or erratic data points (outliers) in order to create a more stable and reliable representation of the underlying data trends.

    A: Temporal Dependence: Time series data points are often dependent on their temporal order. An outlier at a specific time point can have a ripple effect on subsequent data points, potentially distorting the entire series. Therefore, special attention is needed to handle outliers without introducing bias.
1. Explain seasonality in time series with an example.
    A: In the summer there will be more people who go and eat an ice cream compared to the winter when there will be less people going for an ice cream. Thus the amount of people going for an ice cream depends on what the weather and what season it is.
1. When selecting a predictor in AWS forecaster you need to select a domain. Explain and give some examples.
    A: In AWS Forecast, when selecting a predictor, you are essentially choosing a forecasting algorithm or model to use for making predictions on your time series data. To make this selection, you need to specify a "domain," which is essentially a high-level category or context for the type of data you're working with. AWS Forecast uses different forecasting domains to optimize predictions based on the characteristics of the data. Here are some examples of domains in AWS Forecast:
    1. Retail
    2. Energy
    3. Supply chain

1. When predicting, your data can include the time series, metadata and related. Explain with an example. Which are required and which are optional?
    A: Time Series Data: This is the primary data containing historical observations over time, such as daily sales, stock prices, or temperature measurements.

    Metadata: Metadata provides additional information about the time series data. For example, in retail forecasting, metadata might include product attributes (color, size) or store locations.

    Related Time Series: Related time series are secondary data sets that can impact the primary time series, like sales of umbrellas related to rainfall data.

    Time series data is required for forecasting.
    Metadata is optional but can improve forecast accuracy by providing context.
    Related time series are optional and used when they provide valuable insights into the primary time series.

1. Explain what a backtest windows is, and how it relates to the test and training-set split.
    A: A backtest window in time series analysis refers to a specific period in the dataset that is used to evaluate the predictive performance of a model12. The concept of backtesting is actually quite simple. It involves keeping a later part of the data as test data so that we can evaluate the model against this test data.
    Backtesting means we train the algorithm on data from a certain time period and then test its performance on older data. For example, we could train on data from a date range of 2015 to 2018 and then test on data from 1990 to 2015.

1. What are prediction quantiles?
    A: Prediction quantiles provide a range of possible outcomes with associated probabilities in a predictive model. They convey the uncertainty in predictions by offering lower and upper bounds for potential values at specific probability levels.

1. When would you use the P10 quantile? And the P50? And P90?
    A: P10 (10th Percentile): This quantile represents a conservative, lower-bound forecast. It is used when you want to plan for a scenario where outcomes are worse than expected or when dealing with a risk-averse approach. For example, in financial planning, you might use P10 for revenue forecasts to ensure you have enough resources in case of poor performance.

    P50 (50th Percentile): Also known as the median, P50 represents the most likely or central forecast. It is commonly used for the baseline scenario when you want a balanced estimate without an overly optimistic or pessimistic bias. P50 provides a point estimate that is often used for decision-making and budgeting.
    
    P90 (90th Percentile): P90 is an upper-bound forecast that is more optimistic and represents a scenario where outcomes are better than expected. It's useful when you want to assess the best-case scenario and potential opportunities. For instance, in energy demand forecasting, P90 might be used to ensure adequate supply under favorable conditions.
    

## The powerpoint and exercises