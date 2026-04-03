
---

# Phase: Data Understanding

## Task: Collect Initial Data

### Output: Initial Data Collection Report

The initial data has already been collected, and is stored in the `data` folder together with the *data dictionary* (i.e. descriptions or each column/feature in each dataset) in the `data/data_dictionary` folder.

The datasets are:
- `vg_charts.csv`
- `vg_developers.csv`
- `vg_publishers.csv`
- `vg_geo_cities.csv`
- `vg_geo_countries.csv`

## Task: Describe Data

### Output: Data Description Report

- Here you need to describe the data that has been acquired, including the format of the data, the quantity of data (for example, the number of records (rows) and fields (columns) in each dataset/table), the identities of the fields, and any other surface features which have been discovered.
- You also have to evaluate whether the data acquired satisfies the relevant requirements (or if you need to collect more data).

## Task: Explore Data

### Output: Data Exploration Report

- Here you need to describe the results of this task, including first findings or initial hypothesis and their impact on the remainder of the project:
  - This task addresses the data mining questions (under `Phase: Business Uuderstanding -> Task: Determine Data Mining Goals`) using querying, visualization, and reporting techniques.
  - These include distribution of key attributes (e.g. sales, regions, genres, platforms, etc.) relationships between pairs of attributes, results of simple aggregations, properties of significant sub-populations (e.g. groupings of genres, platforms, etc.), and simple statistical analyses (counts, sums, means, standard deviations, etc.).
  - These analyses may directly address the data mining goals; they may also contribute to or refine the data description and quality  reports, and feed into the transformation (e.g. merging, feature engineering) and other data preparation steps (e.g. cleaning) needed for further analysis.
- If appropriate, include graphs and plots to indicate data characteristics that suggest further examination of interesting data subsets.

## Task: Verify Data Quality

### Output: Data Quality Report

Here you need to list the results of the data quality verification, i.e. if quality problems exist, possible solutions to data quality issues, etc.

This includes examining the quality of the data, addressing questions
such as:
- Is the data complete (i.e. does it cover all the cases required, or will you need to collect more data)?
- Is it correct, or does it contain errors and, if there are errors, how common are they?
- Are there missing values in the data? If so, how are they represented, where do they occur, and how common are they?