# Tutorial Install

Please follow these steps to install the necessary software for the tutorial

## Step 1. Download and install VS Code on your computer

https://code.visualstudio.com/download 

## Step 2. Start VS Code

## Step 3. Configure VS Code

### Open the Extension tab on the left. In the Menu: View | Extensions (Shortcut ⇧⌘X)
   
### Search for and install the following extensions

- Python
- Jupyter
- Github Copilot Chat

You can get GitHub Copilot for free through an education application (later in Step 8). However, if you have a ChatGPT Plus or an Anthropic Claude Code Pro account, you can also (alternatively) use them (optional):
#### If you have a ChatGPT Plus account, install the extension
- Codex - OpenAI's coding agent

#### If you have an Anthropic Claude Code Pro account, install the extension
- Claude Code for VS Code

## Step 4. Create and open a new project folder in VS Code
- in Menu: Open | Open Folder..,
- Navigate to where you want to create a new folder 
- Click the New Folder button and name it, e.g. tutorial
- Click Open

##  Step 5: Open Terminal and install uv

- in Menu: Terminal | New Terminal
- If you are on a Mac: Copy and paste this command into the terminal and execute it (hit return key) (If you are on Windows, go to https://docs.astral.sh/uv/getting-started/installation for installation instructions of uv):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Step 6: Install Python and Python packages with uv

Copy and paste these commands into the terminal one by one and execute them (hit the return key)
```bash
uv init --python 3.13
```

```bash
uv add jupyter matplotlib seaborn pandas scipy pingouin statsmodels openpyxl statannotations scikit-learn xgboost shap
```

```bash
uv sync
```

## Step 7: Register at Github.com (skip if you already have a Github account)

https://github.com/signup

## Step 8: Apply for Education Benefits at Github

https://github.com/settings/education/benefits 

This may take a couple of days for approval. After you get the approval, go to Step 9. 

## Step 9: Activate Github Copilot

https://github.com/settings/copilot/features

