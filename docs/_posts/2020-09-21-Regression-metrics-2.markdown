<script type="text/javascript" id="MathJax-script" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.0.0/es5/latest?tex-mml-chtml.js">
</script>

# (R)MSPE, MAPE, and (R)MSLE
## An Off-By-One Example
   Suppose we are predicting sales for two shops and the two shops have different sales volumes but our predictions for both cases are off by one. In this case our Mean-Squared-Error (MSE) might be the same, but they have a different significance.

| Shop | Actual | Predicted | MSE |
|------+--------+-----------+-----|
|    1 |      9 | 10        |   1 |
|    2 |    999 | 1,000     |   1 |

# Root Mean Squared Percentage Error and Mean Absolute Percentage Error
   The MSE and Mean-Absolute-Error (MAE) are absolute errors which don't take into account how significant the error is. There are two relative errors,  Mean-Squared-Percentage-Error (MSPE) and Mean-Absolute-Percentage-Error (MAPE) that divide each error term by the actual value to give you a realive error instead of an absolute error.

$$ MSPE = \frac{1}{N} \sum_{i=1}^n \left( \frac{y_i - \hat{y}}{y_i}\right)^2 $$

$$ MAPE = \frac{1}{N} \sum_{i=1}^n \left| \frac{y_i - \hat{y}}{y_i}\right| $$

The MAPE will be inversely proportional to its target and the MSPE will be inversely proportional to the square of the target.

## Optimal Constant Predictions
   The best constant prediction you can make when using the Mean Squared Error is to predict the mean of the target values. The best prediction you can make for the MSPE is to take a weighted mean of the target values. The best constant prediction you can make for the Mean Absolute Percentage Error is the weighted median.

# Root Mean Squared Logarithmic Error (MSLE)

$$ MSLE = \sqrt{\frac{1}{N}\sum_{i=1}^N (\log (y_i + 1) - \log(\hat{y}_i + 1))^2}\\
= \sqrt{MSE(\log(y_i + 1), \log(\hat{y}_i + 1))} $$

You add a 1 to each term to prevent you from trying to take the /log/ of 0, which is undefined. The RMSLE is biased toward predictions that are higher than the actual values rather than lower.

These are the best constant predictions you can make for the competition data set.

| Metric | Constant |
|--------+----------|
| MSE    |       11 |
| RMSLE  |      9.9 |
| MAE    |        8 |
| MSPE   |      6.6 |
| MAPE   |        6 |
