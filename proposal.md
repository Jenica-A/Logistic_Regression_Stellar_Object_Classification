## Classification Project Proposal
Jenica Andersen April 1, 2022

#### Question/Need:

The question behind my proposed analysis is: Based on the spectral and photometric characteristics of a celestial object, can it be classified as a galaxy, quasar (active galactic nucleus), or star? What model and hyper parameters produce the best results (greatest accuracy)? 
The impact will be having a better understanding of the universe, and a better understanding of what models are most accurate in this application.

On the [webpage](Kaggle.com) where this data can be accessed, an eloquent context is given:
>In astronomy, stellar classification is the classification of stars based on their spectral characteristics. The classification scheme of galaxies, quasars, and stars is one of the most fundamental in astronomy. The early cataloguing of stars and their distribution in the sky has led to the understanding that they make up our own galaxy and, following the distinction that Andromeda was a separate galaxy to our own, numerous galaxies began to be surveyed as more powerful telescopes were built. This datasat aims to classificate stars, galaxies, and quasars based on their spectral characteristics.<

My client is my University of Farmington research advisors/committee. They will benefit by graduating another competent scholar and will be credited with another groundbreaking publication in a peer reviewed journal. 

#### Data Description:

I plan to use the [Stellar Classification Dataset - SDSS17](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17), which is available from [kaggle](kaggle.com). 
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
I plan to use jupyter notebooks, python, pandas, sklearn, logistic regression models, possibly k-nearest neighbor models, and other necessary libraries to perform this analysis. I am not planning to need or use additional tools beyond those required.

#### MVP Goal:

A minimum viable product would be a binary classification of objects from the dataset. 
