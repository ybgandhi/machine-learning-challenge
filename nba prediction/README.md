## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

##Model-1 SVM.

### Libraries / Dependencies
* sklearn (ML)
    * .model_selection
      * train_test_split
      * LabelEncoder
      * MinMaxScaler
      * StandardScaler
      * GridSearchCV
    * .svm
      * SVC
* tensorflow
    * .keras.utils
      * to_categorical
* joblib (sav file)
* pandas


### Data Processing
* First step was to decide which columns/features to keep. The more the better as the data will probably be more accurate with the most information, but there are some features that are irrelevant/noise.
* kepts all features except "koi_tce_plnt_num" since it just gives planet position in relation to the Sun
* Used `MinMaxScaler` to scale the numerical data.

### Tune Model Parameters
* Assigned X and Y values for the model to be able to slit data to get training and testing data for the model
* Normalized and scale date to create an accurate model that has a minimal gap between data points by ensuring all have accurate weights. 'StandardScaler' proved to be the best to scale the data.
* Used GridSearchCV to tune the model's parameters and change the grid parameters "C" and "gamma" didn't yield any significant score improvement

## Reporting
* SVM - 'StandardScaler': produced uninspiring results of "0.8888044957393081"
* SVM - 'MinMaxScaler': produced uninspiring results of "0.8815571354761715"


### Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

