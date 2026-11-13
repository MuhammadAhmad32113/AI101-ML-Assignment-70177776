# Dataset: Concrete Compressive Strength

## Source
- **UCI Machine Learning Repository** – Dataset ID 165
- **Original Donor**: Prof. I-Cheng Yeh, Department of Information Management, Chung-Hua University, Taiwan
- **Paper**: Yeh, I-C. (1998). "Modeling of strength of high-performance concrete using artificial neural networks." *Cement and Concrete Research*, 28(12), 1797–1808.

## Description
The dataset contains **1,030 samples** of concrete mixtures with **8 numeric input features** and **1 continuous target** (compressive strength in MPa).

## Features (Inputs)
| # | Feature | Unit | Description |
|---|---------|------|-------------|
| 1 | Cement | kg/m³ | Portland cement content |
| 2 | Blast Furnace Slag | kg/m³ | Ground granulated blast-furnace slag |
| 3 | Fly Ash | kg/m³ | Fly ash content |
| 4 | Water | kg/m³ | Water content |
| 5 | Superplasticizer | kg/m³ | High-range water reducer |
| 6 | Coarse Aggregate | kg/m³ | Coarse aggregate content |
| 7 | Fine Aggregate | kg/m³ | Fine aggregate content |
| 8 | Age | days | Age of concrete (1–365 days) |

## Target (Output)
| Feature | Unit | Range (approx.) |
|---------|------|-----------------|
| Concrete Compressive Strength | MPa | 2–83 |

## Loading the Dataset
```python
from ucimlrepo import fetch_ucirepo
concrete = fetch_ucirepo(id=165)
X = concrete.data.features
y = concrete.data.targets
```

## Key Characteristics
- **No missing values**
- All features are continuous / numeric
- The `Age` feature is heavily right-skewed (most samples are ≤ 28 days, but some go to 365)
- The water-to-cement ratio (`Water / Cement`) is a well-known domain predictor of strength (Abram's law)

## Citation
Yeh, I-C. (1998). UCI Machine Learning Repository. https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength
