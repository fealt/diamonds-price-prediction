<img src="https://bit.ly/2VnXWr2" width="60">

##### *Data Analytics Bootcamp* – Mini Project
##### October 2021

<br>

## The Linear Regression Challenge: Diamonds Price Prediction 💎🏷🤑

Authors:

* **Natália Mendes Ceoldo** ▫︎ [GitHub](https://github.com/natmceoldo) ▫︎ [LinkedIn](https://www.linkedin.com/in/natmceoldo/)

* **Felipe Altermann** ▫︎ [GitHub](https://github.com/fealt) ▫︎ [LinkedIn](https://www.linkedin.com/in/felipealtermann/)

<br>

<br>

## Project Documentation
- [Project Description](#project-description)
- [Metrics](#metrics)
- [Conclusion](#conclusion)
- [Deliverable files in this repository](#deliverables)
- [Tech](#tech)
- [Data source](#data_source)


<a name="project-description"></a>

## Project Description

* Work with data to understand the characteristics of a diamond which are most likely to influence its price.

* Rick – *our client* – has 5,000 diamonds and asked us to estimate their price based on a historic dataset with over 54,000 diamond prices.

![img](./images/challenge_objectives.png)

<a name="metrics"></a>

## Metrics

**The metric of success is, of course, money** 💲💰💲💰💲

* Our assignment is to estimate the price of Rick’s 5,000 diamonds achieving the smallest amount of error, so he can sell them properly.

* We will specifically measure the **root mean squared error (RMSE)** of our predictions.

* Rick’s goal is to obtain an average error **below 900 dollars**.

<br>


<a name="conclusion"></a>

## Conclusion

```

▫️ The price of a diamond has a directly correlation with its carat. It is not a straight linear correlation, but exponential one, and there are others relevant features that influences its price, as the color, clarity and cut.

▫️ Our first approach was to predict the price using a regression for each color category and carat, clarity and cut as independent variables, and we had a good result of RMSE 979,66 USD, almost beating the goal. Then we tried to improve the model using a new variable that classified if the diamond's carat belongs to the first 3 quartiles or not, according to our historical data. With that improvment we have got a slightly better result with a RMSE of 967.38 USD.

▫️ On our second approach we switched the way we used the color and clarity to create our model, i.e., we created a regression for each clarity, and used color as independent variable along with carat and cut. With this second approach we got our best result of RMSE of 791.55 USD. Then we tried same strategy to improve the model inclunding the variable that classifies if the diamond's carat belongs to the first 3 quartiles of the historical sample, but the results were worsened, going to RMSE of 1,213.73 USD.

▫️ We did not tried the approach using a different regression for each cut, because when we analysed it graphically on the scatterplot, it showed to be more spread than clarity and color.

▫️ At the end, we can conclude that the order of the 4 C's features that most influences the prices are: carat, clarity, color and cut.

▫️ One thing to notice with this challenge is that when we calculate the RMSE using the data used for the model we always got lower values than with the rick's dataset, because the model is biased with the data it used to be created from.

```

![img](./images/Rick_Predicted_02_A.png)

<a name="deliverables"></a>

## Deliverables in this repository

* A *.csv* file containing the data related to the 5,000 diamonds and a new column named *'price_predicted'* with the predictions from our *linear regression model*.
* Upload the *.csv* file to this [LINK](https://daft-oct2020-rick-diamonds.herokuapp.com/) – the web site will calculate the root mean squared error (RMSE) based on its own algorithms.

* Rick cleaned final datasets (./final_csv):
   - `Diamonds_Analysis_01_A.csv`
   - `Diamonds_Analysis_01_B.csv`
   - `Diamonds_Analysis_02_A.csv`
   - `Diamonds_Analysis_02_B.csv`

* Data analysis in Jupyter Notebook:
   - `Diamonds_Analysis_01_A.ipynb`
   - `Diamonds_Analysis_01_B.ipynb`
   - `Diamonds_Analysis_02_A.ipynb`
   - `Diamonds_Analysis_02_B.ipynb`

* Images with the resulted analysis after checked by the above mentioned website:
   - `Rick_Predicted_01_A.png`
   - `Rick_Predicted_01_B.png`
   - `Rick_Predicted_02_A.png`
   - `Rick_Predicted_02_B.png`

<br>


<a name="tech"></a>

## Tech

   - Python @ Jupyter Notebook
   - Pandas / Numpy
   - Matplotlib / Seaborn
   - Sklearn (LinearRegression / mean_squared_error)

<br>


<a name="data_source"></a>

## Data source

  - Rick's Dataset in CSV format (5,000 rows and 10 different columns) named *rick_diamonds.csv* (./data). 

  - Dataset with historic diamonds prices in CSV format (~49,000 rows and 11 different columns) named *hist_diamonds.csv* (./data).

<br>

<br>
