# Breast Cancer Wisconsin (Diagnostic) Dataset

## Source
This dataset is built into scikit-learn and can be loaded directly:

```python
from sklearn.datasets import load_breast_cancer
data = load_breast_cancer()
X, y = data.data, data.target
```

## Description
- **Samples**: 569
- **Features**: 30 numeric features computed from digitized images of fine needle aspirate (FNA) of breast masses
- **Target**: Binary classification
  - `0` = Malignant (212 samples)
  - `1` = Benign (357 samples)

## Features
Ten real-valued features are computed for each cell nucleus:
1. Radius (mean of distances from center to points on the perimeter)
2. Texture (standard deviation of gray-scale values)
3. Perimeter
4. Area
5. Smoothness (local variation in radius lengths)
6. Compactness (perimeter² / area − 1.0)
7. Concavity (severity of concave portions of the contour)
8. Concave points (number of concave portions of the contour)
9. Symmetry
10. Fractal dimension ("coastline approximation" − 1)

For each of the 10 features, the mean, standard error (SE), and "worst" (mean of the three largest values) are reported, giving 30 features total.

## Original Source
- UCI Machine Learning Repository: [Breast Cancer Wisconsin (Diagnostic)](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- Creators: Dr. William H. Wolberg, W. Nick Street, Olvi L. Mangasarian
- Donor: Nick Street

## Citation
Street, W.N., Wolberg, W.H., & Mangasarian, O.L. (1993). Nuclear feature extraction for breast tumor diagnosis. *IS&T/SPIE 1993 International Symposium on Electronic Imaging: Science and Technology*, 1905, 861-870.

## No Download Required
Since this dataset ships with scikit-learn, no manual download is necessary. Simply run the notebook and the data will be loaded automatically.
