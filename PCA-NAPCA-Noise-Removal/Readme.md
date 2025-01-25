# Multispectral Data Analysis: PCA & NAPC for Noise Removal

This project leverages **Principal Component Analysis (PCA)** and **Noise Adjusted Principal Component Analysis (NAPC)** to remove noise from multispectral imagery. The dataset used in this lab consists of a **16-band multispectral image** of the **Lake Ontario Shoreline** located in **Rochester, NY**, captured using the **Modular Imaging Spectrometer Instrument (MISI)** through airborne means. The image spans the **NIR range (730 nm to 985 nm)**.

The primary objective is to clean the noisy image by using these advanced dimensionality reduction techniques to enhance the quality of the data.

## Objectives

- Apply **PCA** to the MISI data, compare before/after results, and analyze variances, covariances, and eigenvalues.
- Implement **NAPC** with noise data, compare it to PCA, and evaluate how it improves noise reduction.
- Investigate noise reduction by eliminating noisy bands in transformed spaces (both PCA and NAPC).

## Methodology

1. **PCA Transformation**:
   - Perform PCA on the MISI dataset.
   - Report variances, covariances, and eigenvalues.
   - Analyze decorrelation of noise in transformed bands.
   - Eliminate noisy bands and evaluate the results.
   
2. **NAPC Transformation**:
   - Implement NAPC using MISI and noise data.
   - Compare results to PCA and analyze noise reduction effectiveness.
   - Report variances, covariances, and eigenvalues for NAPC.
   - Evaluate decorrelation of noise and remove noisy bands.

## Results

- **PCA vs. NAPC**: NAPC outperforms PCA in terms of noise reduction, with a clearer separation of noise and signal.
- **Noise Reduction**: Fewer bands need to be eliminated in the NAPC space for effective noise reduction.
- **Variance & Covariance**: NAPC shows better decorrelation compared to PCA, demonstrating its effectiveness in handling noise.

Special thanks to **Dr. Emmett Ientilucci**(https://www.rit.edu/science/directory/ejipci-emmett-ientilucci) for providing resources and data for this work.
The original work can be referred from: 
   - @inproceedings{Ientilucci2003ComparisonAU,
   title={Comparison and Usage of Principal Component Analysis ( PCA ) and Noise Adjusted Principal Component ( NAPC ) Analysis or Maximum Noise Fraction ( MNF )},
   author={Emmett Ientilucci},
   year={2003},
   url={https://api.semanticscholar.org/CorpusID:53370643}
   }