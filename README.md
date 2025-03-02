# Linear Regression on Bike Sharing Dataset

## Project Overview

This project performs linear regression analysis on the bike-sharing dataset to predict the number of rented bikes (`cnt`). The dataset contains various features such as temperature, humidity, wind speed, and seasonality that influence bike rental demand.

## Dataset

### Dataset Characteristics

day.csv has the following fields:

- **instant**: record index
- **dteday**: date
- **season**: season (1: spring, 2: summer, 3: fall, 4: winter)
- **yr**: year (0: 2018, 1: 2019)
- **mnth**: month (1 to 12)
- **holiday**: whether the day is a holiday or not (extracted from [DC Holiday Schedule](http://dchr.dc.gov/page/holiday-schedule))
- **weekday**: day of the week
- **workingday**: if the day is neither a weekend nor a holiday, it is 1; otherwise, it is 0.
- **weathersit**:
  - 1: Clear, Few clouds, Partly cloudy
  - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  - 4: Heavy Rain + Ice Pellets + Thunderstorm + Mist, Snow + Fog
- **temp**: temperature in Celsius
- **atemp**: feeling temperature in Celsius
- **hum**: humidity
- **windspeed**: wind speed
- **casual**: count of casual users
- **registered**: count of registered users
- **cnt**: count of total rental bikes, including both casual and registered

**Additional Information:**

- **Filename:** `day.csv`
- **Description:** The dataset includes daily records of bike rentals, along with environmental and seasonal features.
- **Target Variable:** `cnt` (Total count of bikes rented per day)
- **Excluded Variables:** `casual`, `registered` (as they sum up to `cnt` and may introduce data leakage)

## Steps Performed

1. **Data Preprocessing:**

   - Loaded the dataset
   - Checked for missing values and handled them appropriately
   - Converted categorical variables to numerical
   - Dropped unnecessary features (`casual`, `registered`)
   - Mapped categorical variables

2. **Exploratory Data Analysis (EDA):**

   - Univariate analysis
   - Bivariate analysis
   - Multivariate analysis

3. **Train-Test Split:**

   - Split the dataset into training and testing sets

4. **Scaling:**

   - Standardized numerical features

5. **Feature Selection:**

   - Used Recursive Feature Elimination (RFE)
   - Removed highly correlated and redundant variables using p-values and Variance Inflation Factor (VIF)

6. **Model Training:**

   - Applied linear regression to predict `cnt`
   - Evaluated performance using metrics like RMSE, R-squared, and adjusted R-squared

7. **Model Evaluation:**

   - Assessed residuals and checked model assumptions
   - Compared predictions with actual values

## How to Run

1. Install required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
   ```
2. Run the Jupyter Notebook or Python script containing the linear regression model.

## Future Improvements

- Incorporate time-series forecasting techniques.

## Author

- Your Name (or Team Name)

