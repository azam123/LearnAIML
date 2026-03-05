# Machine Learning Interview -- Quick Reference (Questions & Answers)

A concise reference to review before attending a Machine Learning or ML
Engineer interview.

------------------------------------------------------------------------

# 1. Machine Learning Fundamentals

**What is the bias--variance tradeoff?**\
Bias is error due to overly simple assumptions in the model, while
variance is error due to sensitivity to small fluctuations in training
data. A good model balances both.

**What is overfitting vs underfitting?**\
Overfitting occurs when a model learns training data too well and
performs poorly on new data. Underfitting happens when the model is too
simple to capture patterns.

**What is cross-validation?**\
A technique used to evaluate models by splitting the dataset into
multiple train/test folds to ensure the model generalizes well.

**What are common evaluation metrics?**\
Accuracy, Precision, Recall, F1-score, ROC-AUC for classification; RMSE,
MAE, and R² for regression.

**Classification vs Regression**\
Classification predicts categories (spam/not spam). Regression predicts
continuous values (house price).

------------------------------------------------------------------------

# 2. Random Forest

**How does Random Forest work?**\
Random Forest builds multiple decision trees using random subsets of
data and features, then aggregates their predictions.

**Why is it an ensemble method?**\
It combines predictions from many models (trees) to improve performance.

**What is bagging?**\
Bootstrap Aggregation -- sampling training data with replacement to
train multiple models independently.

**How does Random Forest reduce overfitting?**\
By averaging many decision trees trained on different subsets of data.

**Important hyperparameters** - Number of trees (n_estimators) - Maximum
depth - Minimum samples split - Maximum features

------------------------------------------------------------------------

# 3. Regression Models

**What is Linear Regression?**\
A statistical model used to predict continuous values by fitting a line
to the data.

**Assumptions of Linear Regression** - Linearity - Independence -
Homoscedasticity - Normal distribution of errors

**Linear vs Logistic Regression**\
Linear predicts continuous values. Logistic predicts probabilities for
classification.

**What is multicollinearity?**\
When independent variables are highly correlated, causing instability in
regression coefficients.

**R² (R-squared)**\
Measures how much variance in the target variable is explained by the
model.

------------------------------------------------------------------------

# 4. Convolutional Neural Networks (CNN)

**What is CNN?**\
A deep learning architecture designed mainly for image and spatial data
processing.

**What is a convolution layer?**\
Applies filters to input data to detect patterns like edges or textures.

**What are stride and padding?**\
Stride controls movement of filters; padding adds extra pixels around
input to preserve spatial size.

**What is pooling?**\
Pooling layers reduce spatial dimensions to make computation efficient.

------------------------------------------------------------------------

# 5. ML Pipelines & MLOps

**What is an ML pipeline?**\
An automated workflow that handles data ingestion, preprocessing,
training, evaluation, and deployment.

**Typical stages** 1. Data collection\
2. Data preprocessing\
3. Feature engineering\
4. Model training\
5. Evaluation\
6. Deployment\
7. Monitoring

**What is model drift?**\
When model performance degrades because real-world data distribution
changes.

**What is data drift?**\
When input data distribution changes over time.

------------------------------------------------------------------------

# 6. PySpark / Big Data

**What is Apache Spark?**\
A distributed computing framework for large-scale data processing.

**What is PySpark?**\
Python API for Apache Spark.

**RDD vs DataFrame** - RDD: low-level distributed collection -
DataFrame: structured data with optimization support

**Transformations vs Actions** - Transformations: lazy operations (map,
filter) - Actions: return results (count, collect)

**Lazy evaluation**\
Spark delays computation until an action is called.

------------------------------------------------------------------------

# 7. SQL for ML Engineers

**INNER JOIN vs LEFT JOIN** - INNER JOIN returns matching rows - LEFT
JOIN returns all rows from the left table

**GROUP BY vs HAVING** - GROUP BY aggregates rows - HAVING filters
aggregated results

**Find duplicate records**

``` sql
SELECT column_name, COUNT(*)
FROM table_name
GROUP BY column_name
HAVING COUNT(*) > 1;
```

**Second highest salary**

``` sql
SELECT MAX(salary)
FROM employees
WHERE salary < (SELECT MAX(salary) FROM employees);
```

------------------------------------------------------------------------

# 8. Python for ML

**List vs Tuple vs Set vs Dictionary** - List: ordered, mutable - Tuple:
ordered, immutable - Set: unordered, unique elements - Dictionary:
key-value pairs

**What are generators?**\
Generators produce values lazily using `yield`, saving memory.

**What are decorators?**\
Functions that modify behavior of other functions.

**Example -- Remove duplicates**

``` python
unique_values = list(set(arr))
```

**Example -- Word frequency**

``` python
from collections import Counter
Counter(words)
```

------------------------------------------------------------------------

# 9. ML System Design

**How to design a scalable ML system?**

Typical architecture:

Data Ingestion → Data Storage → Data Processing → Feature Engineering →
Model Training → Model Evaluation → Deployment → Monitoring

**Example technologies** - Data ingestion: Kafka - Storage: S3 /
Hadoop - Processing: Spark / PySpark - Training: Python / ML
frameworks - Serving: REST API / microservices

------------------------------------------------------------------------

# 10. Behavioral Questions

**Describe a machine learning project you built.**\
Explain the problem, dataset, model used, evaluation metrics, and
deployment.

**Challenges with large datasets?**\
Memory limitations, distributed processing, feature engineering, and
pipeline scaling.

**How did you improve model performance?**\
Feature engineering, hyperparameter tuning, better algorithms, and
cross-validation.

------------------------------------------------------------------------

# Key Technologies to Review

-   Python
-   PySpark
-   SQL
-   Hadoop
-   AWS S3
-   Random Forest
-   CNN
-   Regression Models
-   ML Pipelines
-   Model Deployment

