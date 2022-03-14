
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


