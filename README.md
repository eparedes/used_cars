# Used Cars

## 1. Business Understanding
### Problem Statement
What drives the price of a car?

## 2. Data Understanding
### Dataset Overview
The dataset consists of one separate file:
- `vehicles.csv`: Contains **426,880** samples cars.

There are categorical and numerical features.

#### Key Findings from Exploratory Data Analysis (EDA):
- There are many missing values in the data set. Some features missing more 50% of values.
- There are extremly high values for price and odometer, so outlier analysis must be performed.

For detailed data exploration, refer to the [used cars notebook](used_cars.ipynb).

## 3. Data Preparation
### Outlier Treatment
After analyzing the price and odometer features, it was determined that prices greater than 499,999 and odometer values greater than 9,999,999 can be dropped. Data exploration revealed data input patterns that suggest random input (e.g. 123456789, 111111111, etc.)

### Data Cleansing
-The VIN feature was used to check for and remove duplicate values
-Domain knowledge indicates that some irrelevant features to determine the price of a car can be removed: `['id', 'VIN', 'condition', 'cylinders', 'size', 'paint_color', 'model', 'type', 'region', 'state']`
-The mode was used to imput missing values 

## 4. Modeling
A linear regression model was trained to predict the price of cars.

## 5. Evaluation
### Model Performance
The model was assessed using **the roor mean squared error (RMSE)** as the primary metric.
```
Root Mean Squared Error: 12759.382368016595
```


## Next Steps
### Future Enhancements
- **Feature Engineering:** Explore additional features and models to improve predictive performance.