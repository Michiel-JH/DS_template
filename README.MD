## Introduction

This folder structure is meant to provide your with a framework for structuring your modeling projects. 
This is a list of potential (not exhaustive) use cases:

* Forecasting
* Optimization
* Classification
* Outlier detection
* Time series analyses
* Clustering

## How to use it

Simple copy paste the following command in your terminal to create the folder stucture in your current director:
```
cookiecutter https://github.com/MichielWiel/DS_template
```

## Workflow

The various folders naturally have different purposes in the journey towards creating a proper model.
These are clarified in the figure below

```

├── data
│   ├── processed_data      <- The final, canonical data sets for modeling. Can contain excel files for smaller projects
│   └── raw_data            <- The original, immutable data dump. Can contain excel files for smaller projects
│
│
├── models                  <- Trained and serialized models, model predictions, or model summaries
│
|
├── src                     <- Source code for use in this project.
│   |
│   ├── ingest              <- Scripts to download or generate data
│   │   └── ingest.py
│   │
│   ├── Processing          <- Scripts to turn raw data into features for modeling
│   │   └── processing.py
│   │
│   ├── modelling           <- Scripts to train models and then use trained models to make predictions
│   │   │                      
│   │   ├── train_model.py
│   │   └── test_model.py
│   │
│   └── visualization       <- Scripts to create exploratory and results oriented visualizations
|    └── visualize.py
|
├── requirements.txt        <- The requirements file for reproducing the analysis environment. Generated with `pip freeze > requirements.txt`

``` 