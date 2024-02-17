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

#### Methodology
My approach involved using four different prediction models, evaluating their performance with two key metrics: Mean Square Error (MSE) and Mean Absolute Error (MAE). This comprehensive evaluation allowed me to identify the most accurate model for the specific forecasting needs.

#### Results
My findings were encouraging, indicating that predicting the number of tickets sold is a feasible task with relatively low error rates. This suggests that the models I developed can provide reliable forecasts for future sales.

#### Next steps
Moving forward, I recommend utilizing the VAR model in real-life scenarios for financial forecasting of upcoming seasons. Additionally, there's potential for further improvement by incorporating pricing data into the dataset. This would allow for more nuanced predictions that could inform ticket pricing strategies, enhancing the SBB's ability to meet financial goals and adapt to changing market conditions.

#### Outline of project

- [Link to notebook 1](https://github.com/flonotter/SBB/blob/main/SBB.ipynb)


##### Contact and Further Information
flo.notter@gmail.com
