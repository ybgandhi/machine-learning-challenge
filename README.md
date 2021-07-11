# machine-learning-challenge

##Model-1 SVM

### Preprocess the Data
* First step was to decide which columns/features to keep. The more the better as the data will probably be more accurate with the most information, but there are some features that are irrelevant/noise.
* kepts all features except "koi_tce_plnt_num" since it just gives planet position in relation to the Sun

### Tune Model Parameters
* Assigned X and Y values for the model to be able to slit data to get training and testing data for the model
* Normalized and scale date to create an accurate model that has a minimal gap between data points by ensuring all have accurate weights. StandardScaler proved to be the best to scale the data.
* Used GridSearchCV to tune the model's parameters and change the grid parameters "C" and "gamma" didn't yield any significant score improvement

### Reporting
* SVM produced uninspiring results of "0.8888044957393081"