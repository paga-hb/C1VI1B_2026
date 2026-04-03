
---

# Phase: Data Preparation

## Task: Select Data

### Output: Rationale for Inclusion/Exclusion

Here you need to list the data to be included/excluded in the project and rationale (reasons for these decisions).
- Criteria can include relevance to the data mining goals, quality, and technical constraints such as limits on data volume or data types.
- Note that *data selection* covers selection of attributes (columns, features) as well as selection of records (rows) in a dataset/table.

## Task: Clean Data

### Output: Data Cleaning Report

Here you need to describe decisions and actions taken to address the data quality problems reported during `Task: Verify Data Quality` of `Phase: Data Understanding`.

You also have to consider transformations of the data for cleaning purposes and the possible impact on the analysis/visualizations.
- This may involve selection of clean subsets of the data, the imputation and/or deletion of missing values, changing data types and/or names of attributes (columns, features), etc.

## Task: Construct Data

### Output: Derived Attributes

Here you need to describe *derived attributes*, which are new attributes (columns, features) that are constructed from other existing attributes (i.e. *feature engineering*), e.g.:

$$area = length \times width$$

$$bmi = \frac{weight}{height^2}$$

### Output: Generated Records

Here you need to describe the creation of any new records (rows), if any.

## Task: Integrate Data

### Output: Merged Data

Here you need to describe merged datasets/tables, which refers to joining together two or more  datasets/tables that have different information about the same *objects*.

You also want to describe any aggregations, e.g. new values computed by summarizing information from multiple records (rows) and/or datasets/tables.

## Task: Format Data

### Output: Reformatted Data

Here you need to describe any reformatting of the data done (if any), which could include changing the order of the attributes (columns, features) and/or the records (rows).

**Note:** This is more important for machine learning.

## Main Output

This is not listed as a Generic Task in CRISP-DM, but is essentially a listing of (with descriptions) the resulting datasets from the Tasks above.

### Output: Datasets

Here you need to list the dataset(s) produced by the data preparation phase, which will be used for the major analysis work and visualizations of the project.

### Output: Dataset Descriptions

Here you need to describe the dataset(s) that will be used for the major analysis work and visualizations of the project.