# BT-SuccessfulFootballTransfer
Bachelor Thesis: Analysis and Prediction of Successful Football Player Transfers

This repository contains the code used for "Analysis and Prediction of Successful Football Player Transfers" to produce and verify the results. The code generates and cleans the data from Fbref.com and Transfermarkt.com, performs  principal component analysis (PCA), trains random forest models (both regression and classification) and visualizes the results.

To run the code you can follow the instructions below in the order provided. If you do not want to generate the data yourself, all data is provided to download and generate the models and plots. 

---

## Repository Structure

To **run everything from scratch**, follow this order:

1. **PCA.Rmd**  
   - Performs PCA analysis on the raw data.
   - Generates transformed features for modeling.

2. **Daten.Rmd**  
   - Loads and processes the datasets.
   - Prepares the datasets for both regression and classification tasks.
   - Outputs cleaned datasets and generates transfer value

3. **rf.Rmd**  
   - Trains all random forest models (using `ranger`).
   - Saves the trained models (both regression and binary classification) in the `models/` folder using `.rds`.
   - Generates all variable interaction tables

4. **plots.Rmd**  
   - Generates 1D and 2D partial dependence plots.
   - Saves output plots into the `plots/` folder as PNG files using `ggsave()`.

---

## Folder for Data Structure

### `csv data/`
Contains all cleaned datasets used or generated in the project.

- Example: `df_data2reg.csv`, `fw_data2bin.csv`, `train_data_df2.csv`, etc.

### `models/`
Contains all saved random forest models in `.rds` format.

- Example: `rfbin_df2.rds`, `rfreg_fw2.rds`, etc.

### `plots/`
Contains saved plots as image files (e.g., `.png`).

- Example: `vivi_df.png`, `vivi_fw.png`, etc.

### `data/`
Contains raw or intermediate data used in PCA or loaded in `Daten.Rmd`.

---

## To Load Everything Without Running Code

If you don't want to rerun the full pipeline, you can:

- Use the CSVs in `csv data/` to load all preprocessed datasets.
- Use the `.rds` files in `models/` to load trained models.
- Use the plots in `plots/` for visual analysis and reporting.

  
