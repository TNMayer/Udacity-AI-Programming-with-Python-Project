# Transformational AI - Amazon Reviews Data Science Project

## Project Overview
This project analyzes Amazon Reviews 2023 datasets to prepare a cleaned product dataset for machine learning. It uses pandas for data transformation, matplotlib/seaborn for visualization (including a regression line with a confidence band), and exports cleaned results to .csv and .parquet. The notebook also captures reflection answers and writes them to a text file.

## Environment Setup

### Prerequisites
- Anaconda or Miniconda installed

### Creating the Conda Environment
The project uses a dedicated conda environment named `transformational_ai`. The environment is defined in `environment.yml` for cross-platform reproducibility.

**Create the environment from the YAML file:**
```bash
conda env create -f environment.yml
```

**Activate the environment:**
```bash
conda activate transformational_ai
```

**Update the environment (if `environment.yml` changes):**
```bash
conda env update -f environment.yml --prune
```

**Remove the environment (if needed):**
```bash
conda deactivate
conda env remove -n transformational_ai
```

### Installed Packages
- `python` - Python 3.11
- `datasets` - For loading Hugging Face datasets
- `pandas` - Data manipulation and analysis
- `matplotlib` - Data visualization
- `seaborn` - Statistical data visualization
- `pyarrow` - For parquet file support
- `ipykernel` - Jupyter notebook support

### Running Jupyter Notebooks
1. Activate the conda environment: `conda activate transformational_ai`
2. Open VS Code and select the `transformational_ai` kernel
3. Run the notebook cells

## Project Structure
```
01_Python_for_AI/
├── README.md
├── RUBRIC.md
├── environment.yml                      # Conda environment specification
├── Udacity - PCEP Project.ipynb         # Main analysis notebook
├── user_inputs.txt                      # Reflection answers (generated)
└── data/
	├── top_products.csv                 # Cleaned dataset export
	└── top_products.parquet             # Cleaned dataset export
```

## Learning Objectives
- Set up and use a Python environment with Jupyter Notebooks
- Load large datasets with sampling and transform data using pandas
- Visualize distributions and relationships, including regression with a confidence band
- Export cleaned datasets to .csv and .parquet
- Capture and save reflection answers to a text file

## Data Sources
- Amazon Reviews 2023 datasets from Hugging Face (Electronics reviews + metadata)

## Rubric Coverage Checklist
All rubric criteria are addressed in the notebook:

- Environment checks and package installs ✅
- Reviews and metadata datasets loaded with limits and boolean parameters ✅
- Data inspection via `.head()`, `.columns`, `.dtypes`, and `.info()` ✅
- Robust product lookup with `try/except` ✅
- Cleaning and filtering for top products (rating and price constraints) ✅
- Percentage calculation function ✅
- CSV and Parquet exports ✅
- Title list extraction ✅
- Histogram and scatterplot visualizations (including regression line + confidence band) ✅
- 4.7 rating cutoff and sorted highly rated table ✅
- Reflection answers exported to `user_inputs.txt` ✅

## Troubleshooting

### Environment Creation Issues
If you encounter issues creating the environment, try:
```bash
conda clean --all
conda env create -f environment.yml
```

### Platform-Specific Notes
- **Windows**: Use Anaconda Prompt or PowerShell with conda initialized
- **macOS/Linux**: Use terminal with conda initialized
- The `environment.yml` uses platform-independent package specifications to ensure compatibility across all operating systems
