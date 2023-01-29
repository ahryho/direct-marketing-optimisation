# Data science: Direct marketing optimisation

## Task: Use dummy data to maximise revenue from direct marketing campaigns.

## Data:

-   Social-demographical data (age, gender, tenure in a bank)

-   Products owned + actual volumes (current account, saving account, mutual funds, overdraft, credit card, consumer loan)

-   Inflow/outflow on C/A, aggregated card turnover (monthly average over past three months)

-   For 60 % of clients, actual sales and revenues from these are available (training set)

## Conditions:

The bank has the capacity to contact only 15 pct. of the clients (cca 100 people) with a marketing offer, and each client can be targeted only once.

## Proposed steps:

1.  Create an analytical dataset (both training and targeting sets)

2.  Develop three propensity models (consumer loan, credit card, mutual fund) using the training data set

3.  Optimise targeting clients with the direct marketing offer to maximise the revenue

## Expected result:

1.  Which clients have a higher propensity to buy a consumer loan, CL?

2.  Which clients have a higher propensity to buy a credit card, CC?

3.  Which clients have a higher propensity to buy a mutual fund, MF?

4.  Which clients are to be targeted with which offer? General description.

5.  What would be the expected revenue based on your strategy?

The executive summary of the analysis should not be larger than two pages. Attach the technical report, list of clients to be contacted with which offer, data, algorithms and codes used.

## Solution:

1.  Repository structure:

-   folder *data*: input and QC'ed datasets

-   folder *notebooks*: jupyter-notebooks with data pre-processing, model development and summary of the results

-   folder *results*: three lists of clients with a higher propensity to buy CL, CC, MF, and a list of clients to be contacted to get maximum revenue.

2.  Create and activate a conda environment, and run jupyter-notebook:

``` sh
conda env create -f conda-env.yml
conda activate dmo
jupyter-notebook
```

3.  Notebooks:

- *01_transform_ds.ipynb*: aggregate all data into one dataset. The result is in the `dmo.csv`.

- *02_exploratory_data_analysis.ipynb*: EDA of the given dataset. The output is in the `dmo_reduced.csv`.

- *03_model.ipynb*: feature selection procedure, model development, revenue prediction, results' explanation.
