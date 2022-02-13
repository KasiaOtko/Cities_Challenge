# About

This is a project for [Introduction to Business Analytics](https://kurser.dtu.dk/course/42577/info) course on Technical University of Denmark (winter 2020 edition), where we explored a dataset from the [Urban Typologies project](http://web.mit.edu/afs/athena.mit.edu/org/i/its-lab/www/dashboard/new%20dashboard/index.html), consisting of 331 cities and 64 factors describing them. The project contains exploratory and prediction component. In the latter, the goal was to predict CO2 Emissions per capita.

Techniques used in the exploratory part:
* imputation of missing data using mean, median and `KNNImputer` model from scikit-learn package. We evaluated how each method affects a distribution of each variable as well as a correlation with the target variable;
* investigation of relationship between modes of transportation and a quality of life;
* visual analysis of factors correlating with longevity;
* K-means and hierarchical clustering to find clusters of cities with similar characteristics that influence the standard of living in a given city.

Prediction part includes:
* linear regression with 17 variables that are most correlated with the target;
* linear regression with manually selected features based on correlation with the target but also considering colinearity between the features;
* linear regression with logarithmic transformation of the target variable;
* use of L1 regularization and cross-validation for feature selection: remove features whose coefficients were schrinked completely to zero by L1 regularization;
* `RandomForrestRegressor` and `RandomizedSearchCV` for hyperparameter tuning;
* simple neural network in Keras;
* discussion of generalizability/transferability: prediction using an invalid train-test split, where the train set would only include cities that belong to North America and South America.

All the results are presented in the .ipynb file.
