# Pattern Classification of Stock Price Movement

MSc Data Science project, The University of Manchester, 2026.

Stock prices are noisy time series with no predefined labels. This project compares three unsupervised clustering methods on FTSE 100 and FTSE 250 daily adjusted closing prices (z-score standardised) to find stocks that move in similar ways, and tests how meaningful and stable the resulting groups are.

## Notebooks

| Notebook | Method |
|---|---|
| kmeans_clustering.ipynb | PCA and K-Means |
| kmedoids_dtw_pam_clustering.ipynb | Dynamic Time Warping and K-Medoids (PAM) |
| gmm_em_clustering.ipynb | PCA and Gaussian Mixture Model fitted by EM |

All three use consensus clustering (100 subsamples of 80 percent of the stocks) to check stability.

## Data

| File | Stocks | Trading days |
|---|---|---|
| FTSE_100_2015_2025_Dataset.csv | 103 | 2,779 |
| FTSE_250_2021_2026_Dataset.csv | 241 | 1,153 |
| FTSE_250_2025_2026_Dataset.csv | 250 (248 after cleaning) | 273 |

Each CSV has a Ticker column followed by one column per trading date.

## How to run

1. Open a notebook in Google Colab.
2. Run the upload cell and choose a CSV file.
3. Run all cells from top to bottom.

Results are not saved automatically, so export the cluster assignments if you need them.
