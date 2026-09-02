<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]




<!-- PROJECT LOGO -->
<br />
<h3 align="center">Dave3625 - Lab 0</h3>
<p align="center">
  <a href="https://github.com/DAVE3625/Dave3625-Host-2025/tree/main/Lab0">
    <img src="img/logo.png" alt="Environment Setup" width="auto" height="auto">
  </a>
  <p align="center">
    Set up your Python environment with UV, then write your first Python.
    <br />
    ·
    <a href="https://github.com/DAVE3625/Dave3625-Host-2025/issues">Report Bug</a>
    ·
    <a href="https://github.com/DAVE3625/Dave3625-Host-2025/issues">Request Feature</a>
  </p>
</p>


## About The Lab

Getting your tools working is the boring part, so we do it first and get it over with. By the end of this lab you will have VS Code running notebooks against a UV environment, and you will have written some basic Python.

You will repeat the setup steps once per lab. **Every lab is its own project with its own `.venv`**, so it is worth understanding them now.


## Before you start: get the lab files onto your machine

The labs live in this GitHub repo. **They are not on your laptop yet, you have to get them first.**

**Recommended:** clone once, then `git pull` before each lab to pick up our updates:

```bash
git clone https://github.com/DAVE3625/Dave3625-Host-2025.git
```

**Or** go to [the repo page](https://github.com/DAVE3625/Dave3625-Host-2025), click the green **`< > Code`** button → **Download ZIP**, and unzip it. No Git needed, but you re-download each time we update the labs.

Either way, unzip or clone somewhere you will find again, your Documents folder is fine. Then:

**In VS Code: File → Open Folder, and pick the `Lab0` folder** — not the whole `Dave3625-Host-2025` folder.

`Lab0` is a folder *inside* what you just downloaded. Opening it directly keeps your terminal in the right place for the setup below, and avoids creating a project at the top level by mistake.

> New to the repo? [Help/navigating-the-repo.md](../Help/navigating-the-repo.md) explains how every lab is laid out. Git questions → [Help/git.md](../Help/git.md).


## Part 0: Install your tools

We use **Visual Studio Code** in this course. You may use another IDE, but the TAs may not be able to help you debug it.

1. Install [Visual Studio Code](https://code.visualstudio.com/).
2. In VS Code, open the **Extensions** menu on the left and install the **Python** extension.
3. Install the **Jupyter** extension the same way.
4. Install **UV** — [installation docs](https://docs.astral.sh/uv/getting-started/installation/):

   ```bash
   # macOS / Linux
   curl -LsSf https://astral.sh/uv/install.sh | sh

   # Windows
   powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
   ```

5. Check it worked:

   ```bash
   uv --version
   ```

   Not recognized? Restart your terminal.


## Part 1: Set up the environment

Open a terminal in VS Code and run these **from inside the `Lab0` folder**:

```bash
cd Lab0
uv init --bare
uv add jupyter ipykernel
```

What each step does:

| Command | Result |
|---------|--------|
| `uv init --bare` | Creates `pyproject.toml` — your project's dependency list. **Nothing else appears yet.** |
| `uv add jupyter ipykernel` | Creates `.venv` and `uv.lock`, and installs the packages into `.venv`. |

> **Check your folder before running `uv init`.** If a `pyproject.toml` exists in a parent folder, UV attaches your lab to *that* project instead of creating a new one, and you will end up selecting the wrong kernel later.

Now create your notebook:

1. Make a new file called `lab0.ipynb`.
2. Open it and select the Python interpreter in the **top-right corner**. Pick the one under `Lab0/.venv`.

Can't find the environment? → **[Help/uv-troubleshooting.md](../Help/uv-troubleshooting.md)**

More UV commands → **[Help/uv-cheatsheet.md](../Help/uv-cheatsheet.md)**

> This folder ships a `.python-version` file pinning Python 3.12, so everyone gets a version new enough for Task 6.


## Part 2: Python exercises

Solve these in `lab0.ipynb`. Compare with [Solution.ipynb](Solution.ipynb) when you are done.

**Printable version:** [Lab-0-exercises.pdf](./Lab-0-exercises.pdf)

### Task 1: "Hello World!"

Write and run a program that prints `Hello World!`.

### Task 2: Basic arithmetic

Perform basic arithmetic operations in Python.

1. Write code to:
    - Add two numbers.
    - Multiply two numbers.
    - Divide one number by another.
2. Display the results of each calculation.

### Task 3: Variables

Learn to store and use values in variables.
1. Create variables to store a name and an age.
2. Print the values of the variables in a formatted string.

### Task 4: Simple loops

Use a loop to repeat an action multiple times.
1. Write a for-loop that iterates over a range of numbers.
2. In each iteration, print a line of text that includes the current iteration number.

### Task 5: Conditional statements

Implement decision-making in your code using if-else statements.
1. Write an if-statement that checks if a number is greater than 5.
2. Print a message based on whether the condition is true or false.

### Task 6: Match-case statements *(needs Python 3.10+)*

Learn to use Python's modern match-case syntax for pattern matching (Python 3.10+).
1. Create a variable holding a day of the week as a string, e.g. `"Monday"`.
2. Use a `match` / `case` statement to print:
   - `"Start of the work week!"` for Monday
   - `"Midweek already!"` for Wednesday
   - `"Almost weekend!"` for Friday
   - `"Weekend time!"` for Saturday or Sunday
   - `"Just another day"` for anything else
3. Test it with different days.

**Bonus:** make it handle both lowercase and uppercase input, e.g `"monday"` and `"Monday"`.


## Next

**Next session is [Lab 2](../Lab2/README.md) — Pandas and data wrangling.**

[Lab 1](../Lab1/README.md) is optional self-study: a Python and Jupyter reference notebook. Read it before Lab 2 if you are new to Python, or come back to it when you get stuck.


## License

Distributed under the MIT License. See `LICENSE` for more information.

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[issues-shield]: https://img.shields.io/github/issues/umaimehm/Intro_to_AI_2021.svg?style=for-the-badge
[issues-url]: https://github.com/DAVE3625/Dave3625-Host-2025/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/DAVE3625/Dave3625-Host-2025/blob/main/Lab0/LICENSE
