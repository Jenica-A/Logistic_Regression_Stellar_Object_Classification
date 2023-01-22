## Project Design
Jenica Andersen April 1, 2022

#### Question/Need:

Based on the spectral and photometric characteristics of a celestial object, can a cosmic point source of light be classified as a galaxy, quasar (active galactic nucleus), or star? What model and hyper parameters produce the best results (greatest accuracy)? Is there a better metric than accuracy?
The impact will be having a better understanding of the universe, and a better understanding of what models are most accurate in this application.

Automating one of the most fundamental astronomical tasks (the above multi-class classification) leads to better understanding our neighborhood, our galaxy, and the universe beyond. More data will likely be coming in with the images and measurements collected from the Webb telescope. And the search for dark matter is heavily underway. This classification method could be the foundation of reaching new discoveries in astronomy.

#### Data Description:

I plan to use [this Stellar Dataset - SDSS17](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17), which is available from [kaggle](kaggle.com). 
An individual sample/unit is an observed stellar object and its spectral characteristics. 
The columns of interest are: 
* alpha = Right Ascension angle (at J2000 epoch)
* delta = Declination angle (at J2000 epoch)
* u = Ultraviolet filter in the photometric system
* g = Green filter in the photometric system
* r = Red filter in the photometric system
* i = Near Infrared filter in the photometric system
* z = Infrared filter in the photometric system
* field_ID = Field number to identify each field
* redshift = redshift value based on the increase in wavelength

The target will be **class** (object class--galaxy, star or quasar object).

#### Tools:
I plan to use jupyter notebooks, python, pandas, sklearn, logistic regression models, possibly k-nearest neighbor models, and other necessary libraries to perform this analysis.

#### MVP Goal:

A minimum viable product would be a binary classification of objects from the dataset with just one model. 
