![Banner](supernova_banner.png)
<div align="center">
  
# 🔭 Supernova Classification using Machine Learning
  
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/hafsani3hi13/supernova-light-curves-ml-classification?style=social)](https://github.com/hafsani3hi13/supernova-light-curves-ml-classification)
[![GitHub forks](https://img.shields.io/github/forks/hafsani3hi13/supernova-light-curves-ml-classification?style=social)](https://github.com/hafsani3hi13/supernova-light-curves-ml-classification)

### *Mathematical Forensics of Stellar Violence*
### AURA Research Project @ CASSA, Independent University Bangladesh

![Banner](supernova_banner.png)

</div>
# Supernova Classification using Machine Learning

**Author:** Nublat Hafsa
**Student ID:** 2411703
**Date:** 2026-02-21

## Project Overview
This pipeline classifies supernovae (Type Ia, II, Ibc) using light curve characteristics.

## Results
- Random Forest Accuracy: 98.8%
- SVM Accuracy: 96.5%

## Files
- supernova_features.csv - Dataset
- random_forest_supernova.pkl - Random Forest model
- svm_supernova.pkl - SVM model
- feature_scaler.pkl - Scaler
- supernova_forensics.png - Plot 1
- confusion_matrices.png - Plot 2

## Quick Start
```python
import joblib
import numpy as np

model = joblib.load('random_forest_supernova.pkl')
scaler = joblib.load('feature_scaler.pkl')

new_supernova = np.array([[18, 0.8, -19.3, 40, 0.2]])
normalized = scaler.transform(new_supernova)
prediction = model.predict(normalized)
print(f"Type: {prediction[0]}")
