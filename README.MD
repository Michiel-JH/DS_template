# Content

This cookiecutter template is meant to provide your with a framework for structuring your modelling projects. 
This readme contains the following sections

1. How to start using it
2. Relative path usage
3. Folder structure
4. Workflow


## 1. How to start using it

Simple copy paste the following command in your terminal to create the folder stucture in your current director:

```
cookiecutter https://bitbucket.org/aimdeloittenl/mle_cookiecutter/src/main/
```

## 2. Relative path usage

To ease the adoption of your project code by someone else it is good practice to use a relative path as opposed to absolute paths.
Using relative paths ensures someone else does not have to hardcode his/her path in the various scripts. An example is given below.

```
Absolute path: "C:/aimdeloittenl/mle_cookiecutter/src/main/{{cookiecutter.project_name}}/modelling/modelling_decisions.md"
relative path: "modelling/modelling_decisions.md"
```

## 3. Folder structure

```


├── data                            Folder that contains all data                         
│   |
│   ├── bronze                      The original, immutable data dump. Can contain excel files for smaller projects
|   └── silver                      Data that is filtered and cleansed. Can contain excel files for smaller projects
|   └── gold                        The final, business-level aggregated, canonical data sets for modelling. Can contain excel files for smaller projects
|
├── EDA                             Folder to do exploratory data analysis
|
├── ETL                             Folder for ETL processes, maturing the data from bronze, to silver to gold. Can be done by analysts themselves in smaller projects (preprocessing)
|
├── modelling                       Folder to model data and save them
│   |                               
|   └── modelling_decisions.md      Place to reflect on hyperparameters, outliers, scope & technical limitations, model assumptions & sensitives and model explainability.
|
├── requirements.txt                The requirements file for reproducing the analysis environment. Generated with `pip freeze > requirements.txt`
|
├──.gitignore                       States explicitly which files GIT should ignore, such as the data and secret information
|
├── readme.md                       Introduces and explains the project   
|
├──.pre-commit-config.yaml          File to declare GIT hooks, automatically checking simple issues before submission to code review



``` 

## 4. Workflow

Depending on the size of the project the ETL process is done by an engineer or as a preprocessing step yourself. 
![Folder structure workflow](workflow.jpeg)