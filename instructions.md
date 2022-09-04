Speed of sound prediction
=========================

This machine learning project predicts the speed of sound in electrolytic aqueous solutions.

Directory structure
-------------------

*   [`instructions.md`](instructions.md) - file with instructions on experiment running.

*   [`data`](data) - directory with input CSV files.

*   [`datasets`](datasets) - directory with preproccesed datasets.

*   [`notebooks`](notebooks) - directory with Jupyter notebooks.

*   [`htmls`](htmls) - directory with all notebooks exported as HTML files.

*   [`environment.yml`](environment.yml) - conda environment file with Python dependencies.


Prerequisities
--------------

All dependencies are listed in [`environment.yml`](environment.yml) file.

Running the experiment
----------------------

To run the full experiment, the following notebook order must be maintained. All notebooks are stored in [`notebooks`](notebooks).

**Step 1:** [`data_loading.ipynb`](notebooks/data_loading.ipynb)

*   loads CSV files from `data/`

*   contains data visualizations


**Step 2:** [`features_addition.ipynb`](notebooks/features_addition.ipynb)

*   enhances dataframes loaded in Step 1 with ion specific features

*   scales all the ion specific features

*   concatenates dataframes for all media into one

*   saves the full dataframe as `dataset.csv` into `datasets/`


**Step 3:** [`baseline_models.ipynb`](notebooks/baseline_models.ipynb)

*   loads `dataset.csv` created in Step 2

*   normalizes temperature and molality features

*   splits data into train, validation and test sets

*   tests baseline models


**Step 4:** [`svm_model.ipynb`](notebooks/svm_model.ipynb) and [`rf_model.ipynb`](notebooks/rf_model.ipynb)

*   performs Bayesian hyperparameter optimization on SVM, respectively random forest model


**Step 5:** [`feature_selection.ipynb`](notebooks/feature_selection.ipynb)

*   performs forward and backward feature selection

*   Step 4 can be repeated with new feature sets


**Step 6:** [`model_evaluation.ipynb`](notebooks/model_evaluation.ipynb)

*   evaluates optimized SVM and random forest models on three tests

    *   general test

    *   inside matrix test

    *   outside matrix test
