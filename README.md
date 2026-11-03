# Sodium-Ion Battery Cathode Dataset: Morphology and Electrochemical Properties

## Dataset overview

The accompanying Excel workbook compiles literature-reported data for sodium-ion battery cathode materials. It contains **2,881 records and 58 columns** in one worksheet (`Sheet1`), with records linked to **145 distinct DOI strings**. The fields cover material formula and structure, synthesis conditions, particle morphology, electrode formulation, cell configuration, electrochemical test conditions, and reported discharge capacity/capacity retention. DOI and source-context fields are provided to support traceability to the original publications.

A row should be treated as a reported data record, not automatically as a unique material or an independent experiment: the same material or paper may contribute multiple records at different rates or cycle numbers. The observed `performance_type` labels include `rate` and `cycling`.

Blank cells indicate that a value was not available or not recorded in the compilation; they must not be interpreted as zero. Units are included in many column names. Text values may retain terminology used in the source publications, so labels and test conditions should be checked before combining records across studies.

## Column descriptions

Column names below are reproduced exactly as they appear in the workbook.

### Material identity, structure, synthesis, and morphology

| Column name | Description |
|---|---|
| `doi` | Digital Object Identifier (DOI) of the source publication used for the record. |
| `normalized_formula` | Normalized chemical formula recorded for the cathode material. |
| `synthesis_method` | Reported material synthesis or processing route; naming may vary across publications. |
| `phase` | Reported structural/stacking phase of the cathode, such as P2, O3, or P3. |
| `secondary_phase` | Secondary phase reported in the source, where specified. |
| `spacegroup` | Crystallographic space group reported for the material. |
| `calcination_temperature_C` | Calcination temperature in degrees Celsius (°C), where reported. |
| `calcination_time_h` | Calcination duration in hours (h), where reported. |
| `particle_size_µm` | Reported particle size in micrometres (µm); measurement methods may differ by source. |
| `morphology` | Recorded morphology descriptor (e.g., spherical, plate, irregular, hexagonal, flake, or rod). The source's characterization method may vary. |

### Electrode formulation and cell configuration

| Column name | Description |
|---|---|
| `active_material_fraction_wt_percent` | Active material fraction in the electrode formulation, in weight percent (wt%). |
| `conductive_additive` | Name or description of the conductive additive used in the electrode. |
| `conductive_additive_fraction_wt_percent` | Conductive additive fraction in the electrode, in weight percent (wt%). |
| `binder` | Name or description of the electrode binder. |
| `binder_fraction_wt_percent` | Binder fraction in the electrode formulation, in weight percent (wt%). |
| `active_material_loading_mg_cm2` | Active-material areal loading, in mg cm⁻². |
| `current_collector` | Material reported for the electrode current collector. |
| `cell_type` | Cell format or type as reported in the source (e.g., coin cell). |
| `cell_configuration` | Reported electrochemical cell configuration, such as a sodium-metal half-cell. |
| `counter_electrode` | Counter-electrode material identified in the source. |
| `reference_electrode` | Reference-electrode material, if specified. |
| `electrolyte` | Reported electrolyte composition or formulation, including components when available. |
| `electrolyte_concentration_M` | Recorded electrolyte concentration in mol L⁻¹ (M), where a numeric concentration is provided. Interpret together with `electrolyte`. |

### Electrochemical conditions and reported performance

| Column name | Description |
|---|---|
| `temperature_C` | Electrochemical test temperature in degrees Celsius (°C). |
| `voltage_min_V` | Lower voltage limit used for the reported test, in volts (V). |
| `voltage_max_V` | Upper voltage limit used for the reported test, in volts (V). |
| `performance_type` | Type of electrochemical record; observed categories include `rate` and `cycling`. |
| `rate_C` | Applied or reported C-rate for the measurement. |
| `current_density_mA_g` | Specific current density in mA g⁻¹, as reported or recorded. |
| `cycle_number` | Cycle number associated with the reported performance value, when applicable. |
| `discharge_capacity_mAh_g` | Reported discharge specific capacity in mAh g⁻¹. |
| `capacity_retention_percent` | Reported capacity retention, in percent (%), when available. The cycle/reference basis should be checked in the source publication. |

### Source context and traceability

| Column name | Description |
|---|---|
| `data_source_reference` | Location of the source information, such as a section, figure, or figure panel. |
| `source_quote_or_context` | Extracted quotation or contextual text supporting the recorded value; consult the full publication for interpretation. |

### Composition descriptors

| Column name | Description |
|---|---|
| `Na_comp` | Numeric sodium composition coefficient recorded for the material. |
| `M_element` | Transition-metal element assigned to the dataset's principal `M` descriptor. |
| `M_comp` | Numeric composition coefficient associated with `M_element`. |
| `dopant_Al` | Numeric composition descriptor for aluminium (Al), as encoded in the dataset. |
| `dopant_B` | Numeric composition descriptor for boron (B), as encoded in the dataset. |
| `dopant_Ca` | Numeric composition descriptor for calcium (Ca), as encoded in the dataset. |
| `dopant_Co` | Numeric composition descriptor for cobalt (Co), as encoded in the dataset. |
| `dopant_Cr` | Numeric composition descriptor for chromium (Cr), as encoded in the dataset. |
| `dopant_Cu` | Numeric composition descriptor for copper (Cu), as encoded in the dataset. |
| `dopant_Fe` | Numeric composition descriptor for iron (Fe), as encoded in the dataset. |
| `dopant_K` | Numeric composition descriptor for potassium (K), as encoded in the dataset. |
| `dopant_Li` | Numeric composition descriptor for lithium (Li), as encoded in the dataset. |
| `dopant_Mg` | Numeric composition descriptor for magnesium (Mg), as encoded in the dataset. |
| `dopant_Mn` | Numeric composition descriptor for manganese (Mn), as encoded in the dataset. |
| `dopant_Mo` | Numeric composition descriptor for molybdenum (Mo), as encoded in the dataset. |
| `dopant_Ni` | Numeric composition descriptor for nickel (Ni), as encoded in the dataset. |
| `dopant_Ru` | Numeric composition descriptor for ruthenium (Ru), as encoded in the dataset. |
| `dopant_Sb` | Numeric composition descriptor for antimony (Sb), as encoded in the dataset. |
| `dopant_Ti` | Numeric composition descriptor for titanium (Ti), as encoded in the dataset. |
| `dopant_Y` | Numeric composition descriptor for yttrium (Y), as encoded in the dataset. |
| `dopant_Zn` | Numeric composition descriptor for zinc (Zn), as encoded in the dataset. |
| `dopant_Zr` | Numeric composition descriptor for zirconium (Zr), as encoded in the dataset. |
| `O_comp` | Numeric oxygen composition coefficient recorded for the material. |
| `F_comp` | Numeric fluorine composition coefficient recorded for the material. |

The `dopant_*` fields are numeric composition descriptors; they should not automatically be treated as binary presence/absence flags. Interpret them together with `normalized_formula`, `Na_comp`, `M_element`, `M_comp`, `O_comp`, and `F_comp`, and confirm the intended encoding against the data-curation protocol before model development.

## Use and reporting notes

Differences in synthesis terminology, morphology labels, cell formats, electrolytes, current densities, C-rates, temperatures, voltage windows, and cycle definitions may affect cross-publication comparisons.
