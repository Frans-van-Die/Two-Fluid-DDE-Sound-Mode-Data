# Scale-Dependent Growth Forecasts in Two-Fluid Dark Energy Models

This repository contains the data used to compute the figures and signal-to-noise forecasts for ArXiv:2602.XX, focussing on scale-dependent growth in two-fluid dark energy models.

## Repository Structure

```
├── GrowthRate/
│   GrowthRate_*.txt
│
├── SUdata/
│   SUcollapse_*.txt
```

### GrowthRate

This folder contains files with the **scale-dependent linear growth factor** D(z, k)

Each file contains columns

```
k, D(z=0), D(z=0.1), D(z=0.2), D(z=0.35), D(z=0.5), D(z=0.75), D(z=1), D(z=1.25), D(z=1.5), D(z=2)
```

Example file:

```
GrowthRate/GrowthRate_2fluidPhantom_c2p0.001_c2m0.01.txt
```

The filename encodes the model parameters:
- model type (Phantom or Quintom)
- dark energy sound speeds c+² and c−²

---

### SUdata

This folder contains results from **separate-universe collapse calculations** used to compute the scale-dependent bias response.

Each file contains columns

```
k, f(k)
```

The function `f(k)` describes the response of the spherical collapse threshold to a long-wavelength matter perturbation. More precisely, it is defined as:

```
f(k) = ∂δ_c(z,k) / ∂δ_m(z,k)
```

Example:

```
SUdata/SUcollapse_2fluidPhantom_z0.5_c2p0.001_c2m0.01.txt
```
The filename encodes the model parameters:
- model type (Phantom or Quintom)
- dark energy sound speeds c+² and c−²
- redshift z
---
