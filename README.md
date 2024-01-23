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
Longitude: Ranging from -140° to -122°.  
Latitude: Spanning from 45° to 55°.  
Depth: Covering from the surface down to 500 meters.  
Temperature Range: From the cold -3° Celsius up to a warmer 20° Celsius.  
Salinity Range: Measuring from 20 to 40 PSU (Practical Salinity Units).  

This refined approach not only streamlined our data processing efforts but also ensured that our machine-learning models were trained on the most relevant and impactful data subsets. By focusing on these specific geographic, depth, temperature, and salinity parameters, we aimed to maximize the accuracy and relevance of our oceanic forecasts.

**Tools and Methods**


**Model Performance Metrics**
