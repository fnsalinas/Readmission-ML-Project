Diabetes Dataset Classification Project 
=======================================

Analyze factors related to readmission as well as other outcomes pertaining to patients in order to classify a patient-hospital outcome

3 different outputs:

1. No readmission

2. A readmission in less than 30 days (this situation is not good, because maybe your treatment was not appropriate);

3. A readmission in more than 30 days (this one is not so good as well the last one, however, the reason could be the state of the patient.

## Main Objective

> **How effective was the treatment received in hospital?** 

## Principal References

### Paper

Beata Strack, Jonathan P. DeShazo, Chris Gennings, Juan L. Olmo, Sebastian Ventura, Krzysztof J. Cios, and John N. Clore, “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records,” BioMed Research International, vol. 2014, Article ID 781670, 11 pages, 2014.

https://www.hindawi.com/journals/bmri/2014/781670/

### Dataset

https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008#

### Data description

https://www.hindawi.com/journals/bmri/2014/781670/tab1/

# Notebooks
**note:** I use plotly for make and interactive plots, but can be seen if you open the notebooks on github.

[1-readmited_preprocess.ipynb](https://github.com/JoseRZapata/Readmission-ML-Project/blob/master/notebooks/1-readmited_preprocess.ipynb) - Data loading and cleaning

[2-readmited_data_explore.ipynb](https://github.com/JoseRZapata/Readmission-ML-Project/blob/master/notebooks/2-readmited_data_explore.ipynb) - Data explore and analysis

[3-readmited_Models_imbalance.ipynb](https://github.com/JoseRZapata/Readmission-ML-Project/blob/master/notebooks/3-readmited_Models_imbalance.ipynb) (**Selected Model**) - Modeling with a imbalanced dataset.

**Modeling conclusions**

[4-readmited_Models_balanced.ipynb](https://github.com/JoseRZapata/Readmission-ML-Project/blob/master/notebooks/4-readmited_Models_balanced.ipynb) - Modeling  using smote for balanced the dataset

5-readmited_Models_imbalance_NoMeds.ipynb - Modeling with imbalanced dataset and no Medication features

# Selected Measure

The selected evaluation metric is the 
> **Recall - Sensitivity**

A False Negative might delay more tests or treatment, 
however a False Positive may just lead to more tests or treatments – not as costly as putting a life at stake.

# Selected Model

the selected model is the result of process detailed in 3-readmited_Models_imbalance.ipynb

The model is saved in the models folder:

`NB_pipeline_imbalance_recall.joblib`



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


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
