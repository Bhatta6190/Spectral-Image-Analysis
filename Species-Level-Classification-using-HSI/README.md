# Forest Species Classification using HSI

### Overview
Tree species classification is crucial for ecological studies and sustainable forest management. This project explores **Hyperspectral Imaging (HSI)** data from the **Compact Airborne Spectrographic Imager (CASI)**, which captures spectral responses in 36 bands. The classification is performed using **Maximum Likelihood Estimation (MLE)** and **Spectral Angle Mapper (SAM)** to evaluate their performance on raw and transformed data.

### Dataset
- **Classes:**
  - `Eucalyptus grandis (Gran)`
  - `Eucalyptus dunnii (Dun)`
  - `Eucalyptus grandis x nitens (GraNit)`
  - `Acacia mearnsii (Amea)`
  - `OtherTree`
  - `Bare Soil (BS)`
- **Data Source:** Hyperspectral airborne imagery
- **Method:** Minimum Noise Fraction (MNF) transformation for dimensionality reduction

### Workflow
```
1. Preprocess raw hyperspectral data (radiometric and geometric corrections)
2. Apply MNF transformation to reduce data dimensionality
3. Train classifiers (MLE, SAM) on both raw and MNF-transformed bands
4. Evaluate classification accuracy using standard metrics
```

### Acknowledgments
Special thanks to [Dr. Jan van Aardt](https://www.rit.edu/directory/jvacis-jan-van-aardt) for providing guidance and resources for this work.
