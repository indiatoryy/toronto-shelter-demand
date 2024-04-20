# Optimising Homeless Shelter Operations in Toronto: A Machine Learning Approach

Note: as of April 20th, this project is in active development and is being updated regularly.

Let's Solve It (2024)

Project by Nida Copty, Tom Nguyen, and India Tory

## Problem Statement

### Background

In Toronto, over 9000 people are homeless each night due to various factors like family violence, mental illness, and job loss. The city provides services such as shelters, respite sites, drop-in programs, and warming centres to assist them. Recently, there has been unprecedented pressure on the shelter system due to the increased cost of living and lack of affordable housing. Despite having one of the largest shelter systems in the country, Toronto shelters had to turn away almost 200 people each day in December. Homelessness support services in Toronto encounter difficulties in forecasting the demand for shelter beds, resources, and staff. The current reactive approach relies on outreach efforts and community support when shortages arise. This strain on the shelter system highlights the need for improved demand forecasting and resource allocation to improve operation efficiency.

### Importance

By enhancing forecasting and resource allocation for homeless support services, we can alleviate the strain on the shelter system and better meet the needs of those experiencing homelessness. This initiative aims to not only improve operational efficiency but also uphold the dignity and rights of all individuals in Toronto by ensuring access to stable housing, healthcare, and support services. Ultimately, by tackling homelessness, we strive to create a more compassionate and inclusive city where everyone has the opportunity to thrive.

### What We Will Predict

Our machine learning model aims to predict the demand for shelter beds and resources within Toronto's homeless support services. By analysing various factors such as weather conditions, social events, demographics, and historical occupancy rates, the model will forecast the expected need for temporary accommodation and support services. This prediction will enable better resource allocation and planning, allowing shelters to proactively address fluctuations in demand and optimise their operations.

## Data

### Data Sets

We currently plan on using the following datasets:

* Daily Shelter Occupancy: https://open.toronto.ca/dataset/daily-shelter-overnight-service-occupancy-capacity/
* Weather: https://climate.weather.gc.ca/historical_data/search_historic_data_e.html
* Available low-cost housing: https://open.canada.ca/data/en/dataset/324befd1-893b-42e6-bece-6d30af3dd9f1
* (un)employment rate: https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1410029501

Additional datasets we could consider include:

* Mental health and mental health service availability: https://data.torontopolice.on.ca/datasets/79c8e950bfe54ce39334ba108e1b325f_0/explore
* Economic Conditions: https://www.statcan.gc.ca/en/start
* GDP: https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=3610043402
* Inflation: https://www.genengnews.com/
