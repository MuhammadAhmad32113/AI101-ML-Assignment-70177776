# Flickr8k Dataset — Download Instructions

## Dataset Overview
- **Source**: [Flickr8k on Kaggle](https://www.kaggle.com/datasets/adityajn105/flickr8k)
- **Contents**: 8,091 images × 5 captions each = 40,455 captions
- **License**: Research use only

## Option 1: Kaggle API (Recommended for Colab)

```bash
# Install Kaggle CLI (if not already installed)
pip install -q kaggle

# Set up credentials — upload your kaggle.json or set env vars
# mkdir -p ~/.kaggle && cp kaggle.json ~/.kaggle/ && chmod 600 ~/.kaggle/kaggle.json

# Download and unzip
kaggle datasets download -d adityajn105/flickr8k -p data/ --unzip
```

## Option 2: Manual Download

1. Go to https://www.kaggle.com/datasets/adityajn105/flickr8k
2. Click **Download** (≈1.1 GB zip)
3. Extract into the `data/` folder

## Expected Directory Structure

After extraction the layout should be:

```
data/
├── Images/          # 8,091 JPEG files
│   ├── 1000268201_693b08cb0e.jpg
│   ├── 1001773457_577c3a7d70.jpg
│   └── ...
├── captions.txt     # TSV: image | caption
└── README.md        # This file
```

## Captions Format

`captions.txt` is a pipe/comma-delimited file with columns:
- `image` — filename of the image (e.g., `1000268201_693b08cb0e.jpg`)
- `caption` — one English caption

Each image has exactly 5 captions.
