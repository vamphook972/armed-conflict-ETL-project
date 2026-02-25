# Armed Conflict Project – ETL

ETL project focused on processing and analyzing datasets related to victims of armed conflicts. The repository includes data extraction, transformation, as well as data cleaning and exploratory analysis to ensure data quality and generate meaningful insights.

This project documents a reproducible ETL flow: the notebooks in `notebooks/` perform extraction and cleaning from `data/raw/` and generate artifacts in `data/processed/`. The code and dependencies are designed to facilitate reproducibility and academic collaboration.

## Requirements
- Python 3.8 or higher
- git
- (Optional) JupyterLab or Jupyter Notebook
- Creating and activating a virtual environment is recommended

---

## Project Structure
```
armed-conflict-ETL-project/
│
├── data/
│   ├── raw/         # Original datasets (do not modify)
│   ├── processed/    # Cleaned/transformed datasets
│
├── notebooks/       # Jupyter notebooks (EDA & analysis)
│
├── requirements.txt
└── README.md
```

### Output and data
- Original data: `data/raw/`
- Processed data: `data/processed`

### Technology stack and justification
- **Python**: mature language with a strong ecosystem for data science.
- **pandas / numpy**: manipulation and transformation of tabular data.
- **Jupyter (Lab/Notebook)**: interactive environment for exploration, documentation, and reproducibility.
- **matplotlib / seaborn**: static and exploratory visualization.
- **scikit-learn** (if applicable): tools for preprocessing and modeling.
- **virtualenv / venv + pip**: simple and explicit dependency management.
- **nbdime**: diffs and merges specific to notebooks (avoids binary conflicts in .ipynb).




## Environment Setup

It is recommended to use a virtual environment:

### macOS/Linux
```bash
python -m venv venv
source venv/bin/activate

pip install -r requirements.txt
```

### Windows
```bash
python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
```
---

### Working with Notebooks (IMPORTANT)

We keep outputs and some initial ETL funtion in notebooks, so follow these rules (only for developers who need to submit changes):

Before committing:

	1.	Restart Kernel
	2.	Run All cells
	3.	Save notebook
	4.	Then commit

This ensures:

	•	Clean execution order
	•	Reproducibility
	•	Reduced merge conflicts

### Required Tool: nbdime

To properly manage notebook diffs and merges, install:
```bash
pip install nbdime
nbdime config-git --enable
```