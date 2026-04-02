# Airbnb Athens Analysis

This project explores Airbnb listings in Athens, Greece, with a focus on price formation, neighborhood concentration, host behavior, review activity, and listing availability.

The notebook follows a compact end-to-end workflow:
- data loading and cleaning
- exploratory data analysis
- feature engineering
- baseline linear regression
- model evaluation and diagnostics

## Main questions

The analysis focuses on a few practical questions:

- Where are Airbnb listings concentrated in Athens?
- Which neighborhoods and room types are associated with higher prices?
- How do host type, reviews, and availability relate to price?
- How much of Airbnb pricing can be explained with a simple linear model?

## Main findings

A few patterns stand out:

- Airbnb supply is highly concentrated in central Athens, especially around the Acropolis and nearby tourist areas.
- Room type and location are the strongest price drivers in the dataset.
- Entire homes command clearly higher prices than private or shared rooms.
- Reviews, availability, and host scale show weaker relationships with price.
- A baseline linear regression captures part of the pricing structure, but a large share of variation remains unexplained.

## Repository structure

```text
.
├── Airbnb_Athens_Analysis.ipynb
├── requirements.txt
└── data/
    └── raw/
        └── listings.csv
```

## Data

The notebook expects the dataset in one of the following locations:

- `data/raw/listings.csv`
- `data/listings.csv`
- `listings.csv`

The recommended location is:

```text
data/raw/listings.csv
```

## How to run

1. Clone the repository.
2. Create and activate a Python environment.
3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Launch Jupyter:

```bash
jupyter notebook
```

5. Open `Airbnb_Athens_Analysis_Portfolio.ipynb` and run the notebook from top to bottom.

## Notes

- The notebook is written as a first portfolio project, so the focus is on clarity and reproducibility rather than production packaging.
- The model section uses both scikit-learn (baseline regression) and statsmodels (OLS summary and diagnostics).
- The dataset represents a snapshot of the Athens Airbnb market and should not be interpreted as a current market forecast.

## Possible next steps

- Compare linear regression with Ridge or Lasso.
- Test non-linear models such as Random Forest or Gradient Boosting.
- Add richer location features, such as distances to landmarks or transit stations.
