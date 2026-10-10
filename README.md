# MP1 - Data Processing Pipeline

## Project Description

This project is a Python data processing pipeline that loads, validates, cleans, and saves data. The `pipeline.py` file coordinates the entire process using settings from `config/config.yaml`. The `data_loaders.py` module loads input data from CSV, JSON, or YAML files. The `data_validator.py` module checks required columns and removes rows containing invalid numeric values. The `data_processor.py` module removes duplicates, handles missing values, and removes outliers using the IQR method. The `data_output.py` module saves the cleaned dataset as a CSV file, while `utils.py` handles logging and input file validation. All these modules are organized in the `src` folder, and the pipeline generates a cleaning report showing how many rows and columns were removed.

## How to Run

Run the following command in the terminal:

```bash
python pipeline.py --input fixtures/sample_data.csv --output output/clean.csv --config config/config.yaml --verbose
```

## Example Output

Using the provided sample dataset:

- Original dataset: 100 rows
- After validation: 98 rows
- After duplicate removal: 96 rows
- After missing-value handling: 94 rows
- After outlier removal: 92 rows

The cleaned dataset is saved to `output/clean.csv`.

## Cleaning Report

```text
rows_before: 98
rows_after: 92
rows_removed: 6
columns_before: 5
columns_after: 5
columns_removed: 0
```
