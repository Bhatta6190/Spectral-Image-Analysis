# Land Degradation Assessment using Hyperspectral Imagery

## Overview
This project analyzes land degradation in a savanna environment using hyperspectral imagery from the Carnegie Airborne Observatory. It compares conserved (Kruger National Park) and degraded (communal lands) regions in South Africa, leveraging spectral analysis techniques to classify land cover types.

## Dataset
- **Source:** Carnegie Airborne Observatory
- **Coverage:** Kruger National Park (Conserved) & Communal Lands (Degraded)
- **Spectral Range:** 24 bands from visible (394.3 nm) to near-infrared (1044.9 nm)

## Methodology
1. **Preprocessing:**
   - Minimum Noise Fraction (MNF) for dimensionality reduction
   - Pixel Purity Index (PPI) for endmember selection
2. **Classification:**
   - Spectral Angle Mapper (SAM)
   - Linear unmixing for abundance maps
3. **Land Cover Categories:**
   - Photosynthetic Vegetation (PV)
   - Non-photosynthetic Vegetation (NPV)
   - Bare Soil (BS)
   - Shadow (S)
4. **Accuracy Assessment:**
   - Stratified sampling (10 samples per class)
   - Confusion matrix for classification evaluation

## Results
- **Key Findings:**
  - Degraded areas exhibit higher bare soil cover and lower NPV compared to conserved regions.
  - PV distribution is more uniform in the conserved region, while it is clustered along water sources in degraded lands.
  - Classification achieved high accuracy, with PV having the best producer’s accuracy (90%-100%) and NPV facing the most misclassification issues.

### Classified Map
<p align="center">
  <img src="./Conserved-Landuse7-Results/lanuse7_RGB_image.jpg" alt="Conserved Area" width="45%"/>
  <img src="./Degraded-Landuse2-Results/landuse2_RGB_image.jpg" alt="Communal Area" width="46%"/>
  <img src="./Conserved-Landuse7-Results/landuse_7_sam_classification_result.jpg" alt="Conserved Area Classification Result" width="45%"/>
  <img src="./Degraded-Landuse2-Results/landuse2_sam_classification_result.jpg" alt="Conserved Area Classification Result" width="46%"/>
</p>
<p align="center"><strong>Figure:</strong>Top Left) RGB Image of Conserved Area, (Top Right) RGB Image of Degraded Area, (Bottom Left) SAM Classified Conserved Area, (Bottom Right) SAM Classified Degraded Area<br>Classes: Green = PV, Red = NPV, Brown = Bare Soil, White = Shadow, and Black = Unclassified.</p>

#### **Comments:** A simple Spectral Mapping (SAM) algorithm is used to classify the imagery into 4 classes- PV (photosynthetic vegetation), NPV (Non-photosynthetic vegetation), BS (Bare Soil) and Shadow areas (S). The classification results shows that the PV within the reserve were found to be distributed proportionally across the whole area while the PV outside the reserve are accumulated to smaller portion and most of the area is does not contain vegetation. Similarly the bare soil cover (BS) within reserved area is very less while it is comparatively higher in the communal areas. The NPV cover is relatively higher in conserved area compared to the communal area. Such widespread decrease in NPV and increase in Bare soil outside the reserve indicates a change in key landscape and soil properties such as loss of organic matter, which is an indicator of land degradation in such areas. Hence, NPV and bare soil cover can be the good indicators for land degradation in communal areas. *For mor information refer to report `Report_Land_degradation.pdf`*

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

