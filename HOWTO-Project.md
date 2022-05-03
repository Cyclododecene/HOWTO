# Guideline of Project Management

There are multiple articles have illustruated that the project(code) management are important:
1. [neptune.ai - how to organize deep learning projects](https://neptune.ai/blog/how-to-organize-deep-learning-projects-best-practices)
2. [深度学习科研，如何高效进行代码和实验管理？](https://www.zhihu.com/question/269707221/answer/350542551)

In this guideline, we will mainly show you to how to generate a tidy folder structure.

## cookiecutter-data-science

[Cookiecutter Data Science](https://github.com/drivendata/cookiecutter-data-science) is a logical, resonably standarized, but flexible project structure for doing and sharing data science work. To use it, you may follow these procedures:

0. initilize your python environment: `conda create -n template python=3.x` `conda activate template`
1. installation: `python -m pip install cookiecutter`
2. initlize your project `cookiecutter -c v1 https://github.com/drivendata/cookiecutter-data-science` (with following options)
  1. your project name
  2. your repo name
  3. author name
  4. description
  5. open source license
  5. s3 bucket (optional)
  6. python interpreter

The folder structure is as follows:

```bash
├── LICENSE
├── Makefile           <- Makefile with commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
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
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
├── src                <- Source code for use in this project.
│   ├── __init__.py    <- Makes src a Python module
│   │
│   ├── data           <- Scripts to download or generate data
│   │   └── make_dataset.py
│   │
│   ├── features       <- Scripts to turn raw data into features for modeling
│   │   └── build_features.py
│   │
│   ├── models         <- Scripts to train models and then use trained models to make
│   │   │                 predictions
│   │   ├── predict_model.py
│   │   └── train_model.py
│   │
│   └── visualization  <- Scripts to create exploratory and results oriented visualizations
│       └── visualize.py
│
└── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io
```


Then, you can add the project to your git repo.
