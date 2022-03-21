# Forecasting Net Prophet

This prototype application contains data preparation, analysis, and visualizations for all the time series data to predict search traffic for MercadoLibre, a popular e-commerce site in Latin America. 

This Jupyter notebook is broken down into sections fours steps and an optional fifth step, as followed:

1. Find unusual patterns in hourly Google search traffic

2. Mine the search traffic data for seasonality

3. Relate the search traffic to stock price patterns

4. Create a time series model with Prophet

5. (optional): Forecast revenue by using time series models

## Technologies
Click on the links below for documentation on each of the technologies used. This project uses the following libraries and dependencies:
+ [**Anaconda**](https://docs.anaconda.com/): an open source package and environment management system.
+ [**JupyterLab**](https://jupyterlab.readthedocs.io/en/stable/): an extensive environment using web-based user interface designed for data analysis. 
+ [**Pandas**](https://pandas.pydata.org/docs/getting_started/index.html): (included in Anaconda) a Python package data analysis toolkit.
+ [**hvPlot**](https://hvplot.holoviz.org/) incorporated into this project. 
+ [**Facebook Prophet**](https://facebook.github.io/prophet/): Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data
+ [**Pystan**](https://pypi.org/project/pystan/): a state-of-the-art platform for statistical modeling and high-performance statistical computation.
+ [**Holoviews**](https://hvplot.holoviz.org/): an open-source Python library designed to make data analysis and visualization seamless and simple.
+ [**Google Colab**](https://colab.research.google.com/): Colab allows anybody to write and execute arbitrary python code through the browser, and is especially well suited to machine learning, data analysis and education.

## Installation Guide

Check to ensure that packages mentioned above are installed on your machine by entering the following into your environment using `conda list`. If any of these techologies are not installed into your environment, click on the links above or use the corresponding codes in your terminal. The following can be installed on to your local machine, however it is not required when using **Google Colab** (provided in first code cell, see first image in **Usage**)

```
pip install pystan
conda install -c conda-forge fbprophet
```



## Usage 

1. Clone the repository `https://github.com/leighbadua/forecasting_net_prophet.git`
2. Open Jupyter notebook using [Google Colab](https://colab.research.google.com/) 
3.  Choose the Upload method to import the file with the extension `.ipynb` onto the site. 
Install and import the required libraries and dependencies using **Google Colab**. The first cell (as shown in the image below with the `!pip install` tells the notebook to install these packages into memory and it will not be stored permanently installed on your local machine. 

<img width="554" alt="image" src="https://user-images.githubusercontent.com/96001018/159162325-98612eb8-b10f-41f9-87de-77dd86011664.png">


### Import other required libraries and dependencies: 

<img width="533" alt="image" src="https://user-images.githubusercontent.com/96001018/159162364-14992b49-52cf-437d-b4b7-a92a072489ae.png">


### **Step 1: Find Unusual Patterns in Hourly Google Search Traffic**
<img width="830" alt="image" src="https://user-images.githubusercontent.com/96001018/159162434-62a5025e-0733-41e7-a9b8-50928047c8d5.png">

<img width="849" alt="image" src="https://user-images.githubusercontent.com/96001018/159162452-d68501be-f031-48ba-8603-9104a530e56a.png">


### **Step 2: Mine the Search Traffic Data for Seasonality**

Grouping the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday)

<img width="842" alt="image" src="https://user-images.githubusercontent.com/96001018/159162501-834fbeb1-3f48-4066-bcd9-9a105f6710c3.png">


hvPlot heatmap of the hour of the day and day of week search traffic.

<img width="854" alt="image" src="https://user-images.githubusercontent.com/96001018/159162516-e94a2972-c9e3-48b1-b256-ea723be1dc62.png">

Average Search Traffic by Week of the Year

<img width="845" alt="image" src="https://user-images.githubusercontent.com/96001018/159162591-5bb2774b-0011-49ac-bc93-04137a205804.png">


### **Step 3: Relate the Search Traffic to Stock Price Patterns**
Image of Mercado Stock Closing Price from January 2015 to July 2020. 

<img width="848" alt="image" src="https://user-images.githubusercontent.com/96001018/159162679-9c9046d5-1282-490b-a820-bc912762703e.png">

Image of Stock Closing Prices vs Search Traffic from January 2020 to June 2020.

<img width="853" alt="image" src="https://user-images.githubusercontent.com/96001018/159162753-9ef5301d-3c9a-44f5-95f1-ffc4e75b1253.png">

Showing Mercado Stock Volatility

<img width="845" alt="image" src="https://user-images.githubusercontent.com/96001018/159162797-60fa1fe4-8f0a-42d5-8bbe-945a166d3680.png">

Time Series Correlation table

<img width="845" alt="image" src="https://user-images.githubusercontent.com/96001018/159162844-66f173e5-ae3b-40c6-9014-ccab25e897ec.png">


### **Step 4: Create a Time Series Model with Prophet**

Prophet predicitons for the Mercado trends data

<img width="842" alt="image" src="https://user-images.githubusercontent.com/96001018/159162874-f457cbea-ce66-48c5-b516-8a693305b54e.png">

Time Series Components - yhat, yhat_lower, yhat_upper

<img width="862" alt="image" src="https://user-images.githubusercontent.com/96001018/159162923-c3dd989e-dd6b-4e33-bd56-c01f17a62dc0.png">

Time Series Components over last 2000 hours

<img width="851" alt="image" src="https://user-images.githubusercontent.com/96001018/159162945-99f01c82-2db6-4a6a-b591-4450d9954d94.png">

Forecast Mercado Trends (trend, weekly, yearly, daily graphs)

<img width="445" alt="image" src="https://user-images.githubusercontent.com/96001018/159163064-1a79f3f2-5244-4528-a017-ddd701090b0f.png">


### **Step 5 (Optional): Forecast Revenue by Using Time Series Models**

Prophet model of Mercado Daily Revenue

<img width="871" alt="image" src="https://user-images.githubusercontent.com/96001018/159163092-557dc0d7-f610-4e6c-9ed4-f694a19b40ef.png">


Future Trends DataFrame and Analyzing seasonal patterns in revenue

<img width="746" alt="image" src="https://user-images.githubusercontent.com/96001018/159163105-af434791-fef2-4acb-a8c1-c56eb679ce7f.png">


<img width="430" alt="image" src="https://user-images.githubusercontent.com/96001018/159163121-ffba7aa2-7382-431d-ba15-136b44c30fa9.png">


<img width="545" alt="image" src="https://user-images.githubusercontent.com/96001018/159163152-211544f3-9005-4588-9af7-4b7462e5066b.png">


Predicitons for Mercado Sales

<img width="732" alt="image" src="https://user-images.githubusercontent.com/96001018/159163170-4e00334e-6fc2-423e-a635-b2576b2152d1.png">


## Contributors

Leigh Anne Badua leighbadua@gmail.com 


## License
MIT







