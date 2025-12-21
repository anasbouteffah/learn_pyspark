# Python Environment Setup Guide

This guide describes how to set up a new Python project environment on Windows, including virtual environment creation and git configuration.

## 1. Prerequisites

Ensure Python is installed and added to your PATH. Open a terminal (PowerShell or Command Prompt) and run:

```powershell
python --version
```

If this returns a version number (e.g., `Python 3.10.x`), you are ready.

## 2. Create a Virtual Environment

It is best practice to use a virtual environment for each project to manage dependencies in isolation.

1.  Navigate to your project folder:
    ```powershell
    cd c:\Users\dell\Desktop\pyspark
    ```

2.  Run the command to create a virtual environment named `venv`:
    ```powershell
    python -m venv venv
    ```
    This creates a folder named `venv` in your directory.

## 3. Activate the Environment

Before installing packages, you must activate the environment.

**On Windows (PowerShell):**
```powershell
.\venv\Scripts\Activate
```

**On Windows (Command Prompt):**
```cmd
venv\Scripts\activate.bat
```

Once activated, you will see `(venv)` at the start of your command prompt.

## 4. Install & Manage Dependencies

With the environment activated, you can install packages (e.g., `pyspark`, `pandas`):

```powershell
pip install pyspark pandas
```

To save your list of installed packages for others to use:

```powershell
pip freeze > requirements.txt
```

## 5. Configure .gitignore

Before pushing to GitHub, you **must** ignore the virtual environment folder and other generated files to avoid bloating your repository with unnecessary binaries.

Add the following content to your `.gitignore` file:

```gitignore
# Virtual Environment
venv/
env/
.env

# Python compilation cache
__pycache__/
*.py[cod]

# Distribution / Packaging
dist/
build/
*.egg-info/

# IDE settings
.vscode/
.idea/
```
