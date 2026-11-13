# Data Directory — C1: English-to-Urdu Neural Machine Translation

## Dataset

| Field | Value |
|---|---|
| **Name** | OPUS-100 (English–Urdu subset) |
| **Hugging Face ID** | `Helsinki-NLP/opus-100`, config `en-ur` |
| **Source** | [https://huggingface.co/datasets/Helsinki-NLP/opus-100](https://huggingface.co/datasets/Helsinki-NLP/opus-100) |
| **License** | See individual OPUS sub-corpora licences |

## Splits

| Split | Raw Pairs | After Cleaning (approx.) |
|---|---|---|
| Train | ≈750,000 | 50k–100k subset used |
| Validation | 2,000 | 2,000 |
| Test | 2,000 | 2,000 |

## Cleaning Pipeline

The following filters are applied sequentially to the training data:

1. **Empty pairs** — Remove rows where either source or target is empty / whitespace-only.
2. **Duplicate pairs** — Remove exact (en, ur) duplicate rows.
3. **Length-ratio filter** — Remove pairs where `max(len_en, len_ur) / min(len_en, len_ur) > 3` (token-level).
4. **Max-length filter** — Remove pairs where either sentence exceeds 30 tokens.
5. **Urdu-script filter** — Remove pairs whose target contains no Urdu/Arabic script characters.

## Files Generated at Runtime

| File | Description |
|---|---|
| `source.model` / `source.vocab` | SentencePiece BPE model for English (≈8k merges) |
| `target.model` / `target.vocab` | SentencePiece BPE model for Urdu (≈8k merges) |

## Reproducibility

All random operations use **seed = 42**.
