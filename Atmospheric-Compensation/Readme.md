
# Atmospheric Compensation with the Empirical Line Method (ELM)

## Background: Empirical Line Method (ELM)
The ground-leaving spectral signatures in hyperspectral imagery (HSI) are altered by atmospheric effects like absorption and scattering. Atmospheric compensation aims to minimize these effects, enabling accurate ground reflectance retrieval.

The **Empirical Line Method (ELM)** compensates for these atmospheric effects using known reflectance and radiance pairs (calibration panels). The relationship between sensor-reaching radiance $\ L \$ and ground reflectance $\ rho \$ is modeled as:

$\ L = a \cdot \rho + b \$

Where:
- $\ a \$: Gain (direct solar and downwelling radiance)
- $\ b \$: Offset (path radiance due to atmospheric scattering)

By assuming Lambertian targets and space-invariant illumination, the gain and offset are derived through linear regression using dark and white panel data:

$\
a = \frac{L_2 - L_1}{\rho_2 - \rho_1}, \quad b = L_1 - a \cdot \rho_1
\$

This regression is applied on a band-by-band basis, enabling the transformation of radiance data to reflectance data for the entire scene.

---

## Data Overview

### Files Provided
1. **HSI Radiance Image**:
   - `2017-08-01_14-28-56_000011__061158-066258_radiance_fwd_proj_subset.bin`
   - Dimensions: $\ 340 \times 234 \times 372 \$ (40 cm GSD)

2. **High-Resolution RGB Image**:
   - `2017-08-01_14-33-23_000160_FT010007_subset.jp2`
   - Dimensions: $\ 2555 \times 1906 \times 3 \$ (3 cm GSD)

3. **Calibration Panel Spectra**:
   - `Spectra_8_01_2017.xlsx`
   - Includes dark, white, red, and blue panel reflectances.

### Scene Description
- **Calibration Panels**: Dark and white panels
- **Colored Panels**: Red and blue panels
- **Vegetation and Other Objects**: Around the RIT campus

---

## Lab Workflow

### Objectives
1. Perform atmospheric compensation using ELM.
2. Generate a new hyperspectral data cube in reflectance units.
3. Analyze gain and bias terms and validate reflectance retrievals.

### Steps
1. **Read and Preprocess Data**:
   - Load the HSI and calibration panel data.
   - Extract regions of interest (ROI) for calibration panels.

2. **Compute Gain and Bias**:
   - Calculate $\ a \$ and $\ b \$ for each wavelength:
     $\
     a = \frac{L_2 - L_1}{\rho_2 - \rho_1}, \quad b = L_1 - a \cdot \rho_1
     \$
   - Apply the regression model to convert radiance to reflectance.

3. **Generate Reflectance Data Cube**:
   - Use $\ a \$ and $\ b \$ to transform the radiance data cube to reflectance.

4. **Validation and Analysis**:
   - Plot gain and bias curves.
   - Cross-check retrievals for calibration panels and vegetation spectra.
   - Compare results with color panels (red and blue).

5. **Alternative Method (No Dark Panel)**:
   - Use dark point selection (e.g., lowest valid radiance per wavelength).
   - Analyze the impact on the compensated data.

---

## Results

### Gain and Bias Analysis
- **Gain**: Exhibits solar spectrum features, indicating atmospheric homogeneity.
- **Bias**: Higher at shorter wavelengths due to Rayleigh scattering.

### Reflectance Retrieval
- **Calibration Panels**: Retrieved reflectance matches expected values.
- **Vegetation Spectra**: Reflectance shows accurate spectral shapes.
- **Alternative Dark Point Selection**: Reflectance is consistent, with minor shifts due to bias differences.

### General Assumptions
1. Calibration panels are Lambertian (BRDF is angle-independent).
2. Illumination is space-invariant.
3. Atmosphere is homogeneous across the scene.

---

## Usage Notes
- Carefully select ROIs for calibration panels to reduce noise effects.
- Validate the retrieved reflectance with reference spectra.
- Dark point selection requires careful handling to avoid introducing artifacts.

---

This README provides an overview of the Empirical Line Method (ELM) implementation for atmospheric compensation of hyperspectral imagery collected at RIT. The process generates a new HSI cube in reflectance units, ensuring accurate ground reflectance retrieval.
