# Wavenumber to Wavelength Conversion

In Spectral Analysis, the conversion from "Spectral Radiance in Wavenumber [W/cm2 sr cm-1]" to "Spectral Radiance in Wavelength domain [W/m2 sr μm]" cannot be just done by converting the wavenumber to wavelength by using the reciprocal relation. 

The total energy must be preserved while converting to the different domains as shown by relation below:
![image](https://github.com/Bhatta6190/Spectral-Image-Analysis/assets/112892693/b8433087-18ab-4687-8842-5fc7032e6e74)

where right left side expression shows the integration in wavenumber domain and right hand side is in wavelngth domain. This example shows the conversion of radiances in WN domain to WL domain. The problem sheet, data are uploaded and also the steps for the conversion are shown in the uploaded jupyter notebook file.


Special thanks to **Dr. Emmett Ientilucci**(https://www.rit.edu/science/directory/ejipci-emmett-ientilucci) for providing resources and data for this work.