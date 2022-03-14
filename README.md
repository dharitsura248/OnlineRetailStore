
![cover_photo](./images/Picture1.jpg)

# Online Retail Store

The idea of the project is to perform forecasting analytics and derive recommendations for the stocking the goods and staffing to meet the future demands. Based on the time of the year,month and day of the year.



## Introduction

A gift retail store, which has majority of customers as wholesalers. We want to be sure to have enough items in stock and be ready for the seasonal trends and surge in orders during the holiday seasons. The dataset contains transactions between 1/12/2009 and 9/12/2011. Our goal is to be able to come up with a model that would be able to accurately predict the total number of orders that we can expect in the coming days. This will help the business to be prepared for any hiring or packing requirements needed.

### Sales Case study

**Problem Statement** – How can the online gift retail store better stock up the goods in order to meet the growing demands?

**Context** – Online gift retail store has a significant presence in UK and ships internationally too. It is a wholesaler for gifts with over 4646 unique items. 

**Criteria for success** – The future sales should be in under acceptable error rate < 5%

**Constraints** – The customerId is doesn’t tell much about the customers information. The dataset is restricted to only the records we have received.

**DataSource** - [UCI Machine Learning Repository: Online Retail II Data Set](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II)

**Stakeholders** – Raghu Pattar

## Data Insights and Cleaning

In this process, I superfically analyzed the data inorder to understand what format the data is going to be and which changes are supposed to be made. The dataset contains approximately 1.06 million records for the transactions between 1/12/2009 and 9/12/2011. Our gift retail store received orders from almost 42 other countries apart from UK and served 4646 unique gift items on sale.

* **Problem 1:** The data contained records with (-ve) quantity which was associated with the returns for the order items or cancelled invoices and there were null customerId. **Solution:-** Drop records which belongs to returns or cancellation. As it would be a noise inorder for performing the forecasting.

* **Problem 2:** A few of the records had price set as 0 incorrectly. **Solution:-** Compute the median prices for the items based on their category,

* **Problem 3:** The dataset contained almost 90% of orders coming in from UK and only 10% which belonged to rest of the 42 countries. **Solution:-** Split the dataset into 2 different datasets - UK and Non-UK dataset. 

* **Problem 4:** CustomerId is null for almost 23% of the records. Since there was no associated customer information. It was best to drop these columns. 

## Exploratory Data analysis

In this step our goal is to further analyze and take a detailed look at the data presented to us. I try and look at which products are most bought from the store and how the price distribution of different products in the store. My further analysis included visualizing the sales pattern in different weeknumbers, days in a month and different hours of the day. I discovered that only 1% of the orders belonged to rest of the 42 countries. ~820k orders belonged to UK and so the exploratory analysis and cleaning activities were performed separated based on UK and the rest of the countries together. 

 


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


