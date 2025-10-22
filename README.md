# data-driven-control

A small repository with materials and data for hands-on exercises on data-driven control.
The repository contains a Jupyter notebook which explores system identification and control using measured/simulated datasets provided in the `Linear/` and `Non-linear/` folders.

## Contents

Top-level files

- `TP_Data_driven_control.ipynb` : Main Jupyter notebook for the practical session (TP).
- `README.md` : This file.
- `LICENSE` : Project license.

Data folders

- `Linear/` : MATLAB .mat files used in linear identification examples.
  - `echelon.mat`
  - `SPEED.mat`
- `Non-linear/` : CSV datasets and simulated speed files for non-linear identification examples.
  - `db_u1.csv` ... `db_u7.csv`
  - `vitesse_simulee1.csv` ... `vitesse_simulee7.csv`

## Purpose

This repository is intended for coursework or self-study on data-driven control and system identification. The included notebook (`TP_Data_driven_control.ipynb`) demonstrates how to:

- Load and pre-process measured data (MAT and CSV files).
- Perform basic system identification (linear / non-linear approaches).
- Design and evaluate control strategies from identified models.
- Plot and compare simulated vs measured responses.

The materials are educational and designed to be run interactively in Jupyter.

## Quick start (Windows / PowerShell)

1. Create and activate a Python virtual environment (recommended):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

1. Install the minimal Python dependencies:

```powershell
pip install --upgrade pip
pip install jupyterlab numpy scipy pandas matplotlib seaborn
```

1. Start Jupyter Lab or Notebook and open `TP_Data_driven_control.ipynb`:

```powershell
jupyter lab
# or
jupyter notebook
```

1. In the notebook, run the cells sequentially. The notebook expects the `Linear/` and `Non-linear/` folders to be present at the repository root.

Notes:

- The `.mat` files in `Linear/` can be read from Python using `scipy.io.loadmat`.
- If you prefer MATLAB, the `.mat` files can be opened directly in MATLAB/Octave.

## Contract (inputs / outputs / success criteria)

- Inputs: data files in `Linear/` (.mat) and `Non-linear/` (.csv). The notebook reads these files and computes identification and simulation results.
- Outputs: plots and numeric results shown inline in the notebook (figures, identified model parameters).
- Success criteria: the notebook runs without errors and produces the expected plots when required dependencies are installed and the data folders are present.

## Edge cases and troubleshooting

- Missing files: ensure all files from the `Linear/` and `Non-linear/` folders are present in the project root.
- Dependency errors: check that the Python virtual environment is activated and required packages (`numpy`, `scipy`, `pandas`, `matplotlib`, `jupyterlab`) are installed.
- Large notebooks: if the notebook is slow, run only the sections you need or increase available memory for Jupyter.

## Suggested improvements / Next steps

- Add a `requirements.txt` or `environment.yml` to pin dependencies.
- Add a small driver script (e.g., `run_tp.py`) to reproduce specific figures non-interactively.
- Add short README files inside `Linear/` and `Non-linear/` to describe each dataset in detail.

## License

This repository includes a `LICENSE` file at the project root. Consult it for license details.

## Author / Contact

Prepared by Josselin Perret (repository owner). For questions, open an issue in the repository.
