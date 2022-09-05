#### Classifying Cosmic Light Point Sources Using Machine Learning
Jenica Andersen
Classification Module in DSML Flex Bootcamp
April 19, 2022

**Abstract**
The map of space contains millions of point sources of light that have been catalogued but not classified. This project created models to classify the point sources as either star, galaxy, or quasar. The aim was to identify which model and associated parameters are best for performing this task, and to fit all of the data to the best performing model. A GridSearchCV-tuned Random Forest model outperformed Logistic Regression and k-Nearest Neighbors models. The final model produced an ROC AUC score of 0.9983 on the test data (compared to a baseline Logistic Regression ROC AUC score of 0.77). Application of the final model to the multi class data produced an F1 score of 0.974. Future steps include inspecting misclassifications, tuning the models to the multi class dataset, and trying stacked model for score improvement. 

**Design** 
This project aimed to classify celestial point sources as stars, galaxies, or quasars. Ultimately aiming to develop a tuned and highly successful multiclass classification model, the initial stages focused on success with a binary model. The star label was considered the positive class, while galaxy was the negative and quasar was omitted from the initial model development.

**Data**
The dataset was obtained via [Kaggle](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17). It contained 100,000 rows, 17 features and 1 target variable (‘class’). Galaxies made up about 60% of the point sources, Stars about 22% and Quasars about 18%. No special handling of imbalanced data was applied (though it was attempted and produced no improvement, so was not carried forward). The independent variables used were continuous and included location data, photometric (brightness) data in different bands of light, and spectrographic (redshift, or elongated wavelength) data. Features that were not included in the final runs were object ID’s, run ID’s, equipment ID’s, and date information. Minimal data cleaning was necessary. No duplicate rows occurred and only one row containing multiple null values was found and removed. 

**Algorithms**
Three types of models were tuned using RandomizedSearchCV for initial tuning, then further hyper parameter honing using GridSearchCV. The models used were kNN, Logistic Regression and Random Forest. A Pipeline was established for each model and its associated preprocessing, validation and parameter tuning. Regularization was applied in the Logistic Regression model in the form of a cost function with value 84.9—the optimized value, as identified via GridSearchCV.

One point of interest noted, the independent variable ‘redshift’ is strongly influential on model performance and produces an F1 score of 0.93 when used exclusively to predict the multiclass data. Past classification practices in the field of astronomy relied solely on redshift to classify point sources, but combining it with the photometric data produced stronger results. 

**Tools** 
The tools used include Jupyter Notebook and a collection of relevant python libraries, especially SciKitLearn libraries, matplotlib, pandas, numpy, and Seaborn.

**Communications**
Please see the accompanying slide deck and Jupyter notebook for more results and more information about this project.
