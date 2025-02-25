# Project Name : Bike Sharing Case Study

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

Company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:
  1. Which variables are significant in predicting the demand for shared bikes.
  2. How well those variables describe the bike demands

Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
  ### Business Goal:
  Build a model to predict the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the 
  demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. 
  Further, the model will be a good way for management to understand the demand dynamics of a new market.
      - **Inventory Management**: The company can use this information to adjust its bike inventory based on the expected demand during different periods.
      - **Marketing Strategies**: Targeted marketing campaigns can be launched to boost rentals during periods of lower demand.
      - **Operational Planning**: Staffing and maintenance schedules can be optimized based on the anticipated rental volumes.

  ### Approach
  Company is concerned and wants to understand the factors affecting the demand for shared bikes. This is a regression problem, since we are trying to predict a 
  continuous value (the number of bike rentals).

  Here are some of the things that we will do to address the problem:

  #### Data Preparation:
  - Convert the `weathersit` and `season` variables to categorical string values.
  - Will keep the `yr` column as it is. Model Building.
  - Will use the `cnt` variable as the target variable.
  - Will build a `linear regression model` to predict the demand for shared bikes. Model Evaluation:
  - Will calculate the `R-squared score` on the test set to evaluate the model's performance.
  
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- **Overall Model Fit**:
  - `R-squared (0.812)`: The model explains approximately 81.2% of the variance in total bike rentals (cnt).
  - `Adjusted R-squared (0.809)`: This is a slightly more conservative estimate, adjusting for the number of predictors. It's very close to the R-squared, suggesting that the model isn't overfitting despite having fewer predictors.

- **Key Predictors and Their Impact**:
  - `yr (Year)`: The coefficient is 0.2420 and highly significant (p < 0.001). This confirms the strong positive trend in bike rentals from 2018 to 2019.
  - `holiday`: The coefficient is -0.0849 and significant (p = 0.002). This indicates that rentals tend to be lower on holidays.
  - `temp (Temperature)`: The coefficient is 0.4300 and highly significant (p < 0.001). This confirms the strong positive relationship: higher temperatures lead to more rentals.
  - `windspeed`: The coefficient is -0.0957 and significant (p < 0.001). This indicates that higher wind speeds are associated with fewer rentals.
  - `season_spring and season_winter`: These are dummy variables for spring and winter, respectively. The coefficients are negative for spring and positive for
    winter, both highly significant. This suggests that rentals are lower in spring and higher in winter compared to the baseline season (likely fall).
  - `weathersit_Light Snow/Rain and weathersit_Mist + Cloudy`: These weather situation variables have negative and highly significant coefficients. This means that these weather conditions are associated with fewer rentals compared to clear weather.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- **python** - 3.13.1
- **numpy** - 2.2.1
- **pandas** - 2.2.3
- **matplotlib** - 3.10.0
- **seaborn** - 0.13.2
- **statsmodels** - 0.14.4
- **sklearn** - 1.6.1

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements

- This project was inspired by Upgrad IIIT Bangalore PG program on ML and AI.
- This project was based on Multiple linear regression


## Contact
Created by @[GVChalamaReddy](https://github.com/GVChalamaReddy) - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
