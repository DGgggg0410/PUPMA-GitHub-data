# PUPMA experimental and computational figure-source data

This repository is a **working data-release candidate** associated with the manuscript *Modification mechanisms and rheological properties of polyurethane prepolymer-modified asphalt: Insights from molecular simulations and experiments*. It preserves 21 author-supplied Origin projects and exports all 37 discovered worksheets into CSV. It is not a complete raw-instrument or simulation-reproducibility archive.


## Contents

- `data/origin/`: unchanged Origin `.opju` projects under descriptive English filenames.
- `data/worksheets/`: one CSV per worksheet, including empty worksheets and auxiliary fitting/baseline outputs.
- `data/curated/`: selected, readable result tables and arithmetic diagnostics. Derived values are explicitly named `calculated`; stored values remain available separately.
- `metadata/file_manifest.csv`: original filenames, worksheet ranges, provenance classification, paper mapping, and SHA-256 hashes.
- `metadata/column_dictionary.csv`: original column names, long names, units, comments, designation codes, and stored value counts.
- `metadata/columns/`: worksheet metadata and exact exported cell values in JSON.
- `metadata/graph_annotations.json`: text and data references from located `Graph1`–`Graph15` objects; this is not a complete rendering or an exhaustive list of arbitrarily named graph windows.
- `docs/`: limitations, audit results, and release instructions.

## Project-to-paper map

| Project ID | Original filename | Related manuscript content |
|---|---|---|
| `storage_modulus` | 储存模量.opju | Fig. 14(a) |
| `storage_stability` | 储存稳定性.opju | Table 9; Section 4.5 |
| `mixture_low_temperature` | 低温性能.opju | Table 12: strain and stiffness only |
| `complex_modulus` | 复数模量.opju | Fig. 13(a) |
| `mixture_high_temperature` | 高温性能.opju | Table 11 |
| `reaction_thermodynamics` | 各反应的热力学参数指标.opju | Fig. 9; Table 6 |
| `ftir_modification_stages` | 红外光谱 - 副本.opju | Fig. 11 |
| `ftir_pup_dosages` | 红外光谱2.opju | Fig. 12(a,b) |
| `pup_density` | 聚氨酯预聚体模型密度图.opju | Fig. 6(b) |
| `reaction_chain_extender` | 扩链剂与聚氨酯预聚体能量计算结果.opju | Fig. 8(b); Table 6 |
| `asphalt_specific_volume` | 沥青比容-温度曲线.opju | Fig. 5 |
| `reaction_asphaltene_phenol` | 沥青质-苯酚与聚氨酯预聚体能量计算结果.opju | Fig. 8(a); Table 6 |
| `reaction_asphaltene_pyrrole` | 沥青质-吡咯与聚氨酯预聚体能量计算结果.opju | Fig. 8(c); Table 6 |
| `rotational_viscosity` | 黏度曲线.opju | Section 4.5; no viscosity figure in manuscript |
| `binder_physical_and_aging` | 三大指标.opju | Tables 8 and 10; mass changes absent |
| `mixture_moisture_resistance` | 水稳定度.opju | Table 13 |
| `loss_modulus` | 损耗模量.opju | Fig. 14(b) |
| `phase_angle` | 相位角.opju | Fig. 13(b) |
| `optimum_binder_content` | 最佳油石比.opju | Mixture-design context; not tabulated in the manuscript |
| `bbr` | BBR.opju | Fig. 16; Section 4.3 |
| `mscr` | MSCR.opju | Fig. 15; Section 4.2 |

## Samples and dosage bases

PUP denotes polyurethane prepolymer, PUPMA polyurethane prepolymer-modified asphalt, RAP reclaimed asphalt pavement, and SBS styrene–butadiene–styrene. Binder PUP dosages of 30%, 40%, and 50% are relative to **base asphalt mass**, not total binder mass. The crosslinking agent and compatibilizer dosages are 2.25% and 4.25% of base asphalt mass; the chain extender dosage is 15% of PUP mass, according to the comparison manuscript.

Source labels `90#` and `基质沥青` refer to the base asphalt. Legacy labels `PUMB`, `PUMB-30`, `PUMB-40`, and `PUMB-50` appear in the projects. Their apparent correspondence to manuscript PUPMA labels must be confirmed by the authors; originals are retained. The RAP mass basis and the RAP contents of the separate `PUMB` and `SBS` mixture comparison groups are not specified in the supplied projects.

## Units and conditions

The curated files use units identified in source labels or the comparison manuscript: creep stiffness MPa, dimensionless BBR m-value, MSCR recovery %, Jnr kPa^-1, softening point degrees C, ductility cm, penetration 0.1 mm, reaction barriers Ha, enthalpy/Gibbs energy kcal/mol, rut depth mm, dynamic stability cycles/mm, flexural strain microstrain, mixture stiffness MPa, and moisture indicators %. BBR is described at -18 degrees C and MSCR at 64 degrees C in the manuscript. Rheology reference temperature is 36 degrees C. These are manuscript metadata, not independently verified instrument settings.

In the complete worksheet CSV files, columns retain their original letters (A, B, ...). Always consult `column_dictionary.csv`. An empty CSV cell means an empty stored cell or padding after that column's last stored value; per-column counts in metadata distinguish these cases. Original Origin designation codes are retained; in these files 0=Y, 2=Y error, 3=X, and 4=label. An error designation does not establish whether values are SD, SE, CI, or plotting offsets.

## Provenance and limitations

Multiple projects contain `DigiData` sheets with image filenames and `PickedData`/path labels. These are stored image-digitizer coordinates and are distributed as such, **not as raw MD, quantum-chemistry, or DSR output**. Their original image sources and generation history require author confirmation. Other sheets contain result tables, spectra, fitted curves, or auxiliary outputs whose primary acquisition provenance is not established by an Origin project alone.

FTIR source graphs label the ordinate as transmittance (%), but stored spectra contain values above 100 and a zero first row. Processing, normalization, offsets, and spectrum-to-sample assignments require confirmation. The values are retained rather than converted into absolute absorbance or transmittance. Do not quantitatively compare reaction extent from these ordinates without the acquisition and processing details.

No primary Materials Studio input/output files, molecular coordinate files, transition-state frequency/IRC validation, original DSR/BBR/MSCR time histories, fluorescence microscopy images, or replicate-level measurement records were supplied in this package. Table 10 mass changes and Table 12 flexural tensile strengths are also absent from the supplied worksheets. The Box–Behnken experimental design and regression data are not included. See the coverage file.

## Reading the files

CSV files use UTF-8 with BOM to support both Chinese labels and Excel. Numeric values are exported at available precision rather than rounded to the plotting display. Open the CSV files using Excel, a text editor, Python, or R. Origin is only needed for the proprietary project layout and graph objects. The local installation used for extraction was Origin 2024b on Windows; project creation versions are not inferred from this installation.

## License

**No open-data license has been assigned.** The author team requested that licensing remain pending. Public visibility alone does not grant an open reuse license. Confirm the applicable data rights and choose a license before a formal open-data release.

## Citation and publication status

No GitHub repository URL, dataset DOI, or publication DOI has been assigned in this local package. Do not use placeholder identifiers as real citations. When a validated version is released, archive that exact version in a DOI-issuing repository and update the citation metadata. The file `CITATION.cff` contains provisional contributor/title metadata only; dataset contributor roles require author confirmation.

## Contact

Please use the corresponding-author contact in the associated manuscript for scientific questions. This package does not assert that every manuscript result is independently reproducible from the included files.
