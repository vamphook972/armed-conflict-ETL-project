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





Descripción profesional
----------------------
Repositorio de trabajo para el proyecto ETL (Extracción, Transformación y Carga) enfocado en el procesamiento y análisis de datos sobre víctimas de conflictos armados. Contiene los datos originales y procesados, notebooks con la extracción/transformación y las visualizaciones, y dependencias reproducibles.

Índice
------
- Descripción
- Requisitos
- Instrucciones de ejecución
- Estructura del proyecto
- Stack tecnológico y justificación
- Buenas prácticas (notebooks y control de versiones)
- .gitignore y limpieza del repositorio

Descripción breve
-----------------
Este proyecto documenta un flujo ETL reproducible: los notebooks en `notebooks/` realizan la extracción y limpieza desde `data/raw/` y generan artefactos en `data/processed/`. El código y las dependencias están diseñados para facilitar reproducibilidad y colaboración académica.

Requisitos
----------
- Python 3.8 o superior
- git
- (Opcional) JupyterLab o Jupyter Notebook
- Crear y activar un entorno virtual recomendado

Instalación rápida
------------------
macOS / Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

Windows (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
```

Ejecución
---------
1. Abrir el entorno virtual (ver pasos anteriores).
2. Iniciar JupyterLab o Jupyter Notebook desde la raíz del proyecto:

```bash
jupyter lab   # o: jupyter notebook
```

3. Notebooks principales:
- `notebooks/extraction_transformation.ipynb` — extracción y transformación de los datos.
- `notebooks/load_visualization.ipynb` — carga final y visualizaciones.

4. Si hay scripts en `src/`, se pueden ejecutar como módulo o script (ejemplo genérico):

```bash
python -m src.run_etl   # si existe el módulo/script
```

Salida y datos
--------------
- Datos originales: `data/raw/`
- Datos procesados (artefactos reproducibles): `data/processed/`

Estructura del proyecto
-----------------------
```
armed-conflict-ETL-project/
├── data/
│   ├── raw/            # Datos originales (no modificar sin versionado)
│   └── processed/      # Artefactos generados por el pipeline
├── notebooks/          # Notebooks principales (ETL, EDA, visualización)
├── requirements.txt    # Dependencias del proyecto
├── .gitignore
└── README.md
```

Stack tecnológico y justificación
---------------------------------
- **Python**: lenguaje maduro y con ecosistema fuerte para ciencia de datos.
- **pandas / numpy**: manipulación y transformación de datos tabulares.
- **Jupyter (Lab/Notebook)**: entorno interactivo para exploración, documentación y reproducibilidad.
- **matplotlib / seaborn**: visualización estática y exploratoria.
- **scikit-learn** (si corresponde): herramientas para preprocesamiento y modelado.
- **virtualenv / venv + pip**: gestión simple y explícita de dependencias.
- **nbdime**: diffs y merges específicos para notebooks (evita conflictos binarios en .ipynb).

Justificación resumida:
- El uso de notebooks facilita la trazabilidad del análisis y la comunicación de resultados.
- `pandas` ofrece operaciones ETL eficientes y ampliamente entendidas en entornos académicos y de prototipo.
- `nbdime` reduce riesgos al versionar notebooks en Git, evitando perder ejecuciones o romper el historial.

Buenas prácticas
----------------
- Antes de commitear notebooks: reiniciar kernel y ejecutar todas las celdas, guardar.
- Mantener datos pesados fuera del repositorio (si procede) o versionarlos con herramientas específicas (DVC, Git LFS).
- Usar ramas y PRs para colaboraciones; activar `nbdime` para manejar notebooks:

```bash
pip install nbdime
nbdime config-git --enable
```

.gitignore y limpieza del repositorio
-----------------------------------
Se incluye un `.gitignore` que excluye caches, entornos virtuales y binarios comunes para mantener el repositorio limpio y liviano.

Licencia y contacto
-------------------
Este repositorio es para fines educativos. Para dudas o mejoras, abrir un issue o contactar al autor.

---

Si quieres, puedo también:
- Añadir instrucciones para usar `pipenv` o `poetry` en lugar de `venv`.
- Crear scripts CLI mínimos en `src/` para ejecutar el pipeline fuera de los notebooks.
