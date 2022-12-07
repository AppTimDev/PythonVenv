# Project demostrates how to use virtual environment in python
- virtualenv
- venv
- pipenv

---

## Environment:
- Windows 10
- Python 3.10.4
- pip 22.2.2
- virtualenv 20.17.1

---

## virtualenv
## For window version and installed python 3.11.0
### Create a virtual environment (python 3.11.0 installed)
virtualenv --python=3.11 venv

### activate the virtual environment
venv\Scripts\activate.bat

### Install python package
pip install requests

### Check the path of the virtual environmnet is added
echo %path%

### Virtual Environment (after installation above):
- Python 3.11.0
- pip 22.3.1

---

## pipenv (recommend)
### Create a virtual environment (python 3.10.4 installed)
pipenv --python 3.10

### activate the virtual environment
pipenv shell

### Install python package
pipenv install requests
pipenv install pytest --dev

### Run the python script (not enter virtual environment)
pipenv run python check.py

### Uninstall python package
pipenv uninstall request

### List the package dependency graph
pipenv graph

## Features of pipenv
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

### Check the version the package virtualenv
```python
virtualenv --version
pip show virtualenv
```

### List all the installed package of python
```python
pip list
```