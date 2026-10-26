# Beer Review Machine Learning Project

This project was completed for **ME315: Machine Learning in Practice**. It investigates whether machine learning models can predict the overall ratings of beers using review scores and beer characteristics.

## Project Overview

The project uses BeerAdvocate beer reviews to explore review characteristics and develop predictive models for overall beer ratings.

The analysis includes:

- Exploratory data analysis (EDA)
- Data preprocessing and missing-value handling
- Feature preparation
- Regression model training and evaluation
- Cross-validation and hyperparameter tuning
- Model comparison using a held-out test set

## Repository Contents

| File | Description |
|---|---|
| `RevisedProjectME315.ipynb` | Jupyter notebook containing the analysis and machine learning workflow |
| `beer_reviews.csv` | Beer review dataset |
| `ME315_Project_Report.pdf` | Final project report |
| `.gitattributes` | Git LFS configuration for the dataset |

## Dataset

The dataset contains beer reviews originally sourced from BeerAdvocate and obtained through Kaggle.

**Potential source:** [Beer Reviews — Kaggle](https://www.kaggle.com/rdoume/beerreviews)

The dataset includes information such as beer names, beer styles, alcohol by volume (ABV), brewery information and review ratings.

The main variables used in the analysis include:

- `review_overall` — overall beer rating and prediction target
- `review_aroma` — aroma rating
- `review_appearance` — appearance rating
- `review_palate` — palate rating
- `review_taste` — taste rating
- `beer_abv` — alcohol by volume
- `beer_style` — beer style category

A sample of 50,000 reviews was used for model development and evaluation.

**Data attribution:** The dataset was obtained from Kaggle and was not originally collected for this project. The exact source and applicable licence should be confirmed against the original dataset page before redistribution.

## Methodology

The project follows a supervised machine learning workflow:

1. Explore the dataset and examine the distribution of review ratings.
2. Preprocess the data, including handling missing values.
3. Split the data into training and test sets.
4. Train and tune regression models using cross-validation.
5. Evaluate model performance on held-out test data.
6. Compare the models using RMSE, MAE and \(R^2\).

The regression models evaluated include:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regression

## Results

The models achieved broadly similar performance on the held-out test set.

| Model | RMSE | MAE | \(R^2\) |
|---|---:|---:|---:|
| Linear Regression | 0.410 | 0.308 | 0.665 |
| Ridge Regression | 0.410 | 0.308 | 0.665 |
| Lasso Regression | 0.410 | 0.308 | 0.665 |
| Random Forest Regression | 0.412 | 0.311 | 0.662 |

Lower RMSE and MAE indicate smaller prediction errors, while a higher \(R^2\) indicates that a model explains more of the variation in overall ratings.

In this evaluation, the linear models performed marginally better than the Random Forest model.

## Tools and Libraries

The project was developed using Python and Google Colab, with libraries including:

- pandas
- NumPy
- scikit-learn
- Matplotlib
- Seaborn

## How to Run

1. Clone or download this repository.
2. Install the Python libraries required by the notebook.
3. Open `RevisedProjectME315.ipynb` in Jupyter Notebook or Google Colab.
4. Ensure `beer_reviews.csv` is accessible at the file path expected by the notebook.
5. Run the notebook cells to reproduce the analysis and model evaluation.

The dataset is stored using Git Large File Storage (Git LFS) because of its size.

## Project Report

See [`ME315_Project_Report.pdf`](ME315_Project_Report.pdf) for the full report, including the methodology, analysis, model evaluation and findings.

---

*Academic project for ME315: Machine Learning in Practice.*
