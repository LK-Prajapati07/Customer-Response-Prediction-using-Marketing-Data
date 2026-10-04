# Customer Response Prediction using Marketing Data

This project analyzes customer records from a marketing campaign dataset and explores whether a customer is likely to respond to a campaign. The analysis is implemented in the notebook `AIML.ipynb` and uses the dataset in `data.csv`.

## Overview

The dataset contains customer demographic, purchase, and campaign-response information. It is suitable for supervised learning tasks where the target variable is whether the customer responded to the campaign.

The project includes:
- Loading and inspecting the dataset
- Handling missing values
- Performing exploratory data analysis (EDA)
- Preparing the dataset for model training
- Building a machine learning model to predict customer response

## Dataset

File: `data.csv`

The dataset has 2,240 rows and 22 columns.

### Target variable
- `Response`: binary flag indicating whether the customer responded to the marketing campaign (1 = responded, 0 = did not respond)

### Main features

| Column | Description |
|---|---|
| `ID` | Unique customer identifier |
| `Year_Birth` | Customer birth year |
| `Education` | Education level (Graduation, PhD, Master, etc.) |
| `Marital_Status` | Marital status |
| `Income` | Annual household income |
| `Kidhome` | Number of children in the household |
| `Teenhome` | Number of teenagers in the household |
| `Dt_Customer` | Date when the customer joined the database |
| `Recency` | Number of days since last purchase |
| `MntWines` | Amount spent on wine |
| `MntFruits` | Amount spent on fruits |
| `MntMeatProducts` | Amount spent on meat |
| `MntFishProducts` | Amount spent on fish |
| `MntSweetProducts` | Amount spent on sweets |
| `MntGoldProds` | Amount spent on gold products |
| `NumDealsPurchases` | Number of purchases made with deals |
| `NumWebPurchases` | Number of purchases made on the website |
| `NumCatalogPurchases` | Number of purchases made through a catalog |
| `NumStorePurchases` | Number of purchases made in stores |
| `NumWebVisitsMonth` | Number of website visits per month |
| `Complain` | Whether the customer filed a complaint |

## Data quality notes

The notebook identifies missing values in the `Income` column and fills them using the mean income value before model preparation. The dataset is otherwise complete for most fields.

The response rate is approximately 15%, which indicates a class imbalance typical of marketing response datasets.

## Project Structure

- `data.csv` — marketing customer dataset
- `AIML.ipynb` — Jupyter notebook with data analysis and ML workflow
- `requirements.txt` — Python dependencies
- `Readme.md` — project documentation

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn

## Setup

1. Clone or download the project.
2. Create a virtual environment (optional but recommended).
3. Install the dependencies:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook AIML.ipynb
```

## Objective

The main goal is to build a predictive model that estimates whether a customer is likely to respond to a marketing campaign based on historical customer behavior and demographic attributes.

This type of analysis is useful for:
- targeted marketing campaigns
- customer segmentation
- sales forecasting and campaign optimization
- identifying high-value customers

## Example Use Cases

- Predict whether a new customer will respond to a campaign
- Analyze how purchase behavior relates to customer demographics
- Identify the strongest indicators of campaign response
- Improve the efficiency of marketing spend

## License

This project is intended for educational and research use.
