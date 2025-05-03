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
1. All data files are stored in [Google Drive](https://drive.google.com/drive/folders/1yRkXccV5pG-vJD93VJ6cPRPnHxwE8rjT?usp=sharing).
2. Download the required raw data files from Google Drive.
3. Place the downloaded files in the `data/raw/` directory.
4. Place any supporting files (such as geojson) in the `data/support/` directory.

### 2. Data Folder Structure
- `data/raw/` — All original, unprocessed data files (e.g., `311_data.csv`, `weather_data.csv`)
- `data/support/` — Supporting/reference files (e.g., geojson)
- `data/processed/` — Cleaned and processed data outputs

### 3. Running the Notebooks
1. Start with the data cleaning notebook: `notebooks/1_data_cleaning.ipynb`  
   - This will read from `data/raw/` and output cleaned datasets to `data/processed/`.
2. Next, run the weather data cleaning notebook: `notebooks/1.5_weather_data_cleaning.ipynb`  
   - This will process weather data and save results to `data/processed/`.
3. Continue with the EDA notebook: `notebooks/2_eda.ipynb`
4. Proceed with the remaining notebooks in order as needed for your analysis and modeling.

### Note
- Raw data and large files are not tracked in this repository.
- Each notebook will output processed data to the appropriate directories.
- GeoJSON and other support files should be placed in `data/support/`.