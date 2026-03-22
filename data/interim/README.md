# Interim data (optional)

Place **merged** country–year files here *before* cleaning if you want a clear pipeline:

- Suggested filename: `country_year_panel_merged.csv` (same columns as your modeling dataset).

Notebook **01** loads the first file that exists among:

1. `interim/country_year_panel_merged.csv`
2. `country_year_modeling_dataset.csv` (project `data/` root)
3. `processed/country_year_modeling_dataset.csv`

The **cleaned** output is always written to `processed/country_year_modeling_panel_cleaned.csv`.
