# Bare Minimum Tutorial: Building a Python Application with UV Package Manager

## Overview

In this part of the lab assignment, you will create a simple Python application that loads a CSV file containing integers, prints each integer along with its squared value. You will use the [UV package manager](https://github.com/astral-sh/uv) to manage the dependencies, and run an application using Python.

## Prerequisites

- Python installed (recommended: Python 3.8+)
- [UV package manager](https://github.com/astral-sh/uv) installed
- VS Code or your preferred editor

## Install The UV Package Manager

If you have not already installed UV yet, then go to the following url: [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/) and follow the instructions for your operating system.

---

### Part 1: The Number Squaring Application

## Create Your Project Directory

In the main (root) directory of your repository, use the following command to create a new working directory for this project. Note: your repository will already exist in the repository that you cloned from GitHub. The source files that you are to edit will also exist, however the commands to create the directory and initialize the project are shown here for clarity.

```sh
mkdir uv_csv_app
cd uv_csv_app
```

## Initialize a Python Project with UV

After you have cloned your GitHub repository, you will run the following command to initialize your project and create a virtual environment from your repository's local directory.

Activating a virtual environment means that your terminal will only have access to the library packages that you installed when you created the virtual environment. Using this command is good practice; here we do not add any new libraries yet for this application, but we will do so in the next tutorial.

Note: to see where you are in your terminal, you can type `pwd` in your terminal (MacOS or Ubuntu) to see your current directory. In Windows, you can type `cd` to see your current directory. Please be sure you are in the correct (local) directory before running the following commands.

To activate the environment, run the following commands.

```sh
uv venv
source .venv/bin/activate
```

---

## Add Dependencies

Your application will be loading a CSV (Comma Separated Variables) file to load some numbers to perform operations to square them and print output. For this, you will need the `pandas` package to read CSV files. Install it with UV with the following commands.

```sh
uv pip install pandas
```

---

## Create a CSV Data File

A CSV file called `numbers.csv` is necessary for this application and is located at following location: `uv_csv_app/numbers.csv`.

The contents of the file are as follows.

``` text
number
1
2
3
4
5
6
7
8
9
10
```

---

## Write the Python Application

Locate the file `uv_csv_app/main.py` and add the following code:

```python
import pandas as pd

# Load the CSV file
numbers = pd.read_csv('numbers.csv')

# Print each integer and its squared value
for n in numbers['number']:
    print(f"\t Number: {n}, Squared: {n**2}")
```

---

## Step 7: Run the Application

Run your application using UV.

```sh
uv run main.py
```

You should see output like the following.

``` text
Number: 1, Squared: 1
Number: 2, Squared: 4
Number: 3, Squared: 9
Number: 4, Squared: 16
Number: 5, Squared: 25
Number: 6, Squared: 36
Number: 7, Squared: 49
Number: 8, Squared: 64
Number: 9, Squared: 81
Number: 10, Squared: 100
```

---

## What Did You Accomplish?

You have built a Python application that reads integers from a CSV file and prints each integer with its squared value, using UV for dependency management.

For more on UV, visit the [UV documentation](https://github.com/astral-sh/uv).

## Next Steps

Once you have completed this mini tutorial, you can move on to the next `tutorial_02.md` which will guide you through creating a more complex application that uses additional libraries and features.

+ Next Tutorial: [tutorial_02.md](tutorial_02.md)
