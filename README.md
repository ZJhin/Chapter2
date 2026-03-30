# Chapter 2 — Southern Ocean & Sea-Ice Diagnostics (CMIP6)

This repository contains three Jupyter notebooks that analyze **Southern Ocean climate dynamics** using CMIP6 model output.  
The workflow focuses on links between:

- atmospheric forcing (wind),
- sea-ice motion and mass redistribution,
- upper-ocean temperature structure,
- and water-mass transformation.

Most analyses target the historical period around **1979–2014** and Southern Ocean latitudes south of about **45°S**.

## Notebook summary

## 1) `2_load_and_show.ipynb`
A comprehensive analysis and plotting notebook that:

- loads preprocessed multi-model diagnostics,
- defines shared utility functions (coordinate detection, correlations, plotting, transformations),
- compares model behavior for sea-ice freeze/melt/redistribution,
- evaluates sea-ice and wind-vector relationships,
- investigates density structure and density-gradient metrics,
- computes and aligns water-mass-transformation (WMT) curves,
- and builds multi-panel summary figures across models.

In short: this is the main synthesis notebook tying dynamic and thermodynamic sea-ice processes to density-space diagnostics.

## 2) `wind_speed.ipynb`
A processing + diagnostic notebook centered on velocity fields. It includes:

- functions to derive wind, sea-ice, and ocean speed from vector components,
- model-by-model loading and preprocessing,
- polar plotting of wind and sea-ice velocity,
- comparisons of sea-ice speed as a fraction of wind speed,
- and area/extent-based wind statistics within sea-ice-covered regions.

In short: this notebook quantifies momentum-related forcing and response in the sea-ice zone.

## 3) `temperature_profile.ipynb`
A profile-focused notebook that explores ocean thermal structure and its sea-ice links:

- extracts `thetao` profiles (e.g., 200 m and 500 m depth ranges) south of 45°S,
- computes model mean meridional/depth thermal structures,
- includes `hfds` (surface heat flux) diagnostics,
- examines relationships among temperature, heat flux, and sea-ice mass,
- and performs inter-model correlation-style profile analysis.

In short: this notebook connects subsurface temperature and heat-flux variability to sea-ice state across CMIP6 models.

## Common workflow characteristics

Across notebooks, the project generally uses:

- `xarray`, `numpy`, `pandas`, `matplotlib`, `cartopy`, `xesmf`, and `intake`,
- CMIP6 catalog/query workflows plus locally saved intermediate NetCDF results,
- multi-model intercomparison with grouped/ensemble plotting,
- Southern Ocean masking/regridding and weighted averaging techniques.

## Overall subject summary

This chapter studies how **Southern Ocean sea ice is controlled by both thermodynamics and dynamics**:

- Thermodynamics: freezing/melting, density changes, and surface heat flux.
- Dynamics: wind forcing, sea-ice drift, and transport/redistribution.
- Ocean context: upper-ocean temperature profiles and water-mass transformation in density space.

The combined objective is to diagnose **why models differ in Antarctic sea-ice behavior** and to identify physically consistent relationships between atmosphere, ice, and ocean fields.
