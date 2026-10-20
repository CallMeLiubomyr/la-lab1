# Labs for Linear Algebra course (UCU)

## Labs

- [Lab 1: Least squares and Fourier analysis](lab1/README.md)
- [Lab 2: Power iteration and PageRank](lab2/README.md)

Each lab keeps its notebooks, documentation, and any input data in its own
directory. All labs use one local virtual environment at the repository root.

## Setup

Use Python 3.14.7 for a consistent environment across the team. From the
repository root on macOS or Linux:

```sh
python3.14 --version  # Expected: Python 3.14.7
python3.14 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip check
```

If `.venv` already exists with this Python version, activate it and install the
requirements without recreating it. Each teammate creates their own `.venv`;
it is ignored by Git. Commit dependency changes to the root `requirements.txt`.

## Running notebooks

Open the repository in VS Code with the Python and Jupyter extensions installed.
Open a notebook, choose **Select Kernel → Python Environments**, and select the
repository's `.venv/bin/python`.

Run notebooks with their lab directory as the working directory. In particular,
Lab 1 reads `land-temp-1850-2015.csv` relative to `lab1/`. If the file is not
found, check the kernel's working directory with `Path.cwd()` from `pathlib`.

Use **Restart & Run All** before submission and save the resulting outputs.
Existing saved outputs may record older Python or package versions; rerunning
with the shared environment refreshes them.

When changing shared dependency versions, rerun the notebooks in both labs to
check compatibility. Use separate lab environments only if future labs require
incompatible Python or package versions.
