# Transformational AI - Amazon Reviews Data Science Project

## Project Overview
This project involves analyzing and transforming Amazon Reviews 2023 datasets for machine learning model development. You will work with pandas DataFrames, create visualizations using seaborn and matplotlib, and export cleaned data in .csv and .parquet formats.

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
├── .gitignore
├── environment.yml                # Conda environment specification
└── amazon_reviews_analysis.ipynb  # Main analysis notebook
```

## Learning Objectives
- Set up a Python environment using Jupyter Notebooks
- Utilize pandas, matplotlib, and seaborn for data manipulation and visualization
- Perform data transformation and export cleaned datasets
- Generate insightful visualizations for business insights
- Reinforce Pythonic concepts for PCEP exam preparation

## Data Sources
- Amazon Reviews 2023 datasets from Hugging Face

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
