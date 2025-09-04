# Tutorial: Using the `uv` Package Manager to Run Your Python Project

This tutorial will guide you through setting up a Python project using the `uv` package manager and running the code in `main.py`. Here, you will be creating an application to load a textfile and then to parse it for words that are entered at the command line. Please follow these steps to get started.

---

## Create a New Project Environment

Navigate to your repository project's main folder in the terminal. Note, if you were just completing the previous tutorial, you will want to back out of that directory to go to the other one.

In the main (root) directory of your repository, locate the working directory for this project: `wordSearch/`. The source files that you are to edit will also exist. If you were to create the directory yourself, the commands to create it and to initialize the project are shown below for clarity.

```sh
mkdir wordSearch
cd wordSearch
```

Now, create a new virtual environment using `uv`:

```sh
uv venv
```

This will set up a virtual environment in your project folder.

## Activate the Environment

Activating a virtual environment means that your terminal will only have access to the library packages that you installed when you created the virtual environment. To activate the environment, run the following command.

```sh
source .venv/bin/activate
```

You should see your prompt change, indicating the environment is active.

## Write the Python Application

Locate the file `uv_word_search/main.py` and add the following code. **Be careful to copy and paste the code exactly as shown!**

```python
# Note: To execute this code use the command
# uv run main.py data/ haiku.md house

import os
from rich import print, box
from rich.panel import Panel
from rich.table import Table
from rich.console import Console
import typer

app = typer.Typer()
console = Console()

def file_exists(file_path):
    """ DOCSTRING: TODO """
    return os.path.isfile(file_path)

def read_file(file_path):
    """ DOCSTRING: TODO """
    try:
        with open(file_path, "r", encoding="utf-8") as f:
            return f.read()
    except Exception as e:
    # TODO: Print a warning message if the file cannot be read
    # Example: print(f"Error reading file: {e}")
        return None

def count_word(content, word):
    """ DOCSTRING: TODO """
    return content.count(word)

def report_result(file_path, word, count):
    """ DOCSTRING: TODO """
    if count > 0:
        # TODO: Print a message showing the word was found File (file_path) and how many times (count)
        pass
    else:
        # TODO: Print a message showing the word was not found
        pass

@app.command()
def search(
    path: str = typer.Argument(..., help="Path to the directory containing the text file"),
    filename: str = typer.Argument(..., help="Name of the text file to search"),
    word: str = typer.Argument(..., help="Word to search for in the text file")
):
    """
    Search for a word in a text file and count its occurrences.
    
    Command: 
    uv run main.py data/ haiku.md house
   """
    # TODO: Print an example command showing how to run the script
    # Example: print("💡 Example: python main.py search data/ story.md house")

    file_path = os.path.join(path, filename)
    if not file_exists(file_path):
        # TODO: Print an error message if the file is not found
        # Example: print(f"File not found: {file_path}")
        raise typer.Exit(code=1)

    content = read_file(file_path)
    if content is None:
        raise typer.Exit(code=1)

    count = count_word(content, word)
    report_result(file_path, word, count)

if __name__ == "__main__":
    """ DOCSTRING: TODO """
    app()
```

## Install Required Packages

Your code requires the packages; `rich` and `typer` that help to format the output. We will use `uv` to install these packages. The general format to install a package.

```sh
uv pip install package_name
```

Replace `package_name` with the name of the package you need.

``` sh
uv pip install rich
uv pip install typer
```

## Run Your Code

With the environment activated, you can run your Python code in the UV packlage manager. Here we will load the file, `data/haiku.md` to search for the word `house`. To execute the command, enter the following command in your terminal.

```sh
uv run main.py data/ haiku.md house
```

## Add `print()` Statements, complete the TODOs, and Run Again

Before your code will run correctly, you need to add doc strings (e.g., comments to describe the actions of the functions in the code) and `print()` statements. The `TODO` sections of the code will draw your attention to these places to fix. 

Please add the necessary print statements to inform the user about the progress in the code. Once you have added doc strings and the `print()` statements, save your file and run the command again. Note: it is a good habit to add print statements in your code as you write it to help with debugging, and to determine what your code is doing at various stages of execution.

Rerun your code with the following command.

```sh
uv run main.py data/ haiku.md house
```

If all has gone well, you should see output indicating whether the word `house` was found in the File `haiku.md` and how many times it was found as well. The output will look similar to the following.

╭────────────────────── Search Result ───────────────────────╮
│ ✅ The word 'house' appears 2 times in 'data/haiku.md'. 🎉 │
╰────────────────────────────────────────────────────────────╯

## Try Testing with Other Words and Text Files

*Does your code function correctly, and as it is intended?*

You can test your code with other words and files. For example, you can search for the word `cheese` in the file `data/haiku.md` by running the following command.

```sh
uv run main.py data/ haiku.md cheese
```

To play with your code a bit, create other text files in the `data/` directory and test your code with those files as well.

## Step 5: Deactivate the Environment (Optional)

When you're done, you can deactivate the environment by running:

```sh
deactivate
```

## Summary

You are now ready to use `uv` for your Python projects!

## Next Steps

You are now ready to begin working on the writing part of this lab; `writing/reflection.md`. Please return to the main lab instructions in `README.md` to continue.
