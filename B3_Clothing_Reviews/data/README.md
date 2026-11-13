# Dataset: Women's E-Commerce Clothing Reviews

## Source
- **Kaggle**: [nicapotato/womens-ecommerce-clothing-reviews](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews)
- **File**: `Womens Clothing E-Commerce Reviews.csv`

## Download Instructions

### Option 1: Kaggle CLI (Recommended)
```bash
pip install kaggle
# Place your kaggle.json API token in ~/.kaggle/
kaggle datasets download -d nicapotato/womens-ecommerce-clothing-reviews -p data/ --unzip
```

### Option 2: Manual Download
1. Go to https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews
2. Click "Download" (requires a free Kaggle account)
3. Extract the CSV file into this `data/` directory

## Dataset Overview
- **Records**: 23,486 reviews
- **Columns** (10):
  | Column | Description |
  |--------|-------------|
  | Clothing ID | Integer categorical variable referring to the specific piece |
  | Age | Positive integer, reviewer's age |
  | Title | String, title of the review |
  | Review Text | String, body of the review |
  | Rating | Ordinal integer 1–5, the customer's rating |
  | Recommended IND | Binary (0/1), whether the customer recommends the product |
  | Positive Feedback Count | Integer, number of other customers who found the review positive |
  | Division Name | Categorical name of the product high-level division |
  | Department Name | Categorical name of the product department |
  | Class Name | Categorical name of the product class |

## ⚠️ Leakage Warning
**Do NOT use `Recommended IND` as a feature** when predicting `Rating`. Both are filled in simultaneously by the same customer, so using one to predict the other constitutes data leakage.
