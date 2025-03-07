# Spectral-Image-Analysis

This repository hosts tools and resources for analyzing remotely sensed spectral data including `Multispectral` and `Hyperspectral` data, covering multiple tasks- from simple `wavenumber-to-wavelength` domain conversion to complex tasks such as `Noise Reduction`, `Target Detection`, `Classification` and so on. Each directory focuses on a specific task of spectral data processing and analysis and includes all necessary resources.

### Current Resources:
- **`Wavenumber-to-Wavelength domain conversion`**: Tools for conversion from "Spectral Radiance in Wavenumber [W/cm2 sr cm-1]" to "Spectral Radiance in Wavelength domain [W/m2 sr μm]"

- **`Spectral-Calibration`**: Tools for calibrating a Spectrometer using pencil lamps.

- **`Remotely-Sensed-Spectral-Radiance`**: Tools for analysis of spectral radiance components and their applications in determining ground-leaving radiance, camouflage detection, and gas plume identification.

- **`PCA-NAPCA-Noise-Removal`**: Tools for removing noise from multispectral imagery using `Principal Component Analysis (PCA)` and `Noise Adjusted Principal Component Analysis (NAPC)` techniques.

- **`Atmospheric-Compensation`**: Tools for performing atmospheric compensation in `Hyperspectral` imagery using `Empirical Line Method (ELM)` and generate redlectance data product.

- **`Hyperspectral-Target-Detection`**: Tools for detecting targets`(Red panel)` in `Hyperspectral` image and performing analysis in both spectral reflectance space and reduced-dimensional space (PCA space).

- **`Species-Level-Classification-using-HSI-ENVI`**: A report on using `Hyperspectral Imagery` to classify forest species using `Maximum Likelihood Estimation (MLE)` algorithm. 

- **`Land-Degradation-Assessment-using-HSI-ENVI`**: A report on using `Hyperspectral Imagery` to assess the status of land degradation using `Pixel Unmixing` and `Spectral Angle Mapper (SAM)` classification algorithm. 


**Note:** The `ENVI` keyword label at the end of directory name indicates that the work has been done using **ENVI Application** and only analysis reports and results are available.

We welcome suggestions to improve the repository.  

**Contact**: [rb1005@rit.edu](mailto:rb1005@rit.edu) for potential collaborations.

