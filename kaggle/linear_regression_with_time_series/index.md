# Linear Regression with Time Series

* Kaggle course:
[Linear Regression with Time Series](https://www.kaggle.com/code/ryanholbrook/linear-regression-with-time-series)
* [Original Notebook Copy](./linear-regression-with-time-series.ipynb)

## Personal notes

**Time Series**:
It's possible to use the index as the timestamp for time series.

**Forecasting**
is the process of predicting the future value of an asset based on the past values.

**Linear Regression**
algorithm learns how to make a weighted sum from its input features. For two features, we would have:

```python
target = w_1 * feature_1 + w_2 * feature_2 + bias
```

During training, the regression algorithm learns values for the parameters weight_1, weight_2, and bias that best fit the target.

* Time-step features are features that comes from:
  * Timestamp column
  * Row indexes

Below is a graph that shows how linear regression (blue line) is able to predict the future value of a time series (gray line).

![](./timeseries_results1.png)

**Linear Regression with Indexes** (like above) are calculated with the following formula:

```python
target = weight * index + bias
```

We can analyze specific points in time by using a linear regression with **Lag Features**.

For **Lag Features** you can get specifics points in time by using whether the index or the timestamp. You would use the following formula:

```python
target = weight * lag + bias
```
