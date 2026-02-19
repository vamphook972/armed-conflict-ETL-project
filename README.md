# Armed Conflict Project – ETL

ETL class project focused on processing and analyzing datasets related to victims of armed conflicts. The repository includes data extraction, transformation, and loading pipelines, as well as data cleaning and exploratory analysis to ensure data quality and generate meaningful insights.

---

## Project Structure
```
armed-conflict-ETL-project/
│
├── data/
│   ├── raw/          # Original datasets (do not modify)
│   ├── processed/    # Cleaned/transformed datasets
│
├── notebooks/       # Jupyter notebooks (EDA & analysis)
│
├── src/              # Python ETL scripts
│
├── requirements.txt
└── README.md
```

---

## Environment Setup

It is recommended to use a virtual environment:

## macOS/Linux
```bash
python -m venv venv
source venv/bin/activate

pip install -r requirements.txt
```

## Windows
```bash
python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
```
---

## Working with Notebooks (IMPORTANT)

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
