# ASRI 2022: PPP Loan Analysis

Code and materials from a project I worked on at the Arkansas Summer Research Institute (ASRI) in summer 2022. ASRI is an NSF EPSCoR-funded summer school that brings together students from more than two dozen states to work on a real machine-learning problem and to meet researchers and industry practitioners.

## The question

Our project used public Paycheck Protection Program (PPP) loan data from the U.S. Small Business Administration to look at who received loans and how much they received, with attention to gender and racial disparities in initial loan approvals. Related work on lending discrimination is included in this repository (`Atkins2022_Article_DiscriminationInLendingEvidenc.pdf`, `SSRN-id3864218.pdf`, `NYU Research Note.pdf`).

## What is here

| File | Contents |
|---|---|
| `ASRI_final.ipynb` | Loads the loan files, filters out zero and missing values, and examines the relationship between initial approval amount and reported jobs |
| `ASRI_model.ipynb` | Joins loans to ZIP-code median income and fits regression models (linear, polynomial, decision tree) to relate income to loan amounts and loans per capita, with k-fold cross-validation |
| `business-int.py` | Starter script from the workshop for loading the SBA loan files |
| `Final Presentation.pptx` | Slides from the final presentation |
| `Info _ Citations - Intermediate SBA.docx` | Notes on the data and citations |

## Running the notebooks

The notebooks read local copies of the SBA PPP loan CSV files and a ZIP-code income table from Kaggle, and those paths are hard-coded to my machine. The data are not included here. To rerun the analysis, download the PPP files from the SBA, download the income table, and change the paths at the top of each notebook. You will need `pandas`, `numpy`, `dask`, `scikit-learn`, `statsmodels`, `seaborn`, and `matplotlib`.

## Status

This is a short summer project from 2022 and is kept as a record of that work. The notebooks are exploratory and have not been cleaned up.
