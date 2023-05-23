# minitorch_static_2022
This repository store the current state (2023/04) of the original minitorch with several modifications.

## What's the difference?
- Use [Ruff](https://github.com/charliermarsh/ruff) to replace [flake8](https://github.com/PyCQA/flake8), [isort](https://github.com/PyCQA/isort), and [darglint](https://github.com/terrencepreilly/darglint).

   This is mainly because the owner archived [darglint](https://github.com/terrencepreilly/darglint) on Dec 16, 2022.
   
   And Ruff has a [plan to implement the functionality](https://github.com/charliermarsh/ruff/issues/458), so I decide to replace flake8 and isort at once.
   
   I add the `.pre-commit-config.yaml` and `ruff.toml` that allows us to utilize [pre-commit](https://pre-commit.com/) base on `setup.cfg`.
   
   But note that Ruff does not support some rules, so that you won't find them in the abovementioned Ruff configuration file.
   
   Here is the list of not supported rules:

    - [E203Whitespace before ':'](https://www.flake8rules.com/rules/E203.html)
    - [E266Too many leading '#' for block comment](https://www.flake8rules.com/rules/E266.html)
    - [W503Line break occurred before a binary operator](https://www.flake8rules.com/rules/W503.html)
    - [F812List comprehension redefines name from line n](https://www.flake8rules.com/rules/F812.html)
      
- I commented out all the code in `mlprimer.py` because it seems incomplete and will affect GitHub Actions.
