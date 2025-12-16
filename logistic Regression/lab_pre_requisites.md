# Lab Environment Setup Instructions

Welcome to the lab! Before you begin, you need to set up your Python environment with the necessary dependencies. Follow the instructions below to ensure everything is installed properly.

## Step 1: Install Python
Make sure Python 3.8 or above is installed on your system. You can check your current version by running the following command in your terminal/command prompt:

```
python --version
```

If Python is not installed, download it from the official Python website: https://www.python.org/downloads/

## Step 2: Set up Project

1. Make a folder with relevant name
2. Open the folder in `Vscode` or your choice of text editor/IDE. 

## Step 3: Create a New Python Environment

It's recommended to use a virtual environment to manage dependencies for this lab. Follow these steps to create a new environment:

**1. Create a new environment:**
```
python -m venv <name-of-the-env>
```
for example: 
```
python -m venv lab_env
```
This will create a folder called lab_env with a clean Python environment.

Note: Please use a good name, so that you do not get confused in the future. 

Examples of some bad names: 
- myenv
- env
- venv
- lol
- test


**2. Activate the environment:**

- On macOS/Linux:
```
source lab_env/bin/activate
```

- On Windows:
```
lab_env\Scripts\activate
```
Once activated, your terminal prompt should change to indicate you’re in the virtual environment.

for example: 
```
>>> (lab_env) D:\Repos\AI_Practical_ACEM>
```


## Step 4: Install the Dependencies

Next, you need to install the libraries required for the lab. Run the following command to install them:
```
pip install pandas numpy matplotlib seaborn scikit-learn

```

This will install the following dependencies:

- `pandas` (for data manipulation)
- `numpy` (for numerical computations)
- `matplotlib` (for plotting and visualization)
- `seaborn` (for statistical data visualization)
- `scikit-learn` (for machine learning datasets)


## Step 5: Create a Jupyter Notebook File

1. Create a new file with an extention `.ipynb` with relevant name. 
2. Open the file. 
