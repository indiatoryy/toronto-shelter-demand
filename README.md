# Optimising Homeless Shelter Operations in Toronto: A Machine Learning Approach

Note: as of April 20th, this project is in active development and is being updated regularly.

Let's Solve It (2024)

Project by Nida, Tom, India, and Emily

## Problem Statement

### Background

In Toronto, over 9000 people are homeless each night due to various factors like family violence, mental illness, and job loss. The city provides services such as shelters, respite sites, drop-in programs, and warming centres to assist them. Recently, there has been unprecedented pressure on the shelter system due to the increased cost of living and lack of affordable housing. Despite having one of the largest shelter systems in the country, Toronto shelters had to turn away almost 200 people each day in December. Homelessness support services in Toronto encounter difficulties in forecasting the demand for shelter beds, resources, and staff. The current reactive approach relies on outreach efforts and community support when shortages arise. This strain on the shelter system highlights the need for improved demand forecasting and resource allocation to improve operation efficiency.

### Importance

By enhancing forecasting and resource allocation for homeless support services, we can alleviate the strain on the shelter system and better meet the needs of those experiencing homelessness. This initiative aims to not only improve operational efficiency but also uphold the dignity and rights of all individuals in Toronto by ensuring access to stable housing, healthcare, and support services. Ultimately, by tackling homelessness, we strive to create a more compassionate and inclusive city where everyone has the opportunity to thrive.

### What We Will Predict

Our machine learning model aims to predict the demand for shelter beds and resources within Toronto's homeless support services. By analysing various factors such as weather conditions, social events, demographics, and historical occupancy rates, the model will forecast the expected need for temporary accommodation and support services. This prediction will enable better resource allocation and planning, allowing shelters to proactively address fluctuations in demand and optimise their operations.

## Machine Learning Approach
In our project, we have decided to consider a comprehensive machine learning approach by experimenting with a selection of different models. 

This strategy involves designing and testing multiple models, including Long Short-Term Memory (LSTM) networks, Random Forest Regression, Facebook Prophet, and Seasonal Autoregressive Integrated Moving Average (SARIMA) models. By leveraging the comparative analysis, we will attempt to combine these models strategically, capitalizing on their individual advantages to enhance overall predictive accuracy. This approach allows us to tailor our solution to deliver the best possible performance in optimizing homeless shelter operations.

We will be using Random Forest, Prophet and SARIMA as our baseline models. 

### LSTM

LSTM (Long Short-Term Memory) networks offer a powerful solution for time series forecasting tasks, particularly in predicting shelter occupancy rates. LSTMs excel in retaining relevant information over extended sequences through their memory cell state, allowing them to recognize seasonalities, trends, and other critical patterns. Furthermore, these networks demonstrate flexibility in handling varying sequence lengths, accommodating the diverse historical data available for each shelter. Robustness to noisy data and the capability to learn hierarchical representations further enhance their utility in forecasting tasks. In essence, LSTM networks present a sophisticated yet adaptable approach to shelter occupancy prediction, leveraging their strengths in temporal modeling to provide accurate and insightful forecasts.

### Multi-Step Approach
Another method we are trying is a model with multiple steps. This multi-tiered approach allows us to tackle the problem from a macro (city-wide) level and then drill down to micro factors influencing individual or grouped shelter demands. Our current implementation includes the following:
1. SARIMA to predict city wide overall capacity each night
2. Regression models trained to predict capacity based on different shelter features (postal code, sector, organization, etc)
3. Use results of regression models to shift overall prediction for a specific shelter.
