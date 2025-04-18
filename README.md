# 311 Data Prediction Project

## Project Structure
```
project/
├── data/
│   ├── raw/               # Original data files from 311
│   ├── processed/         # Cleaned and processed data
│   └── support/           # Support files like geojson
│       └── geojson/       # GeoJSON files for mapping
├── notebooks/
│   ├── 1_data_cleaning.ipynb
│   ├── 2_eda.ipynb
│   ├── 3_feature_engineering.ipynb
│   └── 4_modeling.ipynb
├── models/                # Saved model files
└── README.md              # This file
```

## Data Setup Instructions

### 1. Download 311 Data
1. Visit the Pittsburgh 311 data portal: https://data.wprdc.org/dataset/311-data
2. Click on "Download" or "Export" to download the complete dataset in CSV format
3. Alternatively, use the API to download the data directly in Python:
   ```python
   import pandas as pd
   url = "https://data.wprdc.org/datastore/dump/76fda9d0-69be-4dd5-8108-0de7907fc5a4"
   df = pd.read_csv(url)
   ```

### 2. Place the Data
1. Create a `data/raw` directory in the project root if it doesn't exist already
2. Save the downloaded 311 data as `311_data.csv` in the `data/raw` directory
3. Your data should be located at: `project/data/raw/311_data.csv`

### 3. Running the Notebooks
1. Start with the data cleaning notebook: `notebooks/1_data_cleaning.ipynb`
2. This will generate processed datasets in the `data/processed` directory
3. Continue with the EDA notebook: `notebooks/2_eda.ipynb`
4. Then feature engineering and modeling

### Note
- The raw data is not tracked in this GitHub repository due to its size
- Each notebook will output processed data to the appropriate directories
- GeoJSON files for Pittsburgh neighborhoods will be stored in `data/support/geojson`