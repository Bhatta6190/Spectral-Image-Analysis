# Target Detection In Hyperspectral Imagery (HSI)

## Objective
This work focuses on detecting targets`(Red panel)` in HSI image, performing analysis in both spectral reflectance space and reduced-dimensional space (PCA space). The outcomes include:

- Work on real HSI data.
- Implementation of various target detection algorithms.
- Generation and usage of a truth mask for cross-checking detections.
- Analysis of detection performance via histograms and ROC curves.

The `python` code for achieving all these tasks is included in the included jupyter notebook `target_detection.ipynb` file. 

---

## Data Included
1. **HSI Data**:
   - `001_0729-1919_rad_GeoRef_THOR_ELM_smoothed 146x84.img`
   - `001_0729-1919_rad_GeoRef_THOR_ELM_smoothed 146x84.hdr`
2. **Red Panel Reflectance**:
   - `Red Felt Refl ASD Reseamp 360 ASCII.txt`
3. **Bad Bands List**:
   - Excluded Bands: `114-123, 143-153, 182-197, 253-280, 320-360`

---

## Steps 

### Truth Mask Generation
1. Use ENVI ROI tool to create truth mask.
2. Use the truth mask in the code to validate detection results.

Note: The truth mask already provided here as `classmap.img`, so this task is optional.

---

### Detection Algorithms
Detection is performed in two spaces:
1. **Spectral Reflectance Space**.
2. **Reduced Dimensional Space** (via PCA or SVD).

#### Detection Methods:
- **Spectral Angle Mapper (SAM)**
- **Matched Filter (MF)**
- **Adaptive Coherence Estimator (ACE)**
- **Constrained Energy Minimization (CEM)** 

For details on these detection methods please refer to the reference mentioned at the end section.

#### Key Tasks:
1. **Spectral Space**:
   - Apply each detection algorithm.
   - Display detection scores as:
     - Histograms (with target scores identified).
     - ROC curves (linear and log scales).

2. **Reduced Dimensional Space**:
   - Perform PCA or SVD for dimensionality reduction.
   - Apply detection algorithms on the reduced data cube.
   - Display detection scores as:
     - Histograms (with target scores identified).
     - ROC curves (linear and log scales).

---

## Results

### Final Plots:
1. **Spectral Reflectance Space**:
   - ROC curves for all detectors.

2. **Reduced Dimensional Space**:
   - ROC curves for all detectors.


### Analysis:
- Comparison of detector performance in spectral and reduced space.
- Assessment of the impact of the truth mask on detection results.
- Evaluation of the effectiveness of dimensionality reduction in target localization.

---

**Note:** The Analysis report-`DetectionAnalysisReport.pdf` can be referenced for reviewing quick summary of the work.

## Acknowledgement
Special thanks to **Dr. Emmett Ientilucci** (https://www.rit.edu/science/directory/ejipci-emmett-ientilucci) for providing resources and data for this work.

## References
For further insights on detection algorithms:
- Manolakis, D. SPIE and IEEE papers on HSI detection algorithms.

