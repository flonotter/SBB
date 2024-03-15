### Prediction of Sales for GA and HTA travelcards

Florian Notter

#### Executive summary
In my project, I focused on preprocessing and conducting exploratory data analysis (EDA) on a publicly available dataset. Throughout the EDA phase, I employed various visualizations to gain a deeper understanding of the dataset at hand. I experimented with several predictive models, including Linear Regression, Random Forest, XGB Regressor, and finally, the VAR model. The VAR model emerged as the most effective in predicting future sales, demonstrating its superiority through its results. Utilizing the VAR model, I was able to forecast the number of tickets that would be sold in the upcoming years across different districts, with a special focus on plotting the results for a specific district as an example.

#### Rationale
One might wonder why this topic merits attention. As someone deeply interested in the operational efficiency and future planning of public transportation, I find the prediction of sales for GA (Generalabonnement) and HTA (Half-Fare Travelcards) in Switzerland particularly compelling. These travelcards are integral to the Swiss Federal Railways (SBB), a cornerstone of Swiss public transport, offering extensive travel benefits. Predicting their sales is not just a matter of academic interest but a practical tool for financial forecasting, which can impact the SBB's strategy and operations.

#### Research Question
The core question I sought to answer through this project was whether it's possible to predict the future sales of GA and Half Fare Travelcards in Switzerland for the upcoming years, based on historical sales data. Essentially, I aimed to estimate the number of tickets that will be sold in the future, providing valuable insights for planning and strategy.

#### Data Sources
To tackle this research question, I relied on a publicly available dataset that detailed past sales of GA and HTA, providing a solid foundation for my predictive models.
https://opendata.swiss/en/dataset/ga-hta-liste

My dataset included six columns namely ‘Jahr_An_anno’ which is the year, ‘PLZ_NPA’ which is the district number, ‘GA_AG’ which is the number of GA ticket sales, ‘GA_AG_flag’ is an indicator if district has fewer than 20 travelcards, ‘HTA_ADT_meta-prezzo’ which is the number of half fare sales, ‘HTA_ADT_meta-prezzo_flag’ is an indicator if district has fewer than 20 half fare travelcards. The dataset consists of 35,035 rows, ranging from year 2012 to 2022, across 3194 districts. The average number of sold GA tickets per district in our dataset is 141.5, and the average number of sold half fare tickets per district in our dataset is 787.5, with maximum number of sold GA tickets in one year in specific district being 4,984, for half fare this number was 20,330.


#### Methodology
Data was split into training and testing dataset, 20% of the data was used for testing to avoid overfitting of the models.
My approach involved using four different prediction models: Linear Regression, Random Forest Regreswsor, XGBRegressor and VAR. Ther performance were evaluated with two key metrics: Mean Square Error (MSE) and Mean Absolute Error (MAE). These two metrics are one of the best indicators of how well the regression model is performing. For the VAR model which performed the best out of our four options I also experimented with different orders, I tried orders 1 to 5. This comprehensive evaluation allowed me to identify the most accurate model for the specific forecasting needs.

#### Results
During the data analysis I found that for the GA Travelcards the number of sales increased each year until 2020, and after pandemic the trend is going up again. For the Half Fare the number of sales kept increasing even during COVID, so I can expect even higher number in following years.
The highest correlation in our dataset was between the number of sales of GA Travelcards and half-fare tickets, the correlation was 0.9. That would mean that if a number of sold GA Travelcards in a specific district is high, subsequently also number of sold half-fare tickets would be high, and if the number of sold GA Travelcards was low the same thing would also apply to half-fare tickets in a specific year.

Performance of the models during cross validation is listed below:
Linear Regression on GA Travelcards:
Mean Absolute Error (MAE): 131.02
Root Mean Squared Error (MSE): 75395.76

Random Forest on GA Travelcards:
Mean Absolute Error (MAE): 127.6
Root Mean Squared Error (MSE): 74969.3

XGB on GA Travelcards:
Mean Absolute Error (MAE): 127.56
Root Mean Squared Error (MSE): 74960.67

Linear Regression on GA Travelcards:
Mean Absolute Error (MAE): 692.87
Root Mean Squared Error (MSE): 1788768.17

Random Forest on GA Travelcards:
Mean Absolute Error (MAE): 673.86
Root Mean Squared Error (MSE): 1779322.44

XGB on GA Travelcards:
Mean Absolute Error (MAE): 673.61
Root Mean Squared Error (MSE): 1779025.67

VAR model evaluation:
Order: 1
GA Travelcards - VAR MAE: 18.92, MSE: 54.96
Half Fare Travelcards - VAR MAE: 29.03, MSE: 70.92
-----------------------------------------------------------
Order: 2
GA Travelcards - VAR MAE: 50.48, MSE: 200.51
Half Fare Travelcards - VAR MAE: 93.69, MSE: 319.64
-----------------------------------------------------------
Order: 3
GA Travelcards - VAR MAE: 231.41 MSE: 2464.07
Half Fare Travelcards - VAR MAE: 834.26, MSE: 14125.43
-----------------------------------------------------------
Order: 4
GA Travelcards - VAR MAE: 29.43, MSE: 93.896
Half Fare Travelcards - VAR MAE: 76.66, MSE: 233.87
-----------------------------------------------------------
Order: 5
GA Travelcards - VAR MAE: 18.20, MSE: 49.054
Half Fare Travelcards - VAR MAE: 48.47, MSE: 155.17
-----------------------------------------------------------

The best performing model for predicting number of sold GA travelcards was VAR model with order 5, while for predicting number of sales for half fare travelcards the best preforming model was also VAR model, but with order 1. 

My findings were encouraging, indicating that predicting the number of tickets sold is a feasible task with relatively low error rates. This suggests that the models I developed can provide reliable forecasts for future sales. I can possibly experience even better performance of the model in the future, since the year of pandemic was rather unpredictable, and the situation is much more stable nowadays.


#### Next steps
Moving forward, I recommend utilizing the VAR model in real-life scenarios for financial forecasting of upcoming seasons. Additionally, there's potential for further improvement by incorporating pricing data into the dataset. This would allow for more nuanced predictions that could inform ticket pricing strategies, enhancing the SBB's ability to meet financial goals and adapt to changing market conditions.

#### Outline of project

- [Link to notebook](https://github.com/flonotter/SBB/blob/main/SBB.ipynb)


##### Contact and Further Information
flo.notter@gmail.com
