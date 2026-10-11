# Python Environment Installation

Please follow these steps to install the software for Python for the Data Science and Tutorial courses.

## Step 1. Create a GitHub account

Skip this step if you already have a GitHub account.

https://github.com/signup

## Step 2. Apply for GitHub Education benefits

https://github.com/settings/education/benefits

Approval can take a few days, so apply now and continue with the next steps in the meantime. Once you are approved, you can activate GitHub Copilot for free (Step 10).

## Step 3. Download and install VS Code

https://code.visualstudio.com/download

## Step 4. Start VS Code and install the extensions

Open the Extensions tab on the left (menu: **View | Extensions**, shortcut ⇧⌘X on Mac, Ctrl+Shift+X on Windows).

Search for and install these extensions:

- Python
- Jupyter
- GitHub Copilot Chat (you will sign in to Copilot in Step 10)

Optional: instead of GitHub Copilot, you can use a coding assistant you already pay for:

- If you have a ChatGPT Plus (or higher) plan, install **Codex – OpenAI's coding agent**.
- If you have a Claude Pro or Max subscription, install **Claude Code for VS Code**.

## Step 5. Create and open a project folder

- In the menu: **File | Open Folder…**
- Navigate to where you want to create the folder
- Click **New Folder** and give it a name, e.g. `bipm`
- Click **Open**

## Step 6. Open a terminal and install uv

In the menu: **Terminal | New Terminal**. Copy the command for your system into the terminal and press Return.

On a Mac:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

On Windows:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

**Important:** close the terminal (trash icon in the terminal panel) and open a new one (**Terminal | New Terminal**). Only new terminals know the `uv` command. Check that it works:

```bash
uv --version
```

## Step 7. Install Python and the Python packages

Run these commands one by one in the terminal (inside your project folder).

```bash
uv init --python 3.13
```

This creates the project files (`pyproject.toml`, `.python-version`, `main.py`). Keep Python 3.13: TensorFlow does not support Python 3.14 yet.

```bash
uv add jupyter matplotlib seaborn pandas scipy pingouin statsmodels openpyxl statannotations scikit-learn xgboost shap numpy tensorflow lime treeinterpreter dtreeviz rfpimp
```

This downloads about 1 GB (mostly TensorFlow) and can take a few minutes. It creates a `.venv` folder that contains Python and all packages.

If VS Code asks whether to select the new environment for the workspace folder, click **Yes**.

Later, for example on a new computer or after cloning a project, `uv sync` reinstalls everything listed in `pyproject.toml`.

## Step 8. Check the installation

```bash
uv run python -c "import pandas, sklearn, tensorflow, shap; print('All good')"
```

You should see `All good` (TensorFlow may print a few informational messages first).

## Step 9. Use the environment in a Jupyter notebook

- In the menu: **File | New File…** and choose **Jupyter Notebook**
- Click **Select Kernel** (top right) → **Python Environments…** → **.venv**
- In the first cell, type the code below and run it (Shift+Return):

```python
import pandas as pd
pd.__version__
```

If a version number appears, everything works. In every new notebook, check that **.venv** is selected as the kernel (top right).

## Step 10. Activate GitHub Copilot

After your education benefits are approved (Step 2):

https://github.com/settings/copilot/features

Then sign in to GitHub in VS Code: click the **Accounts** icon (bottom left) and choose **Sign in with GitHub to use GitHub Copilot**.
