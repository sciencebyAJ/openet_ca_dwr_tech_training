# openet_ca_dwr_tech_training
## OpenET Technical Training Resources for California DWR

The notebooks and files in this repository were prepared for an OpenET Technical Training for the California Department of Water Resources in September 2026.

### slide decks will be posted here


## Get Set Up for the Workshp:

### Installing the Python dependencies

These instructions are written for users who are new to Python. The recommended approach is to create a virtual environment for this repository. A virtual environment keeps this project's packages separate from other Python projects on your computer.

#### 1. Install Python

Install Python 3.10 or newer from [python.org](https://www.python.org/downloads/). During installation on Windows, select **Add Python to PATH** if that option is shown.

Check that Python is installed:

##### macOS or Linux

```bash
python3 --version
```

##### Windows

```powershell
py --version
```

#### 2. Open a terminal in the repository folder

Move into the folder that contains this `requirements.txt` file. For example:

```bash
cd path/to/this/repository
```

On Windows PowerShell, use the same command with the repository's actual folder path.

### 3. Create a virtual environment

#### macOS or Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

#### Windows PowerShell

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
```

After activation, your terminal usually shows `(.venv)` at the beginning of the prompt.

### 4. Install the requirements

With the virtual environment activated, run:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

The second command reads the package names in `requirements.txt` and installs them. The geospatial packages may take a few minutes to install.

### 5. Start JupyterLab

```bash
jupyter lab
```

This opens JupyterLab in a web browser. Open the notebook from the repository and select the Python kernel associated with `.venv` if Jupyter asks you to choose one.

### 6. Confirm that the packages work

Run this from the activated virtual environment:

```bash
python -c "import geopandas, matplotlib, numpy, pandas, requests, rioxarray, shapely; print('Dependencies installed successfully.')"
```

### Troubleshooting

- If `python3` is not recognized, try `python`. On Windows, try `py`.
- If a command says that pip is not found, use `python -m pip` as shown above instead of running `pip` directly.
- If PowerShell refuses to activate the environment, open Command Prompt and run `.venv\\Scripts\\activate.bat`, or ask your system administrator about the execution-policy setting.
- To leave the virtual environment, run `deactivate`.
- To use the project again later, open a terminal in the repository, activate `.venv`, and then run `jupyter lab`.
