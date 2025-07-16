# Packages and Virtual Environments

## 1. `pip` and Virtual Environments

It is recommended to use a virtual environment to manage your project's dependencies. This keeps your packages isolated from the global Python installation.

### Creating a Virtual Environment

Open your terminal (Command Prompt on Windows, Terminal on macOS/Linux) on your *projects directory* and run:

```bash
python -m venv .venv
```

This creates a `.venv` folder in your *project directory*.

### Activating the Virtual Environment

- **Windows:**

  ```bash
  .venv\Scripts\activate
  ```

- **macOS/Linux:**

  ```bash
  source .venv/bin/activate
  ```

You should see your prompt change, indicating the environment is active.

### Installing Packages

With the virtual environment activated, install packages using:

```bash
pip install package_name
```

Replace `package_name` with the name of the package you want to install (e.g., `numpy`).

### Requirements File

To manage dependencies, you can create a `requirements.txt` file. This file lists all the packages your project depends on.
You can create it by running:

```bash
pip freeze > requirements.txt
```
Or to create it more efficiently, take a look here,
- <https://stackoverflow.com/questions/31684375/automatically-create-file-requirements-txtu>

To install all packages listed in `requirements.txt`, run:

```bash
pip install -r requirements.txt
```

## 2. Importing Third-Party Packages

After installation, you can import the package in your Python script or notebook:

```python
import package_name
```

For example:

```python
import math # pre-installed module
from datetime import datetime # pre-installed module
import random as rnd # pre-installed module

# Using imported modules
print(math.sqrt(16))
print(math.pi)

# Current datetime
now = datetime.now()
print(now)

# Random number
print(rnd.randint(1, 10))

# Common data science imports (third party)
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

## 3. Using Jupyter Notebook

Jupyter Notebook is an interactive environment for running Python code.

### Installation

For windows you can install directly from their official website, or anaconda distribution. For macOS/Linux, you can install Jupyter from their respective package managers.

### Running Jupyter

If you are using anaconda, you can launch it from the Anaconda Navigator. For other cases, start Jupyter Notebook by running:

```bash
jupyter notebook
```

This will open a web interface in your browser. You can create new notebooks and run Python code interactively.

### Importing Packages in Jupyter

You can import packages in a notebook cell just like in a script:

```python
import pandas as pd
```

---

**Tip:** If you need to install a package directly from a Jupyter notebook in windows, use:

```python
!pip install package_name
```

**Tip:** And for macOS/Linux, you can use your package manager (like `pacman` or `apt` or `brew`) to install Python packages globally, but it's better to stick with virtual environments for project-specific dependencies
