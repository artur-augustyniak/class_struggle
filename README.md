# Class Struggle

Repository accompanying the ["Class Struggle"](article/class_struggle.pdf)  article.
The repository demonstrates use of an autoencoder for detecting domains similar to a known (sub)set of phishing domains published by CERT Polska.

## Data Sources

### CERT Polska Warning List

This project uses data from the **CERT Polska Warning List** https://cert.pl/en/warning-list/
maintained by [CERT Polska (NASK)](https://cert.pl/en/).

The data are used **solely for research and educational purposes**
The raw list of domains is not redistributed in this repository.


### Majestic Million

This project uses data from the Majestic Million dataset 
maintained by [Majestic](https://majestic.com/reports/majestic-million)

The dataset is provided under the Creative Commons Attribution 3.0 License (CC BY 3.0)

The data are used **solely for research and educational purposes**
The raw dataset is not redistributed in this repository.


## Repository contents
- `notebooks/0_fetch_data.ipynb` - downloading source data
- `notebooks/1_eda.ipynb` - exploratory data analysis (EDA) of data from the CERT.PL warning list
- `notebooks/2_eda_based_data_selection.ipynb`- EDA based training set selection
- `notebooks/3_autoencoder_train_eval_inference.ipynb` - construction, training, and inference of the autoencoder
- `notebooks/xor_nn_decission_boundary.ipynb` - auxiliary demonstration script


## Running (locally, in Docker)
1. Build and start the Jupyter container:
   ```bash
   docker compose up --build
   ```
2. Open: `http://127.0.0.1:8888/tree` and run numbered notebooks in order: `0_fetch...`, `1_eda...`, `2_eda_based...`, `3_autoencoder...`.


## Generate article
```bash
cd ./article
pdflatex class_struggle.tex
```

