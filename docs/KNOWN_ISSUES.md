# Known issues and verification boundaries

## Resolved consistency discrepancies in the supplied revision

- BBR 40% PUP stored S/m is now 295.8 MPa, consistent at display precision with 113.6/0.384 = 295.833333 MPa. This confirms summary arithmetic, not specimen-level repeatability.
- The phenol energy summary now stores -8.785 kcal/mol, matching the manuscript's -8.785. This resolves the prior table/figure discrepancy; it does not independently validate the thermochemical definition or primary output.
- The manuscript snapshot now assigns the storage top/bottom values consistently with Origin column comments (B=top, D=bottom). Experimental specimen labels remain subject to source-record confirmation.
- The manuscript snapshot describes viscosity as temperature dependent and no longer makes the unsupported 20–30 degree construction-temperature reduction claim.
- Table 5 formulas and arithmetic were corrected in the manuscript. Actual molecular model files remain absent.

## Remaining limits

1. **Primary calculations:** Model coordinates, input files, unrounded energies, thermal corrections, calculation temperature/standard state, frequency results, and transition-state connectivity verification were not supplied. Summary columns named ΔH/ΔG retain the source labels without certifying them.
2. **Digitizer coordinates:** Rheological curves, density, specific volume, and reaction paths include DigiData sheets. They are not primary instrument or simulation exports. Image sources and processing need confirmation.
3. **Rheological relations:** The unchanged independent digitized curves previously produced loss/complex modulus ratios above 1 in interpolation screening. This is not a paired-measurement test. Recheck raw data, labels, scales, shift factors, and G'=|G*|cos(delta), G''=|G*|sin(delta).
4. **Tg reconstruction:** The digitized coordinates do not directly reproduce the reported 253 K intersection. Original equilibrium values and regression choices are needed; diagnostic intersections must not replace original MD results automatically.
5. **Density interval:** The exploratory >=20 ps coordinate screen does not support a universal 1.05–1.15 g/cm3 interval. Twenty ps is not an author-confirmed equilibrium cutoff; primary density trajectories are needed.
6. **Viscosity source:** The base-asphalt 135-degree summary is 1.06 Pa s, unlike Table 1's 413 labelled Pa s. Same-batch identity and the original unit/source are unresolved. Two-temperature summaries and a separate 19-point curve are not identical; auxiliary fits are not measured construction windows.
7. **FTIR:** Column-to-sample mapping, ordinate units, offsets, normalization, baseline handling, and original exports need confirmation. Some values exceed 100 and spectra contain a zero initial row. Legacy PUMB labels and peak positions remain in source graph objects. Figure-stage labels also need reconciliation with the preparation order.
8. **Uncertainty:** Error columns are retained, but SD/SE/CI and replicate counts are unspecified. No statistical significance interpretation is assigned.
9. **Missing measurements:** Mass changes, flexural tensile strengths, specimen-level records, and BBD optimization records are not present in these worksheets. Fluorescence images and calibration are outside this OPJU package.
10. **Mixture design:** The separate PUMB/PUPMA and SBS controls' RAP contents, RAP percentage basis, and group-specific mixture formulations need confirmation. The optimum-binder-content project lacks a clear target RAP group.
11. **Identifiers and licence:** The existing repository and earlier Zenodo DOI are documented, but this revision has not yet been assigned a new version DOI. No new licence is selected; confirm consistency with the earlier archive's CC BY 4.0 before publication.

The included consistency checks use a precisely identified manuscript file snapshot. They do not include later chat-only edits, verify all references, or establish raw-data authenticity. Original values are retained; calculated diagnostics are labelled separately.
