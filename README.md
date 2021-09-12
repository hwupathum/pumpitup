
# Pump it Up : Data Mining the Water Table

All training and testing data re stored on github. Development was done in Google Colab which can be found [here](https://colab.research.google.com/drive/11xTIt5BTRvcKlSFzSNjcerl2YuA2-RbB?usp=sharing). 

## Analysing data

1. Identified the number of features
2. Identified that the labeld classes does not have even distribution 
3. Identified featured with missing values
4. Identified numerical and categorical data
5. Identified min, max, mean and outliers in numerical data
6. Identified number of unique values in categorical data

## Preprocessing data

### Missing values
1.  Used mode to fill missing values in binary features *public_meeting* and *permit*
2. Removed  *funder*, *installer*, *subvillage*, *scheme_management*, and *scheme_name* features with missing values

### Handling outliers

1. Used scatterplot to find outliers in *latitudes* and *longitudes*, and replaced outliers with mean value grouped by *region_code*
2. Replaced outliers of *gps_height* with mean value grouped by *region_code*

## Feature engineering


### Feature selection
1.  Dropping features with simmilar categorical values (e.g. *quantity*, *payment*, *water_quality*)
2. Using chi-square to select best categorical variables

### Data encoding
1. Used frequancy encoding for categorical variables
2. Used labeled encoding for binary categorical variables and data labels

### Creating new features
1. Created new feature *year_recorded* using *date_recorded*
2. Created the new feature *age_of_water_pumps* using construction_year* and *year_recorded*

## Model
1. Used Random Forest Classifirer model
2. Used randomized search for hyperparameter tuning


## Final submission

Best score is 0.8027 with the rank 2695 from 12368 competitiors

![submission screenshot](https://raw.githubusercontent.com/hwupathum/pumpitup/main/submission.png)