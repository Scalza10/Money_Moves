# Term Project for Data Analytics
Term project based on the stock price of apple share and a collection of indicators of 2018 stock data.

## Motivation for this project

When we started this project I was curios to find out how accurately I would be able to predict the future stock price of a company based on historical data. Also I wasnted to learn which company were profitable based on certain parameters. All of this so I could make better educated guesses at what the stock market would look tomorrow. With these tools at my dispostion, I would be able to prfit of changes on the daily prices of a certain stock.

## Prerequisites

### Built With

* [Python](https://www.python.org/) - Language used.
* [Azure Notebooks](https://notebooks.azure.com/) - Software used.

### Libraries Required
This project was made in the Python language, utilizing Azure notebooks.
The Libraries that are require for this Python project to properly run are:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt #Data visualisation libraries
import seaborn as sns
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn import metrics
from statsmodels.tsa.arima_model import ARIMA
from sklearn.metrics import mean_squared_error
import statistics

#The following function is use in the time series analysis and is not include in conventional libraries.
def smape_kun(y_true, y_pred):
    return np.mean((np.abs(y_pred - y_true) * 200/ (np.abs(y_pred) +       np.abs(y_true))))
 
from sklearn.externals.six import StringIO
from IPython.display import Image
from sklearn.tree import export_graphviz
import pydotplus

```

### Gathering the data

The data for this project was gathered from the webpage Kaggle in the following links [Indicators](https://www.kaggle.com/cnic92/200-financial-indicators-of-us-stocks-20142018/data#) [Apple Data](https://www.kaggle.com/camnugent/sandp500#all_stocks_5yr.csv) .

The first data set includes indicators data (223 indicators to be precise) from 2014 to 2018. Only 2018 was used in this project.
The Second data set contains Stock price data for a large list of stocks from 2013 to 2018. Only Apple was considered in this study.

### Analysis on the data

The Data was divided in two main data sets that then were analyzed. The Apple data set was analyzed in a times series analysis. An ARIMA model was utilized in order to predict future stock prices. The other data set was utilized to categorize the profitability of a company based on certain indicators.

### Visualizations
These are some visualization that were obtained from mine analysis. they will provide a summary of what mine conclusions were.

<details>
           <summary>Average Share price</summary>
           <p>
         
The following visualization shows How the price changed throughout the years. It shows minimun, max and average value
![alt text](https://github.com/TheCodeMaster2030/Money_Moves/blob/master/code/download.png?raw=true)

</p>
</details>
<details>
           <summary>Time Series</summary>
           <p>
                      
   This is mine actual time series model and one can see the predicted values and how close they were to the actual value. The model had a good accuracy interval.

![alt text](https://github.com/TheCodeMaster2030/Money_Moves/blob/master/code/Time_series.png?raw=true)
  </p>
         </details>
<details>
           <summary>Decision Tree</summary>
           <p>
  
  This Tree classifies a compny in whether it is profitable or not based on three indicators: Gross Margin, EPS, and return on assests.
             
![alt text](https://github.com/TheCodeMaster2030/Money_Moves/blob/master/code/Decision_tree.png?raw=true)
 
 </details>
         

## Authors


* **Sebastian Calzadilla** - *The one and only*


## License

This project is licensed under the STU License(Dpt. Of Science).
## Acknowledgments

* **Dr. Mondesire, S.** - *Spiritual guide*
* **Pier Paolo Ippolito** - His model was the one I studied and adapted for the time series analysis [His Link](https://towardsdatascience.com/stock-market-analysis-using-arima-8731ded2447a)
* **God** - *He was always there*
