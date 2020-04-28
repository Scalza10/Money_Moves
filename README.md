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
           <summary>Hypothesis testing</summary>
           <p>
         
The following visualization shows non pitchers' voting percentage for entering the hall of fame, according to their hits. Also, it states if they made it to the hall of fame or not.
![alt text](https://github.com/TheCodeMaster2030/Money_Moves/tree/master/code/download.png?raw=true)

The following visualization shows pitchers' voting percentage for entering the hall of fame, according to their Strikes Out. Also, it states if they made it to the hall of fame or not.
![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz4.png?raw=true)
</p>
</details>
<details>
           <summary>Linear Regression prediction</summary>
           <p>
                      
   Comparison among the actual voting percentage, our model predicted percentage, and the trend predicted percentage.

![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz7.png?raw=true)
  </p>
         </details>
<details>
           <summary>Classification</summary>
           <p>
  
  Non pitchers decision tree. It states if they made it to the hall of fame depending on a statistic.
             
![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz8.png?raw=true)
  Pitchers decision tree. It states if they made it to the hall of fame depending on a statistic.
             ![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz9.png?raw=true)
  </p>
</details>
<details>
           <summary>Times series analysis</summary>
           <p>
  
  Prediction for next years candidates' average strike outs according to our time series analysis.
             
 ![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz12.png?raw=true)
             
  Prediction for next years candidates' average hits according to our time series analysis.
             
  ![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz15.png?raw=true)
   
  As shown, this analysis couldn't be properly perform due to our data.
  </p>
         </details>
<details>
           <summary>Clustering</summary>
           <p>
  
  Clustering analysis that demonstrates the difference in statistics between pitchers and non pitchers. It shows that both classes have similar cluster even though there is a difference in the quantity of each class.
  
  ![alt text](https://github.com/datamonsters10/Term-Project-Data-Science/blob/master/Project%20Graphs/Viz18.png?raw=true)
  </p>
         </details>

## Authors

* **Claudio Lupi** - *The Brain*
* **Eduardo Reyna** - *The Muscle & Looks*
* **Sebastian Calzadilla** - *The Soul*


## License

This project is licensed under the STU License(Dpt. Of Science).
## Acknowledgments

* **Dr. Mondesire, S.** - *Spiritual guide*
* **Max Frank** - Helped to correct code
* **God** - *He was always there*
