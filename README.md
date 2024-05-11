
<img width="1437" alt="Screenshot 2024-04-24 at 6 30 50 PM" src="https://github.com/indiatoryy/toronto-shelter-demand/assets/105636722/02cf20c5-9b8c-4d1c-86d1-b5f99be49b14">


## Background
Homelessness presents a significant challenge in Toronto, affecting around 9,000 individuals on any given night. Each year, homelessness imposes a $7B cost on Canadian society, representing the immense human, social and economic challenges that stem from not having a place to call home. In response to this crisis, the Canadian government is investing $2.2B over 10 years to improve shelters and services for the homeless. This substantial investment highlights the need for strategic, data- driven approaches to ensure this funding is used effectively.
## Objective
This project aimed to develop a machine learning model capable of predicting shelter demands in response to the dynamic and fluctuating needs of the homeless population in Toronto. This model will be used to improve operational efficiency, ensuring that shelters can respond to changes in demand and reduce the number of people on the streets each night.

## Existing Solutions
### Review of Baseline Models
The following are three commonly used baseline models in the field:
* **Autoregressive Models (AR):** These models have been widely used for time series forecasting due to their simplicity and effectiveness in certain scenarios. An autoregressive model predicts future behavior as a linear combination of past values. While AR models are useful for data with strong temporal correlations, they often fall short in scenarios where patterns change over time due to external factors, such as sudden economic shifts or weather-related impacts, which are typical in shelter demand forecasting.
*	**Random Forest Regression (RFR):** This model uses an ensemble learning method for regression tasks, which involves constructing a multitude of decision trees during training and outputting the average prediction of the individual trees. Random Forest can capture nonlinear relationships better than AR models and is robust against overfitting. However, its predictive performance can degrade when encountering data outside the range of the training set, making it less effective in managing the variability and sudden changes often seen in shelter usage data.
*	**Prophet Model:** Developed by Facebook, the Prophet model is designed for forecasting time series data that exhibits seasonal trends and patterns. It is particularly well-suited to data with clear and consistent patterns over time and can accommodate seasonality with multiple frequencies. While Prophet is powerful for handling daily and seasonal fluctuations in data, its performance may diminish in the face of irregular events or when the data includes anomalies, which are common challenges in the context of homelessness.

### Limitations of Baseline Models
Each of these models brings valuable insights and predictive power to different forecasting problems, but they have limitations when applied to the complex and dynamic environment of homeless shelter management:
* **Sensitivity to External Factors:** None of the baseline models inherently account for external influences without significant manual adjustments or additional data engineering, which can be cumbersome and inefficient in real-time operational settings.
*	**Adaptability to Rapid Changes:** Homeless populations are affected by a variety of fast-changing factors that these models may not quickly adapt to, such as sudden policy changes or emergency situations.
*	**Complexity of Integration:** Integrating these models into existing operational workflows can be challenging, as they may require extensive customization to align with specific operational needs and data environments.

Due to these limitations, there was a clear need for a more robust forecasting approach that could more accurately predict fluctuating demands and integrate seamlessly with shelter operations. This led to the development of the LSTM model, which aims to overcome these challenges by leveraging deep learning to enhance prediction accuracy and adaptability.

## Approach and Methodology
### Datasets
This project involved various datasets, including:
* [Daily shelter occupancy](https://open.toronto.ca/dataset/daily-shelter-overnight-service-occupancy-capacity/)
* [Weather](https://climate.weather.gc.ca/historical_data/search_historic_data_e.html)
* [Available low-cost housing](https://open.canada.ca/data/en/dataset/324befd1-893b-42e6-bece-6d30af3dd9f1)
* [Persons in crisis calls](https://data.torontopolice.on.ca/datasets/79c8e950bfe54ce39334ba108e1b325f_0/explore)

### Model Development
The machine learning solution for forecasting homeless shelter demand in Toronto leverages a Long Short-Term Memory (LSTM) model, which is particularly suited for time series data due to its ability to remember information over extended periods. This characteristic is crucial in understanding and predicting patterns in shelter usage that are influenced by complex, dynamic factors.
*	**Clustering and Geospatial Analysis:** To address the diverse nature of the shelter locations and their demand patterns, we applied clustering algorithms. This step categorized shelters into groups based on their geographical locations and other relevant features, allowing the model to make specialized predictions for each cluster rather than a one-size-fits-all forecast.
*	**Initial Demand Forecasting:** Using the clustered groups, we trained the LSTM model on historical data to establish baseline demand forecasts. This model considered both regular patterns and seasonal fluctuations in shelter use.
*	**Forecast Adjustment:** To refine the predictions, we incorporated a feature-based adjustment process. This involved analyzing additional data features that emerged from correlation analysis, such as specific events or sudden economic changes, to adjust the forecast in real-time, enhancing the model’s responsiveness and accuracy.

<img width="1180" alt="Screenshot 2024-05-11 at 3 08 18 PM" src="https://github.com/indiatoryy/toronto-shelter-demand/assets/105636722/07c360b3-6c57-4d80-9e12-b0990c18d8c4">


## Key Findings and Results
The Adjusted Geospatial Multivariate LSTM model significantly outperformed baseline models (Random Forest, Autoregressive, and Prophet models) in predicting shelter demands. The novel model achieved a lower mean squared error (MSE) and mean absolute error (MAE).

<p align="center">
  <img width="683" alt="Screenshot 2024-05-11 at 3 08 06 PM" src="https://github.com/indiatoryy/toronto-shelter-demand/assets/105636722/13578216-0a93-4236-8013-307e6811c8fe">
</p>

## User Interface
<p align="center">
  <img width="1435" alt="Screenshot 2024-04-24 at 6 38 38 PM" src="https://github.com/indiatoryy/toronto-shelter-demand/assets/105636722/39ad9a1b-648e-41af-9768-7ac281def0ee">
</p>


## Future Work

* **Community Impact Analysis:** Future work will involve detailed studies to measure how improvements in shelter forecasting affect the overall well-being of the homeless population. This includes tracking long-term outcomes such as duration of homelessness and success rates in finding permanent housing.
* **Geographic Expansion:** If the project achieves success in Toronto, a major area of future work is to adapt and apply the model to other cities. Each new implementation will help refine the model further, making it more versatile and effective.
* **Real-Time Implementation:** Ongoing development efforts should be focused on integrating real-time data feeds, allowing the model to adjust forecasts instantaneously as new data becomes available. This capability will be particularly valuable during sudden crises, such as extreme weather events or economic downturns.


## Conclusion
This research has yielded a robust tool, the Adjusted Geospatial Multivariate LSTM, that promises to improve how Toronto manages shelter demands. Its adoption by shelter managers and policymakers could be a crucial step toward resolving urban homelessness.

## Contributors
_Project by Nida Copty, Emily Nguyen, Tom Nguyen, and India Tory in collaboration with Borealis AI._

[_See the team repository here._](https://github.com/Tomasdfgh/RBCs_Borealis_AIs_Shelter_Occupancy_Forecast/blob/main/README.md_)
