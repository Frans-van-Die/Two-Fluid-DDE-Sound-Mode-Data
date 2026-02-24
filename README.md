# Scale-Dependent Growth Forecasts in Two-Fluid Dark Energy Models

This repository contains the data used to compute the figures and signal-to-noise forecasts for ArXiv:2602.XX, focussing on scale-dependent growth in two-fluid dark energy models.

## Repository Structure

```
├── GrowthRate/
│   GrowthRate_*.txt
│
├── SNRdata/
│   SNR_*.txt
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

### SNRdata

This folder contains the results of the Fisher Information analysis of a multi-tracer analysis on the scale-dependent bias, with the density and bias of tracer `a` varied and tracer `b` taken unbiased with `n_b = 0.01 h^3/Mpc^3`.

Each file contains columns

```
n_a, b_a, snr_ps, snr_pb 
```

where
- `n_a` — number density of tracer `a`,
- `b_a` — bias of tracer `a`,
- `snr_ps` — signal-to-noise ratio obtained from the galaxy power spectrum only,
- `snr_pb` — signal-to-noise ratio obtained from the combined power spectrum
  and bispectrum analysis.

Example:

```
SNRdata/SNR_2fluidPhantom_z0.5_c2p0.001_c2m0.01.txt
```
The filename encodes the model parameters:
- model type (Phantom or Quintom)
- dark energy sound speeds c+² and c−²
- redshift z
---
