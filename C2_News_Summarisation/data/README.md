# Data Directory — C2: Abstractive Summarisation of BBC News Articles

## Dataset: XSum (Extreme Summarisation)

- **Source:** Hugging Face — `EdinburghNLP/xsum`
- **Paper:** Narayan, Cohen & Lapata (2018), *"Don't Give Me the Details, Just the Summary! Topic-Aware Convolutional Neural Networks for Extreme Summarization"*
- **Full size:** 226,711 BBC articles with one-sentence summaries
  - Train: 204,045
  - Validation: 11,332
  - Test: 11,334

## Subsets Used (seed=42)

| Split      | Original Size | Sampled Size |
|------------|---------------|--------------|
| Train      | 204,045       | 20,000       |
| Validation | 11,332        | 1,000        |
| Test       | 11,334        | 1,000        |

## Download

Data is downloaded automatically via the `datasets` library from Hugging Face.
No manual download is required.

```python
from datasets import load_dataset
dataset = load_dataset("EdinburghNLP/xsum")
```

## Fields

| Field      | Description                              |
|------------|------------------------------------------|
| `document` | Full BBC news article text               |
| `summary`  | One-sentence gold-standard summary       |
| `id`       | Unique article identifier                |

## Notes

- Articles span multiple BBC domains: Politics, Business, Sport, Tech, Health, Entertainment, Education, Science, etc.
- Summaries are **introductory sentences** written by journalists — they are highly abstractive and often contain information that requires understanding the full article.
- This makes XSum particularly challenging for extractive baselines like Lead-1.
