# Spatio-temporal Forecast on Sea Temperature and Salinity - Best Innovative Design Winner Solution

Welcome to the GitHub repository showcasing our Best Innovative Design winning solution for the Ocean of Data Challenge – Coast to Coast to Coast, a collaborative effort by DeepSense, the Canadian Integrated Ocean Observing System (CIOOS), and various partners. As proud participants from the University of Alberta, we are excited to present my innovative machine-learning approach tailored for forecasting sea temperature and salinity.

This challenge, which ran from November 1st to November 20th, 2023, brought together 240 talented students from 10 different Canadian post-secondary institutions. It provided a platform for us to apply advanced machine-learning techniques to understand and solve complex oceanic issues.

To view the detailed results and insights of our project, please refer to our comprehensive video presentation available on YouTube.  

[Video Presentation - Extended Version](https://youtu.be/9YQ4zv3rX-A?si=EWHYAtuFVZEA7GbM)

[Winner Announcement](https://www.linkedin.com/feed/update/urn:li:activity:7135340703865315330/)  

**Project Objective**

Our project embarked on an ambitious journey to forecast oceanic conditions, specifically focusing on the temperature and salinity of the sea, with a long-term outlook extending to the year 2050. This endeavor aimed to contribute valuable insights into the understanding and preservation of oceanic biodiversity. 

Our research utilized comprehensive datasets available on the CIOOS datahub, particularly focusing on:

'IOS Rosette Bottle Data': This dataset provided a rich source of information on various oceanographic parameters, crucial for our time-series analysis.
'Vertical profiles of seawater properties measured by Conductivity-Temperature-Depth loggers in British Columbia, Canada, from 1965 to the present': This extensive dataset offered a historical perspective, enabling us to build a robust model for forecasting future conditions.
By harnessing these datasets available at [CIOOS datahub](https://explore.cioos.ca/?lang=en), our project sought to deliver a nuanced understanding of the changes in ocean temperature and salinity, contributing to the broader field of marine science and aiding in the efforts to preserve our oceans' diverse ecosystems.

**Data Cleaning**  

<img src="https://github.com/gjftns7220/Sea_temperature_and_salinity_prediction/assets/143769164/4f179767-4182-46a0-853d-51a214ee2b1f" width="400" height="300">

Our project tackled the challenge of efficiently analyzing and forecasting ocean temperature and salinity by strategically narrowing the focus of our study. Faced with an initially overwhelming dataset comprising 27.5 million rows of tabular data, we adopted a targeted approach to enhance model training efficiency and optimize our training data to reduce them down to 11.5 million rows.  

To achieve this, our analysis was confined to a specific region of the ocean and specific ranges for the key variables, characterized by:  
Longitude:         Ranging from -140° to -122°.  
Latitude:          Spanning from 45° to 55°.  
Depth:             Covering from the surface down to 500 meters.  
Temperature Range: From the cold -3° Celsius up to a warmer 20° Celsius.  
Salinity Range:    Measuring from 20 to 40 PSU (Practical Salinity Units).  

This refined approach not only streamlined our data processing efforts but also ensured that our machine-learning models were trained on the most relevant and impactful data subsets. By focusing on these specific geographic, depth, temperature, and salinity parameters, we aimed to maximize the accuracy and relevance of our oceanic forecasts.

**Tools and Methods**  
In our quest to predict future sea temperature and salinity, we employed three prominent open-source regression libraries known for their effectiveness in handling complex datasets: LightGBM, XGBoost, and CatBoost. These tools were instrumental in developing our time-series forecasting models.  

A key challenge we faced was the requirement of at least four features for our models: time, longitude, latitude, and depth. Selecting 3D coordinates that were not only relevant but also abundant in our training data posed a significant challenge. These coordinates needed to closely resemble our existing dataset to ensure the accuracy and reliability of our predictions.  

Initially, we explored the use of Generative Models for Synthetic Data Production, specifically Variational Autoencoder (VAE) and Generative Adversarial Network (GAN). These models held the promise of generating new, synthetic data points that could enrich our dataset.  

However, we encountered substantial hurdles in terms of computing resource consumption and time constraints with these generative models. To overcome this, we pivoted our strategy. Instead of relying on synthetic data generation, we opted to select random 3D coordinates directly from our training set. From these, we generated 1 million randomly spaced data points, in terms of time, spanning from June 1st, 2023, to December 31st, 2050. This approach not only streamlined our data preparation process but also ensured that our models were trained on data points that were representative of the conditions we aimed to forecast.  

**Model Performance Metrics**  
In the initial stages of our project, we adopted the conventional Random Forest Regression model from scikit-learn, a widely-used and robust method for regression tasks. However, as our research progressed, we explored advanced gradient-boosting algorithms, namely LightGBM, XGBoost, and CatBoost. These algorithms demonstrated superior performance in terms of training time efficiency and overall predictive accuracy, leading us to pivot our approach towards these more sophisticated methods. This strategic shift was pivotal in enhancing the effectiveness of our model in forecasting sea temperature and salinity with greater precision and speed.

Sea Water Temperature Predictions:  
LightGBM: RMSE - 0.7584, MAE - 0.5834, R² - 0.8339  
XGBoost: RMSE - 0.7495, MAE - 0.5634, R² - 0.8378  
CatBoost: RMSE - 0.7107, MAE - 0.5365, R² - 0.8541  
Sea Water Salinity Predictions:  
LightGBM: RMSE - 0.5469, MAE - 0.2978, R² - 0.8940  
XGBoost: RMSE - 0.5287, MAE - 0.2958, R² - 0.9010  
CatBoost: RMSE - 0.5254, MAE - 0.2968, R² - 0.9022  

To capitalize on the strengths of each library and algorithm, we implemented an Ensemble Voting Approach. This technique led to improvements across all metrics compared to using any single method alone.

Ensemble Voting Results:  
Temperature Predictions:  
Combined Metrics: RMSE - 0.6975, MAE - 0.5327, R² - 0.8595  
Weights: LightGBM - 27.66%, XGBoost - 9.31%, CatBoost - 63.03%  
Salinity Predictions:  
Combined Metrics: RMSE - 0.4967, MAE - 0.2659, R² - 0.9126  
Weights: LightGBM - 27.60%, XGBoost - 28.38%, CatBoost - 44.02%  

The Ensemble Voting Approach effectively combined the predictive capabilities of each model, resulting in a more accurate and reliable forecasting system for both sea water temperature and practical salinity.



In concluding our solution for the Ocean of Data Challenge – Coast to Coast to Coast, I would like to extend my sincere gratitude to DeepSense for offering such a remarkable opportunity to engage in this data science competition. The experience has been immensely educational, enriching our understanding of machine learning and data analysis. The knowledge and skills we have acquired through this challenge will undoubtedly be invaluable in our future career endeavors. Thank you, DeepSense, for fostering an environment of learning and growth in the field of data science.



