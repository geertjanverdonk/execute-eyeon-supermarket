# EyeOn Supermarket data science case study

## Introduction

Brick-and-mortar grocery stores are always in a delicate dance with purchasing and sales forecasting. Predict a little over, and grocers are stuck with overstocked, perishable goods. Guess a little under, and popular items quickly sell out, leaving money on the table and customers fuming.

The problem becomes more complex as retailers add new locations with unique needs, new products, ever transitioning seasonal tastes, and unpredictable product marketing. Corporación Favorita Grocery Sales (CFGS), a large Ecuadorian-based grocery retailer, knows this all too well. They operate hundreds of supermarkets, with over 200,000 different product-store combinations.

CFGS has challenged you to help in the forecasting process. They currently rely on subjective forecasting methods with very little data to back them up and very little automation to execute plans. CFGS have collected a large dataset containing detailed point-of-sale data and data on external factors. They’re excited to see what insights you bring and what steps you suggest to improve their forecast.

## Case assignment

We invite you to shed some light on the CFGS case, with CRISP-DM as a guideline.

### Business understanding

- Why is it important for CFGS to make their forecast less subjective?
- How can the business context of the case be used in the analysis of the data?

### Data understanding

The data is provided in the `data` folder. Consider how this data can help you in solving this challenge:

- How complete is the data?
- What kind of business dynamics do you recognize in the data?
- Which patterns do you see in the historical sales (trend, seasonality, events, week patterns, etc.)?
- What are your hypothesis on the underlying causes for the patterns that you find?

Based on your initial insights, what would be your advise to the sales manager on the period September to December. Use the data to answer support your advice and present your insights in a compelling story during the interview. We are keen to see not only your results, but also what approach you’ve taken. Use your creativity to find insights that will raise CFGS’s interest and show’s them the value of their data.

### Data preparation and modeling

TODO: add specific modeling tasks

## Using the data

Start with downloading or cloning this repository to your local machine. The data is provided in [Apache parquet](https://parquet.apache.org/) format, which requires [pyarrow](https://arrow.apache.org/docs/python/) (recommended) or [fastparquet](https://github.com/dask/fastparquet) (alternative):

```
pip install --user pyarrow
```

You can then load the data as follows

```python
import pandas as pd

df = pd.read_parquet('./data/history-per-year.parquet')
```

Note that `history-per-year.parquet` span multiple folders and files; it is [partitioned](https://arrow.apache.org/docs/python/parquet.html#reading-from-partitioned-datasets) by `year` and `month`. Do not change names of the folders or files.

## Attribution

This case study, including the data, was generously provided by [EyeOn](https://www.eyeon.nl/) for teaching purposes. 
