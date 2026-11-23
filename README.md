# Credit Card Customer Analysis - Python EDA

An exploratory data analysis (EDA) of credit card customer data using Python. The project checks data quality, summarises customer demographics and spending, and uses charts and a correlation heatmap to find patterns in age, income and expenditure.

## Overview

The analysis covers **1,319 customers** and **13 columns**. It follows a standard EDA workflow: load and inspect the data, check for missing values and duplicates, compute descriptive statistics, and visualise distributions and relationships between variables.

## Tools Used

- Python 3
- Pandas and NumPy (data handling and statistics)
- Matplotlib and Seaborn (visualisation)
- Jupyter Notebook

## Repository Contents

| File | Description |
|------|-------------|
| `credit_card_analysis.ipynb` | Jupyter Notebook with the full analysis |
| `creditcard.csv` | Dataset (add it here or link to the source) |

## Dataset Description

| Column | Description |
|--------|-------------|
| `rownames` | Row index |
| `card` | Credit card application/ownership status (yes/no) |
| `reports` | Number of major derogatory reports |
| `age` | Customer age in years |
| `income` | Yearly income (in $10,000s) |
| `share` | Ratio of monthly credit card expenditure to yearly income |
| `expenditure` | Average monthly credit card expenditure |
| `owner` | Owner status (yes/no) |
| `selfemp` | Self-employed (yes/no) |
| `dependents` | Number of dependents |
| `months` | Months living at current address |
| `majorcards` | Number of major credit cards held |
| `active` | Number of active credit accounts |

> Column descriptions follow the public AER `CreditCard` dataset. Please verify them against your own data source.

## Analysis Steps

1. **Load and inspect** the data with `head()`, `shape`, `columns`, `info()` and `describe()`
2. **Check data quality** for missing values and duplicate rows
3. **Summarise categorical columns**: `card`, `owner` and `selfemp`
4. **Compute descriptive statistics**: mean income, age and expenditure, plus min and max expenditure
5. **Visualise the data**:
   - Histogram of customer age
   - Histogram of credit card expenditure
   - Bar chart of average expenditure by `owner`
   - Bar chart of average expenditure by `card`
   - Correlation heatmap of numeric variables
6. **Summarise findings** and write conclusions

## Key Findings

| Metric | Value |
|--------|-------|
| Total customers | 1,319 |
| Missing values / duplicates | None |
| Average expenditure | 185.06 (min 0, max 3,099.51) |
| Average income | 3.37 |
| Average age | 33.21 years |
| `card` = yes / no | 1,023 / 296 |
| `owner` = yes / no | 581 / 738 |
| Self-employed customers | 91 (about 7%) |
| Avg. expenditure, `owner` = yes | about 213.63 |
| Avg. expenditure, `owner` = no | about 162.56 |

- The dataset is clean, with no missing values or duplicates.
- Customers with `owner` = yes spend more on average than those with `owner` = no.
- Most customers are young (average age about 33) and very few are self-employed.
- Expenditure is right-skewed: most customers spend little, while a few spend a lot.

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Make sure `creditcard.csv` is in the same folder as the notebook.
4. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook credit_card_analysis.ipynb
   ```

## Skills Demonstrated

- Data loading and inspection
- Data quality checks
- Descriptive statistics and `groupby` aggregation
- Data visualisation
- Correlation analysis

## Future Improvements

- Remove the `rownames` index column before computing correlations
- Handle outliers in `expenditure` and unusually low `age` values
- Add income-group and age-group segmentation
- Build a simple model to predict card approval or spending

## Data Source

Add the source of your dataset here (for example, the AER `CreditCard` dataset or the Kaggle page you downloaded it from).

## Author

*Akhildas*
