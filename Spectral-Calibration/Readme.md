# Ocean Optics Spectrometer Calibration  

## Objective  
The purpose of this work is to calibrate the Ocean Optics Spectrometer using HgNe and Ar pencil lamps. These lamps produce spectra with distinct lines at specific wavelengths.  

By utilizing these known wavelength values, we aim to:  
1. Establish a model that maps pixel numbers to wavelength values.  
2. Compare the obtained calibration model with the factory-provided calibration.  

The step-by-step procedure, including Python code and results, is presented in the `spectral_calibration.ipynb` python notebook.  

## Overview  
The `python` code includes:  
- Data preprocessing and pixel-intensity analysis.  
- Gaussian fitting to identify peak positions.  
- Polynomial models (linear, 3rd, 4th, 5th degree) for pixel-to-wavelength mapping.  
- Comparison of predicted wavelengths with factory calibration.  
- Visualizations to assess calibration accuracy.  

## Steps  
1. Process spectral data to identify peak pixel values.  
2. Fit polynomial models and calculate residuals.  
3. Compare predicted wavelengths with factory-calibrated values

Special thanks to **Dr. Anthony Vodacek**(https://www.rit.edu/science/directory/axvpci-anthony-vodacek) for providing resources and data for this work.