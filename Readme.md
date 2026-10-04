# Customer Response Prediction using Marketing Data

This project predicts whether a customer is likely to respond to a marketing campaign using customer demographics and purchase behavior. The analysis is implemented in the notebook `AIML.ipynb`, and the workflow uses the dataset in `data.csv` along with serialized intermediate files saved as `.pkl` for reuse and faster processing.

## Overview

The dataset contains customer demographic, purchase, and campaign-response information. It is designed for a supervised learning problem in which the target variable indicates whether the customer responded to a campaign.

The workflow includes:
- loading and inspecting the dataset
- cleaning and preparing the data
- handling missing values
- performing exploratory data analysis (EDA)
- engineering features and preparing the model inputs
- training a machine learning model for response prediction
- saving processed outputs as pickle files for later use

## Dataset

File: `data.csv`

The dataset contains 2,240 rows and 22 columns.

### Target variable
- `Response`: binary label indicating whether a customer responded to the campaign (`1` = responded, `0` = did not respond)

### Key features

| Column | Description |
|---|---|
| `ID` | Unique customer identifier |
| `Year_Birth` | Customer birth year |
| `Education` | Education level |
| `Marital_Status` | Marital status |
| `Income` | Annual household income |
| `Kidhome` | Number of children in the household |
| `Teenhome` | Number of teenagers in the household |
| `Dt_Customer` | Date when the customer joined the database |
| `Recency` | Number of days since the last purchase |
| `MntWines` | Amount spent on wine |
| `MntFruits` | Amount spent on fruit |
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

The notebook identifies missing values in the `Income` column and fills them using the mean income before model preparation. The dataset is otherwise mostly complete, and the response rate is around 15%, which indicates a class imbalance typical of customer response data.

## Pickle files

This project also contains serialized pickle artifacts to store processed outputs and reusable feature data:

- `preprocessed_customer_data.pkl` — cleaned and transformed dataset used during preparation and modeling
- `customer_segmented_features.pkl` — feature-engineered customer data, likely used for segmentation or downstream analysis

These files are useful for saving intermediate outputs without re-running the full preprocessing pipeline.

## Project Structure

- `data.csv` — marketing customer dataset
- `AIML.ipynb` — notebook containing data analysis, preprocessing, and model building
- `preprocessed_customer_data.pkl` — saved preprocessed dataset
- `customer_segmented_features.pkl` — saved feature-engineered output
- `requirements.txt` — Python dependencies
- `Readme.md` — project documentation

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- pickle for serialized data storage

## Setup

1. Clone or download the project.
2. Create a virtual environment (recommended).
3. Install the dependencies:

```bash
pip install -r requirements.txt
```

4. Open the notebook:

```bash
jupyter notebook AIML.ipynb
```

## Objective

The main goal is to build a predictive model that estimates whether a customer is likely to respond to a marketing campaign using historical customer behavior and demographic attributes.

This kind of analysis can help with:
- targeted marketing campaigns
- customer segmentation
- campaign optimization
- identifying high-value customers
- improving marketing spend efficiency

## Example use cases

- Predict whether a new customer will respond to a campaign
- Understand how purchase behavior is related to customer demographics
- Detect the strongest indicators of campaign response
- Improve the efficiency and effectiveness of future campaigns

## License

This project is intended for educational and research use.
