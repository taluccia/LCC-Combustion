# LCC-Combustion

## 1   Overview


Goals of this analysis
1. Update Combustion model with additional field sites for training

The original combustion Model was published here

citation needed

## 2   Updates

The majors updates include the following
- Integration of additional field sites
- Updating the data source for the Fire Weather Index variables from GFWED to Copernicus
- Updating the Digital Elevation Model Source to the FABDEM (30 m) resolution

## 3   ROI

The original model included field sites from ...

Insert Map

The new model has field sites from ...

Insert Map

## X   Data sets

FiSL n=311
LC n=555
Original Data n = 1011

## X   Notes

| TWI Value    | Interpretation                    | Landscape Feature Examples           |
| ------------ | --------------------------------- | ------------------------------------ |
| **0 – 5**    | Very well-drained, steep slopes   | Ridges, upper slopes                 |
| **5 – 10**   | Moderately well-drained           | Midslopes, footslopes                |
| **10 – 15**  | Moderately to poorly drained      | Lower slopes, gentle terrain         |
| **15 – 20+** | Poorly drained, high accumulation | Valleys, depressions, riparian zones |

Note: TWI is unitless and the absolute range depends on the DEM resolution and hydrological conditioning (e.g., sink filling).

| Variable (after scaling) | Typical unit            | Plausible range (global)                                            | Notes                                                                                   |
| ------------------------ | ----------------------- | ------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **bdod**                 | g cm⁻³                  | **0.3 – 1.9** (rarely 0.1–2.2)                                      | Bulk density of fine earth. Your factor `×0.01` to convert from stored units is common. |
| **cec**                  | cmol(+) kg⁻¹            | **0 – 80** (can reach 100–150 in some clays/organics)               | Very sandy soils often <10; heavy clays/andisols higher.                                |
| **cfvo**                 | vol %                   | **0 – 60** (stony areas can be >60)                                 | Coarse fragments volume %.                                                              |
| **clay**                 | %                       | **0 – 60** (rarely to 80)                                           | Must lie within 0–100 and clay+silt+sand ≈ 100.                                         |
| **silt**                 | %                       | **0 – 80**                                                          | 0–100 bounds; check texture closure.                                                    |
| **sand**                 | %                       | **10 – 90** (0–100 is possible)                                     | Texture closure check as above.                                                         |
| **nitrogen**             | % (or g kg⁻¹; see note) | **0 – 0.5 %** typical (0–5 g kg⁻¹), **peat up to \~1 %**            | You used factor `×0.01`. If you interpret as %, typical mineral soils are very low.     |
| **phh2o**                | pH units                | **3.5 – 8.5** (absolute 0–14)                                       | Your factor `×0.1` gives standard pH.                                                   |
| **soc**                  | g kg⁻¹ (or %)           | **0 – 150 g kg⁻¹** (0–15 %) typical; peats can be 400 g kg⁻¹ (40 %) | Your factor `×0.1` often yields g kg⁻¹.                                                 |
| **ocd**                  | t ha⁻¹                  | **0 – 300 t ha⁻¹** (0–30 cm) common; peat/organic >500              | Your factor `×0.1` is typical for SoilGrids OCD.                                        |



## 5   TCT
https://bleutner.github.io/RStoolbox/reference/tasseledCap.html
## 4   Citaitions


Gruber, S., & Peckham, S. (2009). Land-surface parameters and objects in hydrology. In Hengl & Reuter, Geomorphometry: Concepts, Software, Applications.
