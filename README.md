# Project demostrates how to use virtual environments in python
1. virtualenv
2. venv (build-in) (Not demostrate)
3. pipenv (Recommend to use)

---

## Environment:
- Windows 10
- Python 3.11.3
- pip 23.1.2
- virtualenv 20.23.0
- pipenv 2023.4.29

---

## 1. Virtual environment (virtualenv)
## For window version and installed python 3.11
### 1a. Create a virtual environment (python 3.11 installed)
```cmd
virtualenv --python=3.11 venv
```

### 1b. activate the virtual environment
```cmd
venv\Scripts\activate.bat
```

### 1c. Install python package after activating the virtual environment
```cmd
pip install requests
```

### 1d. Check the path of the virtual environmnet is added
```sh
echo %path%
```
and test if the requests package is installed
```sh
python check.py
```

### Verison of the Virtual Environment venv (after installation above):
- Python 3.11.3
- pip 23.1.2

---

## 3. pipenv (recommend)
### 3a. Install pipenv
```sh
python -m pip install --upgrade pip
python -m pip install --upgrade pipenv
```

### 3b. Create a virtual environment (python 3.11 installed)
```sh
pipenv --python 3.11.3
```

### 3c. Install all python packages or specific packages (no need enter virtual environment)
```sh
pipenv install
pipenv install requests beautifulsoup4 html5lib
pipenv install pytest --dev
```

### 3d. Run the python script (no need enter virtual environment)
```sh
pipenv run python check.py
```

### Activate the virtual environment
```sh
pipenv shell
```

### Uninstall python package
```sh
pipenv uninstall requests
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
```sh
python -V
```

### Check pip version
```sh
pip -V
```

### Check the version the package pipenv
```sh
pip show pipenv
```

### List all the installed package of python
```sh
pip list
```

### Locate pip and the Python interpreter
```sh
where pip
where python
where pipenv
```

and sometimes it may be important to find the path of python interpreter using in the pipenv environment
#### Output Python interpreter, pip, pipenv  information of pipenv environment
```sh
pipenv run pip -V
pipenv --py
pipenv --version
```

#### Output virtualenv information.
```sh
pipenv --venv
```

#### Remove the virtualenv.
```sh
pipenv  --rm  
```                          

---

## Other Commands 
### Export the installed package to requirements.txt
```sh
pip freeze > requirements.txt
```
or package of pipenv environment to requirements.txt
```sh
pipenv run pip freeze > requirements.txt
```

### Install the python packages from requirements.txt 
```sh
pip -r requirements.txt 
```

or inside pipenv environment (not recommend)
```sh
pipenv run pip -r requirements.txt 
```

### Install virtualenv
```sh
pip install virtualenv
pip install virtualenv==20.23.0
```

### Install pipenv
```sh
pip install pipenv
pip install pipenv==2023.4.29
```

### Check the version the package virtualenv and pipenv
```sh
virtualenv --version
pip show virtualenv pipenv
```
