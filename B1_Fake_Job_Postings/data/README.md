# Dataset: Real or Fake Job Posting Prediction (EMSCAD)

## Source
- **Kaggle**: [Real or Fake - Fake Job Posting Prediction](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)
- **Original Paper**: Habiba Kalthoum Habib Baki, "Employment Scam Aegean Dataset" (EMSCAD), University of the Aegean, 2020.

## Download Instructions

### Option 1: Kaggle CLI (Recommended)
```bash
pip install kaggle
kaggle datasets download -d shivamb/real-or-fake-fake-jobposting-prediction -p data/
unzip data/real-or-fake-fake-jobposting-prediction.zip -d data/
```
Make sure your Kaggle API token is configured at `~/.kaggle/kaggle.json`.

### Option 2: Manual Download
1. Go to https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction
2. Click "Download" (requires Kaggle account)
3. Extract the ZIP file
4. Place `fake_job_postings.csv` in this `data/` folder

## Dataset Description
- **Rows**: 17,880 job postings
- **Fraudulent**: 866 (≈4.84%) — highly imbalanced
- **Columns**: 18 total (17 features + 1 target `fraudulent`)

### Key Columns
| Column | Type | Description |
|---|---|---|
| `title` | text | Job title |
| `location` | text | Geographic location |
| `department` | text | Department within the company |
| `salary_range` | text | Offered salary range |
| `company_profile` | text | Company description |
| `description` | text | Job description |
| `requirements` | text | Job requirements |
| `benefits` | text | Benefits offered |
| `telecommuting` | binary | 1 if telecommuting allowed |
| `has_company_logo` | binary | 1 if company logo present |
| `has_questions` | binary | 1 if screening questions present |
| `employment_type` | categorical | Full-time, Part-time, Contract, etc. |
| `required_experience` | categorical | Experience level required |
| `required_education` | categorical | Education level required |
| `industry` | categorical | Industry sector |
| `function` | categorical | Job function |
| `fraudulent` | binary (target) | 1 = fraudulent, 0 = real |

## File Expected
The notebook expects `fake_job_postings.csv` in this directory.
