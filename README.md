# openet_ca_dwr_tech_training

## OpenET Technical Training Resources for California DWR

The notebooks and files in this repository were prepared for an OpenET Technical Training for the California Department of Water Resources in September 2026.

### Slide decks will be posted here

## Get Set Up for the Workshop

### Installing Python and package dependencies

These instructions install the required Python packages to follow along and participate in the workshop.

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
Download the `requirements.txt` file from this repository. Navigate into the folder that contains this `requirements.txt` file. For example:

```bash
cd path/to/this/repository
```

On Windows PowerShell, use the repository's actual folder path.

#### 3. Install the required packages

##### macOS or Linux

```bash
python3 -m pip install --user --upgrade pip
python3 -m pip install --user -r requirements.txt
```

##### Windows PowerShell

```powershell
py -m pip install --user --upgrade pip
py -m pip install --user -r requirements.txt
```

The above commands read the package names in `requirements.txt` and installs them in your Python environment. Some of the the geospatial packages may take a few minutes to install. It's important for the requirements to be fully installed to ensure the Python environment works appropriately.

#### 4. Confirm that the packages work

In terminal or PowerShell paste the following command to verify the dependencies are installed.

##### macOS or Linux

```bash
python3 -c "import geopandas, matplotlib, numpy, pandas, requests, rioxarray, shapely; print('Dependencies installed successfully.')"
```

##### Windows PowerShell

```powershell
py -c "import geopandas, matplotlib, numpy, pandas, requests, rioxarray, shapely; print('Dependencies installed successfully.')"
```

#### 5. Confirm JupyterLab is installed.
##### macOS or Linux

```bash
python3 -m jupyter lab
```

##### Windows PowerShell

```powershell
py -m jupyter lab
```

This opens JupyterLab in a web browser. Open the notebook from the repository and select the Python installation where you installed the packages, if Jupyter asks you to choose a kernel.


### Troubleshooting

- If `python3` is not recognized, try `python`. On Windows, try `py`.
- If pip is not found, use `python3 -m pip` on macOS or Linux, or `py -m pip` on Windows.
- If the `jupyter` command is not found, use the `python3 -m jupyter lab` or `py -m jupyter lab` command shown above.
- To use the project again later, open a terminal in the repository and run the appropriate JupyterLab command. You do not need to activate anything.


### How to close a JupyterLab session

Always save your notebooks before closing JupyterLab. Closing the browser tab alone does not stop the JupyterLab server.

1. Save your notebooks.
2. Close the JupyterLab browser tab.
3. Return to the terminal or PowerShell window.
4. Press `Ctrl+C`, confirm shutdown if prompted, and press `Ctrl+C` again only if necessary.

#### If JupyterLab is running in the current terminal

Return to the terminal or PowerShell window where JupyterLab is running and press:

```text
Ctrl+C
```

If prompted to shut down the server, type `y` and press **Enter**. If there is no prompt, press `Ctrl+C` a second time.

#### Stop JupyterLab from another terminal

If the original terminal is unavailable, list the running Jupyter servers:

##### macOS or Linux

```bash
python3 -m jupyter server list
```

##### Windows PowerShell

```powershell
py -m jupyter server list
```

Then stop the server using its port number, usually `8888`:

##### macOS or Linux

```bash
python3 -m jupyter server stop 8888
```

##### Windows PowerShell

```powershell
py -m jupyter server stop 8888
```

Replace `8888` with the port shown by the server-list command.

