# Timing the evolution of local galaxies

This repository includes links to the data and catalogs of physical parameters used in
[the paper by Pacifici, Oh, Oh, Lee, and Yi (2016)](https://ui.adsabs.harvard.edu/abs/2016ApJ...824...45P/abstract).

Notebooks to reproduce some figures will come (when I can find the time...but
feel free to ping me). You can contact me at camilla.pacifici@gmail.com.

Here is the material with some explanations (links point to Dropbox).

## [Photometric catalog](https://www.dropbox.com/scl/fi/hkckoys936ln8s8mjnadl/MIST_phot_v5.dat?rlkey=glhanidmy37ots3x9uen4fm8k&dl=0)

This file can be parsed with `pandas.read_csv`.

It contains:
- ID and position on the sky of the objects (columns `ID`, `RA`, `DEC`),
- spectroscopic redshifts and uncertainties from SDSS (columns `specz`, `especz`),
- AB magnitudes and uncertainties in GALEX filters (columns `FUV`, `eFUV`, `NUV`, `eNUV`),
- AB magnitudes and uncertainties in SDSS filters (columns `u`, `eu`, `g`, `eg`, `r`, `er`, `i`, `ei`, `z`, `ez`),
- AB magnitudes and uncertainties in WISE channel 1 (columns `W1`, `eW1`),
- the magnitude correction for WISE channel 1 (column `dm`),
- the aperture in arcseconds (column `aptarc`),
- a flag (column `flgO`).

## [Catalog of physical parameters](https://www.dropbox.com/scl/fi/2cpt0utjc5pcsfn5ndlxi/mederr_mist_phot_v5.dat?rlkey=r3pz404g3iolbkzx32qa2m04v&dl=0)

This file can be parsed with `pandas.read_csv`.

It contains 50, 16, and 84 percentiles of the probability distribution functions
for the following parameters:
- `logM` logarithm of the stellar mass in solar masses,
- `logSFR` logarithm of the star formation rate in solar masses per year,
- `logSSFR` logarithm of the specific star formation rate in 1/Gyr,
- `logOH` metallicity in units of 12+log(O/H),
- `tauV` optical depth of the dust,
- `logAGE` logarithm of the light-weighted age in years,
- `col1` rest-frame dust-corrected NUV − g color,
- `col2` rest-frame dust-corrected g - i color,
- `logML` logarithm of the mast to light ratio.

## [Catalog of timescales](https://www.dropbox.com/scl/fi/3p1711u1ax36he0gvjxwq/timescales_mist_phot_v5.dat?rlkey=19xoj3zulohqprya2afl4oqfp&dl=0)

This file can be parsed with `pandas.read_csv`.

It contains the parameters derived from the best-estimate star formation histories:
- `t_form` lookback time of first stars formed in Gyr
- `t_10` lookback time at which the galaxy reaches 10% of the total stellar mass formed
- `t_50` lookback time at which the galaxy reaches 50% of the total stellar mass formed
- `t_90` lookback time at which the galaxy reaches 90% of the total stellar mass formed
- `SFR_10` star formation rate in solar masses per year at t_10
- `SFR_50` star formation rate in solar masses per year at t_50
- `SFR_90` star formation rate in solar masses per year at t_90
- `logM_10` logarithm of the stellar mass in solar masses at t_10
- `logM_50` logarithm of the stellar mass in solar masses at t_50
(I now see that it is criminal that I called this quantity the same as the
median of the stellar mass in the previous file...sorry...)
- `logM_90` logarithm of the stellar mass in solar masses at t_90
- `lbtz` lookback time in Gyr at the redshift of observation
- `tq1` lookback time in Gyr at which the galaxy reaches quiescence for the first time
- `tqf` lookback time in Gyr at which the galaxy reaches quiescence for good
- `logM_tq` logarith of the stellar mass in solar masses when the galaxy reaches quiescence
