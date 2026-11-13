# Wine Reviews Dataset

## Source
- **Kaggle**: [Wine Reviews](https://www.kaggle.com/datasets/zynicide/wine-reviews)
- **File**: `winemag-data-130k-v2.csv`

## Download Instructions

### Option 1: Kaggle CLI
```bash
pip install kaggle
kaggle datasets download -d zynicide/wine-reviews -f winemag-data-130k-v2.csv -p data/
```

### Option 2: Manual Download
1. Visit https://www.kaggle.com/datasets/zynicide/wine-reviews
2. Download `winemag-data-130k-v2.csv`
3. Place it in this `data/` directory

## Dataset Description
- **Rows**: ~130,000 wine reviews scraped from WineEnthusiast
- **Columns**: 13 features + 1 unnamed index column

| Column | Description |
|--------|-------------|
| `country` | Country of origin |
| `description` | Tasting note / review text |
| `designation` | Vineyard designation within the winery |
| `points` | Rating on a scale of 80–100 (target variable) |
| `price` | Price of the bottle in USD |
| `province` | Province or state of origin |
| `region_1` | Wine-growing region |
| `region_2` | More specific sub-region (often missing) |
| `taster_name` | Name of the reviewer |
| `taster_twitter_handle` | Twitter handle of the reviewer |
| `title` | Title of the review |
| `variety` | Grape variety (e.g. Pinot Noir) |
| `winery` | Name of the winery |

## Notes
- The target variable `points` ranges from 80 to 100.
- `price` has ~8,996 missing values; requires imputation.
- The raw file contains thousands of exact duplicate reviews that must be removed before modeling.
