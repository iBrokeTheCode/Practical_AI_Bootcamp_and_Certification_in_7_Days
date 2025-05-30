# Python and Jupyter Lab

This guide will walk you through setting up a dedicated Python virtual environment using `uv` to install JupyterLab and essential Machine Learning (ML) libraries. This ensures your project dependencies are isolated and your development environment remains clean and efficient.

## Prerequisites

Before you begin, make sure you have the following installed:

1.  **Python 3.8+**: Download and install Python from [python.org](https://www.python.org/downloads/).
2.  **`uv`**: The `uv` tool is a fast Python package installer and virtual environment manager. If you don't have it yet, you can install it using `pip` (Python's package installer, which comes with Python):

    ```bash
    pip install uv
    ```

## Installation Steps

Follow these steps to set up your ML environment:

### Step 1: Create a Project Directory

First, create a dedicated folder for your ML tutorials and navigate into it. This is where your virtual environment and Jupyter notebooks will reside.

```bash
mkdir ml_tutorials
cd ml_tutorials
```

### Step 2: Create a Virtual Environment with `uv`

Now, create a virtual environment using `uv`. This will create an isolated space for your project's Python packages.

```bash
uv venv
```

You should see output similar to `Created virtualenv at ./.venv`. `uv` automatically names the environment `.venv` by default.

### Step 3: Activate the Virtual Environment

Before installing any packages, you need to activate your newly created virtual environment. This tells your system to use the Python interpreter and packages from this specific environment, rather than your global Python installation.

```bash
source .venv/bin/activate
```

_(On Windows, if you're using PowerShell, it might be `.\.venv\Scripts\Activate.ps1` or `.\.venv\Scripts\activate.bat` for Command Prompt)._

You'll know the environment is active when you see `(.venv)` prepended to your terminal prompt.

### Step 4: Install JupyterLab and Essential ML Libraries

With your virtual environment activated, install `jupyterlab` and other common Machine Learning libraries that you'll likely use in your tutorials.

```bash
uv pip install jupyterlab numpy pandas scikit-learn matplotlib seaborn
```

- **`jupyterlab`**: The modern, web-based interactive development environment for Jupyter notebooks.
- **`numpy`**: Fundamental package for numerical computing with Python.
- **`pandas`**: Data manipulation and analysis library.
- **`scikit-learn`**: A comprehensive library for various ML algorithms.
- **`matplotlib`**: A widely used plotting library for creating static, interactive, and animated visualizations.
- **`seaborn`**: A data visualization library based on matplotlib, providing a high-level interface for drawing attractive and informative statistical graphics.

### Step 5: Launch JupyterLab

Once all packages are installed, you can launch JupyterLab from your active virtual environment:

```bash
jupyter lab
```

This command will open JupyterLab in a new tab in your default web browser (usually at `http://localhost:8888/lab`). From here, you can start creating new notebooks (`.ipynb` files), open existing ones, and begin coding!

### Step 6: Deactivate the Virtual Environment (When Done)

When you're finished working on your ML tutorials and want to exit the virtual environment, simply type:

```bash
deactivate
```

Your terminal prompt will return to its normal state. Remember to reactivate the environment (`source .venv/bin/activate`) each time you want to work on this project.
