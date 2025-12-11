---
layout: default
---

# Python Virtual Environment Guide

## What is a Virtual Environment?

A virtual environment is an isolated Python environment that allows you to install packages and dependencies specific to a project without affecting your system-wide Python installation. This is essential for managing different project requirements and avoiding dependency conflicts.

## Creating a Virtual Environment

### Basic Creation

```bash
python3 -m venv venv
```

This creates a new virtual environment in a directory called `venv`. You can name it anything you want:

```bash
python3 -m venv myenv
python3 -m venv .venv
python3 -m venv env
```

**Note:** `.venv` or `venv` are common conventions. Many IDEs automatically detect these names.

### Creating with Specific Python Version

If you have multiple Python versions installed:

```bash
python3.11 -m venv venv
python3.12 -m venv venv
```

## Activating the Virtual Environment

### On macOS/Linux

```bash
source venv/bin/activate
```

After activation, your terminal prompt will show the environment name:
```
(venv) user@computer:~/project$
```

### On Windows

**Command Prompt:**
```cmd
venv\Scripts\activate.bat
```

**PowerShell:**
```powershell
venv\Scripts\Activate.ps1
```

**Git Bash:**
```bash
source venv/Scripts/activate
```

## Deactivating the Virtual Environment

From any operating system, simply run:

```bash
deactivate
```

This returns you to your system's default Python environment.

## Reactivating the Virtual Environment

To reactivate, just run the activation command again:

**macOS/Linux:**
```bash
source venv/bin/activate
```

You can activate and deactivate as many times as needed.

## Working with Packages

### Installing Packages

Once activated, use pip to install packages:

```bash
pip install package_name
pip install requests
pip install numpy pandas matplotlib
```

### Viewing Installed Packages

```bash
pip list
pip freeze
```

### Creating a Requirements File

Save all installed packages to a file:

```bash
pip freeze > requirements.txt
```

### Installing from Requirements File

```bash
pip install -r requirements.txt
```

This is useful for sharing projects or setting up environments on different machines.

## Upgrading pip

It's good practice to upgrade pip in your new virtual environment:

```bash
pip install --upgrade pip
```

## Checking Which Python is Being Used

To verify you're using the virtual environment's Python:

```bash
which python    # macOS/Linux
where python    # Windows

python --version
```

## Deleting a Virtual Environment

Simply delete the venv directory:

```bash
rm -rf venv     # macOS/Linux
rmdir /s venv   # Windows
```

Then create a new one if needed.

## Best Practices

1. **Don't commit venv to git:** Add `venv/`, `.venv/`, or `env/` to your `.gitignore` file
2. **One venv per project:** Keep virtual environments separate for each project
3. **Use requirements.txt:** Always maintain a `requirements.txt` file for reproducibility
4. **Activate before installing:** Make sure your venv is activated before installing packages
5. **Update regularly:** Keep your packages updated with `pip install --upgrade package_name`

## Common Issues and Solutions

### Permission Errors on Windows PowerShell

If you get an execution policy error when activating on Windows PowerShell:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### Virtual Environment Not Activating

- Make sure you're in the correct directory
- Check that the venv directory exists
- Try recreating the virtual environment

### Wrong Python Version

If `python3 -m venv venv` uses the wrong Python version:
- Use the full path to the desired Python executable
- Or use `python3.x -m venv venv` with the specific version

### IDE Not Recognizing Virtual Environment

Most IDEs (VS Code, PyCharm) can select the interpreter:
- **VS Code:** Command Palette → "Python: Select Interpreter" → Choose your venv
- **PyCharm:** Settings → Project → Python Interpreter → Add Interpreter

## Quick Reference

```bash
# Create
python3 -m venv venv

# Activate (macOS/Linux)
source venv/bin/activate

# Activate (Windows)
venv\Scripts\activate

# Deactivate
deactivate

# Install packages
pip install package_name

# Save dependencies
pip freeze > requirements.txt

# Install dependencies
pip install -r requirements.txt

# Delete
rm -rf venv
```

## Additional Tools

### virtualenvwrapper

For managing multiple virtual environments more easily:

```bash
pip install virtualenvwrapper
```

### pyenv

For managing multiple Python versions:

```bash
brew install pyenv    # macOS
```

### poetry

Modern dependency management tool that handles virtual environments automatically:

```bash
pip install poetry
```

### conda

Alternative to venv, popular in data science:

```bash
conda create -n myenv python=3.11
conda activate myenv
conda deactivate
```

---

*Last modified: {{ page.last_modified_at | date: '%B %d, %Y' }}*
