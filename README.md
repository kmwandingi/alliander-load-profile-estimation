# Alliander Load Profile Estimation

This project focuses on load profile estimation using conditional Variational Autoencoders (CVAE).

## Project Structure

- `models/`: Contains trained models
- `notebooks/`: Jupyter notebooks for analysis and modeling
- `references/`: Reference papers and documents
- `reports/`: Generated figures and draft results report
- `data/`: Dataset files (provided separately as a zip file)

## Setup

1. Clone this repository: `git clone https://github.com/kmwandingi/alliander-load-profile-estimation.git`

2. Install dependencies: `pip install -r requirements.txt`

3. Unzip the provided dataset files into the `data/processed` directory.

## Running the Notebooks

1. Start Jupyter Notebook:
jupyter notebook

2. Navigate to the `notebooks/` directory and open the desired notebook:
- `0.0-preprocess-features.ipynb`: Data preprocessing
- `1.0-cvae-v3.ipynb`: Conditional Variational Autoencoder model
- `1.1-cvae-v3-month-evaluate-reconstruction.ipynb`: CVAE evaluation
- Other notebooks as listed in the directory

## Docker Support

A Dockerfile is provided for containerized execution:

1. Build the Docker image:
`docker build -t alliander-load-profile .`

2. Run the container:
`docker run -p 8889:8889 -v $(pwd):/notebooks alliander-load-profile`

3. Access Jupyter Notebook through the URL provided in the console output.

## Data Files

The following data files are some of the used files in this project and can be provided via zip:
- df_merged_filtered_no_pv_wind.feather
- df_metered_monthly_500_balanced.feather
- df_unmetered_monthly_500_balanced.feather
- updated_combined_reconstructed_denormalised_balanced.csv

Ensure these files are placed in the `data/processed` directory before running the notebooks.

## Additional Information

For more details on the project, methodology, and results, refer to the draft report in the `reports/` directory.
