# Dry Bean Dataset

## Source
- **UCI Machine Learning Repository**: Dataset ID 602
- **Original Paper**: Koklu, M. and Ozkan, I.A., 2020. Multiclass classification of dry beans using computer vision and machine learning techniques. *Computers and Electronics in Agriculture*, 174, 105507.
- **DOI**: https://doi.org/10.24432/C50S4B

## Description
Images of 13,611 grains of 7 different registered dry bean varieties were captured with a high-resolution camera. A total of 16 features (12 dimension + 4 shape form) were extracted from each grain image after segmentation and feature-extraction stages.

## Features (16 numeric)
| # | Feature | Description |
|---|---------|-------------|
| 1 | Area | Area of the bean zone (pixels) |
| 2 | Perimeter | Circumference of the bean (pixels) |
| 3 | MajorAxisLength | Longest line distance through the bean |
| 4 | MinorAxisLength | Shortest line distance through the bean |
| 5 | AspectRatio | MajorAxisLength / MinorAxisLength |
| 6 | Eccentricity | Eccentricity of the ellipse having same moments |
| 7 | ConvexArea | Pixel count of the smallest convex polygon enclosing the bean |
| 8 | EquivDiameter | Diameter of a circle with the same area |
| 9 | Extent | Ratio of bean area to bounding rectangle area |
| 10 | Solidity | Area / ConvexArea |
| 11 | Roundness | 4πArea / Perimeter² |
| 12 | Compactness | EquivDiameter / MajorAxisLength |
| 13 | ShapeFactor1 | MajorAxisLength / Area |
| 14 | ShapeFactor2 | MinorAxisLength / Area |
| 15 | ShapeFactor3 | Area / (MajorAxisLength/2)² π |
| 16 | ShapeFactor4 | Area / (MinorAxisLength/2)² π |

## Target Classes (7 varieties)
| Class | Count |
|-------|-------|
| DERMASON | 3,546 |
| SIRA | 2,636 |
| SEKER | 2,027 |
| HOROZ | 1,928 |
| CALI | 1,630 |
| BARBUNYA | 1,322 |
| BOMBAY | 522 |

**Total samples**: 13,611

## Usage
```python
from ucimlrepo import fetch_ucirepo
beans = fetch_ucirepo(id=602)
X = beans.data.features
y = beans.data.targets
```

## License
This dataset is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.
