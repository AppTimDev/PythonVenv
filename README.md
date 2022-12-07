# Project demostrates how to use virtual environment in python
- virtualenv
- venv (build-in)
- pipenv

---

## Environment:
- Windows 10
- Python 3.10.4
- pip 22.2.2
- virtualenv 20.17.1
- pipenv 2022.11.30

---

## virtualenv
## For window version and installed python 3.11.0
### Create a virtual environment (python 3.11.0 installed)
```cmd
virtualenv --python=3.11 venv
```

### activate the virtual environment
```cmd
venv\Scripts\activate.bat
```

### Install python package
```cmd
pip install requests
```

### Check the path of the virtual environmnet is added
```cmd
echo %path%
```

### Virtual Environment (after installation above):
- Python 3.11.0
- pip 22.3.1

---

## pipenv (recommend)
### Create a virtual environment (python 3.10.4 installed)
```cmd
pipenv --python 3.10
```

### activate the virtual environment
```cmd
pipenv shell
```

### Install python package
```cmd
pipenv install requests
pipenv install pytest --dev
```

### Run the python script (not enter virtual environment)
```cmd
pipenv run python check.py
```

### Uninstall python package
```cmd
pipenv uninstall request
```

### List the package dependency graph
```cmd
pipenv graph
```

## Some Features of pipenv, not list all
- Pipfile is used instead of requirements.txt
- You no longer need to use pip and virtualenv separately. They work together.

---

## Commands
### Check python version
```cmd
python --version
python -V
```

### Check pip version
```cmd
pip --version
pip -V
```

### Locate pip and the Python interpreter
```cmd
where pip
where python
```

### Export the installed package to requirements.txt
```cmd
pip freeze > requirements.txt
```

### Install the python packages
```cmd
pip -r requirements.txt 
```

### Install virtualenv
```cmd
pip install virtualenv
pip install virtualenv==20.17.1

```

### Install pipenv
```cmd
pip install pipenv
pip install pipenv==2022.11.30
```

### Check the version the package virtualenv and pipenv
```python
virtualenv --version
pip show virtualenv pipenv
```

### List all the installed package of python
```python
pip list
```