
# Spectral Image Analysis

## Overview
In this work we analyzed spectral radiance components and their applications in determining ground-leaving radiance, camouflage detection, and gas plume identification. Tasks involved deriving equations, performing numerical computations, and plotting results. All the tasks are done step-by-step using and available in `rem-sen-spec-rad.ipynb` python notebook code.

---

## Task 1: Ground-Leaving Radiance
- **Goal**: Compute reflected and emitted spectral radiance for VNIR/SWIR (0–2.5 μm), MWIR (3–5 μm), and LWIR (8–14 μm) ranges.
- **Deliverables**:
  - Derived equations for spectral radiance using Lambertian reflectance.
  - Plotted radiance components for varying reflectance, temperature, and solar zenith angles.
- **Results**: Showed spectral dominance of reflectance vs. emission across wavelengths.

---

## Task 2: Camouflage Detection
- **Goal**: Analyze spectral radiance of a camouflaged target vs. a coniferous canopy in VNIR/SWIR.
- **Deliverables**:
  - Derived radiance equations considering solar zenith angle and reflectance.
  - Plotted target/background radiances and differences.
  - Identified key spectral regions for camouflage detection.
- **Results**: Highlighted spectral features enhancing target-background separability.

---

## Task 3: Propane Gas Discrimination
- **Goal**: Analyze spectral radiance differences due to a propane gas plume in LWIR (8–12 μm).
- **Deliverables**:
  - Derived equations for plume and background radiance.
  - Plotted radiances and differences for various plume temperatures.
  - Identified propane absorption features for detection.
- **Results**: Showed conditions where propane is spectrally distinct.

---

## Tools & Methods
- **Programming**: Python/Matlab (NumPy, Matplotlib, SciPy).
- **Concepts**: Radiative transfer, Lambertian reflectance, blackbody radiation.
- **Outputs**: Plots in [uW/cm²·sr·μm].

---

## Summary
- Demonstrated spectral radiance analysis for vegetation and gas detection.
- Provided insights into reflectance, temperature, and spectral feature impacts.

**Note:** The derived expression used are uploaded in `Derived_expressions` directory.

Special thanks to **Dr. Emmett Ientilucci**(https://www.rit.edu/science/directory/ejipci-emmett-ientilucci) for providing resources and data for this work.

