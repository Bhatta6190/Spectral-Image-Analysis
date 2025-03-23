# Foliar Biochemistry Modeling using Non-Invasive Hyperspectral Methods

## Overview  
This study explores the use of **hyperspectral data** for estimating **Nitrogen (N)** and **Potassium (K)** concentrations in crop foliage using a **stepwise linear regression model**. We evaluate different spectral preprocessing techniques:  
- **Raw Spectra**  
- **First Derivative Spectra**  
- **Continuum-Removed Spectra**  

The study aims to determine the most effective spectral transformation and key predictive wavelengths for foliar nutrient estimation.

## Methodology  
- **Dataset:** 92 crop samples with spectral data from **350 nm to 2500 nm** at 1 nm resolution.  
- **Preprocessing Techniques:** Raw reflectance, first derivative, and continuum removal.  
- **Regression Approach:** Stepwise linear regression with varying alpha-to-enter thresholds (**0.005, 0.01, and 0.05**).  
- **Key Evaluation Metrics:** Adjusted \(R^2\), Standard Error (S), and 5-fold Cross-Validation \(R^2\).  

## Results  
- **First Derivative Spectra** achieved the highest accuracy at **α = 0.01**, with adjusted \(R^2 = 96.09\%\) for **N** and \(R^2 = 64.75\%\) for **K**.  
- **Continuum-Removed Spectra** performed well for **N estimation**, with an adjusted \(R^2 = 78.18\%\) at **α = 0.05**.  
- **Raw Spectra** yielded lower accuracy but still captured key nutrient-sensitive spectral regions.  
- The most informative spectral bands were in the **UV (360–450 nm), Red-Edge (600–750 nm), NIR (800–1300 nm), and SWIR (1900–2500 nm)** regions.

## Key Figures  

<p align="center">
  <img src="./Results/sample1_spectrum.png" alt="Raw Spectrum Sample" width="30%"/>
  <img src="./Results/Sample1_firstderivative.png" alt="First Derivative Spectrum" width="30%"/>
  <img src="./Results/Sample1_continuumremoved.png" alt="Continuum Removed Spectrum" width="30%"/>
</p>

<p align="center">
  <img src="./Results/regression_outcome.png" alt="Regression Performance Comparison" width="98%"/>
</p>

<p align="center"><strong>Figure:</strong> Top) Raw spectrum (left), First derivative transformation (center), and Continuum removal (right).  
Bottom) Regression model performance comparison.</p>

## Conclusion  
This study highlights the **importance of spectral preprocessing** for improving foliar nutrient estimation. The **first derivative transformation** emerged as the most effective, enhancing subtle spectral variations critical for **N and K prediction**. The findings reinforce the **potential of hyperspectral data** for precision agriculture and non-invasive nutrient monitoring. Future work will focus on field-based hyperspectral imaging and advanced modeling techniques.
  
This work has been done on [Minitab](https://www.minitab.com/en-us/) statistical software. All the description and results are included in documentation file `Foliar_Biochemistry.pdf`

### Acknowledgments
Special thanks to [Dr. Jan van Aardt](https://www.rit.edu/directory/jvacis-jan-van-aardt) for providing guidance and resources for this work.
