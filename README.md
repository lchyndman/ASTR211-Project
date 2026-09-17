# ASTR211 Project – Spectral Analysis of the Pi Mensae System

Luke Hyndman

A solo, self-managed observational astronomy project — from observing proposal through data reduction to final report — using the UCMJO McLellan 1m Telescope to characterise the exoplanet host star Pi Mensae and search for atmospheric signatures on its transiting Super-Earth, Pi Mensae c.

## Aim

1. Measure the radial velocity, metallicity, effective temperature, and surface gravity of Pi Mensae (a G-dwarf exoplanet host).
2. Attempt transmission spectroscopy on the transiting Super-Earth Pi Mensae c to search for atmospheric absorption features.

Pi Mensae was selected as the target for its bright apparent magnitude (5.7), visibility during the observing window, and short orbital period allowing multiple transit opportunities — despite its small transit depth (0.32 ppt) putting the transmission spectroscopy goal at the margin of feasibility.

## Method

- **Observation:** 6 × 30-minute exposures across 5 nights on the UCMJO McLellan 1m Telescope (1 aborted due to rain), plus hourly thorium-argon calibration lamp exposures and nightly white-light exposures.
- **Reduction:** bias subtraction → master white synthesis → order tracing → wavelength calibration via thorium-argon atlas matching → per-order continuum normalisation → order combination into a single spectrum.
- **Radial velocity:** measured via Gaussian fitting of 62 known strong iron absorption lines (NIST line list) against their catalogued rest wavelengths, converted to velocity via the Doppler shift equation.
- **Transmission spectrum:** obtained by differencing the master in-transit and out-of-transit stellar spectra, then inspecting for absorption features indicating atmospheric gases.
- **Stellar parameters:** fit by χ² comparison of the observed, telluric-clipped spectrum against 123 synthetic spectra from the POLLUX database, spanning a parameter range around literature values.

## Results

| Quantity | Result |
|---|---|
| Radial velocity | (103 ± 6) × 10² m/s — agrees with literature |
| Transmission spectrum | No clear absorption features detected (aside from a likely auroral line and a likely telluric triplet) |
| Stellar parameters (best fit) | Did not agree with literature values (χ² = 150.89) |

**Radial velocity** was successfully determined and matched published values. **Transmission spectroscopy** returned a null result, consistent with Pi Mensae c's very small transit depth and likely atmospheric escape given its close-in orbit (~0.02 AU). **Stellar parameter fitting** was unsuccessful due to over-aggressive continuum normalisation during reduction, which slightly distorted the observed spectrum relative to the un-normalised synthetic comparison spectra; attempts to compensate by fixing individual parameters were confounded by the inverse relationship between temperature and metallicity effects on the spectrum.

## Next Steps

- Capture additional in/out-of-transit spectra of Pi Mensae c to improve signal-to-noise.
- Renormalise the observed spectrum to better align with the synthetic comparison set.
- Develop an automated line-search method (rather than manual inspection) to speed up future transmission spectrum analysis.

## Contents

- `ASTR211_ObservingProposal.docx` — original observing proposal
- `Project Reduction.ipynb` — spectral reduction pipeline
- `Spectrum Fitting.ipynb` — radial velocity and stellar parameter fitting
- `211 Report.docx` — full written report with figures and references
- `Lab1`–`Lab5` — supporting coursework/lab exercises

## References

Full reference list (Garcia Munoz et al. 2019, Huang et al. 2018, King et al. 2019, NIST ASD, SIMBAD, POLLUX/AMBRE, and others) is included in the full report.
