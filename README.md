# Airbnb Athens Analysis

This project explores Airbnb listings in Athens, Greece, with a focus on price formation, neighborhood concentration, host behavior, review activity, and listing availability.

The goal was to build a first end-to-end data science project: clean a real dataset, explore the market structure, engineer a small set of interpretable features, and test whether a simple regression model can explain Airbnb pricing patterns in Athens.

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

The analysis points to a few clear patterns:

- Airbnb supply is highly concentrated in central Athens, especially around the Acropolis and nearby tourist districts.
- Room type and neighborhood are the strongest drivers of price.
- Entire homes/apartments are consistently more expensive than private or shared rooms.
- Reviews, availability, and host scale show weaker relationships with price than location and property type.
- A baseline linear regression explains part of the variation in price, but much of the market remains shaped by factors not captured in the dataset.

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

5. Open `Airbnb_Athens_Analysis.ipynb` and run the notebook from top to bottom.

## Notes

- The notebook is written as a first portfolio project, so the focus is on clarity and reproducibility rather than production packaging.
- The model section uses both scikit-learn (baseline regression) and statsmodels (OLS summary and diagnostics).
- The dataset represents a snapshot of the Athens Airbnb market and should not be interpreted as a current market forecast.

## Limitations

This project is exploratory and uses a relatively small set of features for modeling.  
The regression should be read as an interpretable baseline rather than a production forecasting model.

A few limitations are important:

- the dataset is a snapshot of the market rather than a time series
- some important pricing variables are missing (for example amenities, property size, exact distances, and host history)
- location is simplified into neighborhood labels and clusters rather than richer spatial features

## Possible next steps

- Compare the baseline regression with Ridge or Lasso.
- Add richer spatial features, such as distance to landmarks or metro stations.
- Test a non-linear model to capture effects the linear baseline misses.
- Turn selected notebook findings into a short presentation style summary.
