# Data Quality Validation using Great Expectations and CleanLab
# Introduction
In data-driven workflows, ensuring data quality is paramount to deriving accurate insights and building reliable machine learning models. This lab introduces practical methodologies to address common data challenges using **Great Expectations**, a framework for defining and validating data expectations to enforce consistency, and **Cleanlab**, a tool for detecting and correcting mislabeled data to mitigate label noise. Through guided tasks in interactive notebooks, datasets will be explored to identify anomalies, and implement corrective measures, fostering skills in maintaining data integrity and enhancing model performance. This lab bridges theoretical concepts with hands-on application, emphasizing the critical role of robust data validation and cleansing in real-world data science pipelines.


# Discussion
### Task 2
**Why might this data point be mislabeled, and which feature values could have caused the misclassification?**

It is reasonable for this datapoint to be suspected as mislabled as it is much closer to the mean of class 2 than it is to class 1.  All features are within ~1.1 standard deviations of the means of class 2 while they are ~1.5 standard deviations from the means of class 1.

### Task 3
__**Do these suspected anomalous data points match what you expect for their species? Why or why not?**__

According to background research, the individual features in each class in the iris dataset is approximately normal.

- The first two points have petal lengths around 24-25 standard deviations away from the mean.  The must be anomalies.
- The next two points have petal lengths around 4-5 standard deviations away from the mean.  The must be anomalies.
- The second last datapoint has sepal lengths and petal lengths around 2-3 standard deviations away from the mean.  It is possible that they could be anomalies.
- The last datapoint has sepal width of around 1.5 standard deviations away from the mean.  It is unlikely that it is an anomaly.

__**Which feature (sepal length, petal length, etc.) seems most unusual in these points?**__

Petal lengths has the most extreme and unusual values.  See the analysis above.

__**How can you check if these values are truly anomalies using the original dataset?**__

- The first two points are certainly anomalies.

- The other datapoints should be plotted on a boxplot, or graphed and visually inspected.
