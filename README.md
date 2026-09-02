# Intro to AI — DAVE3625, Høst 2026

Lab repository for **DAVE3625** at OsloMet.

[Course description on student.oslomet.no](https://student.oslomet.no/en/studier/-/studieinfo/emne/DAVE3625/2025H%C3%98ST)

> **This repo is a work in progress.** We update the labs during the semester — tasks and topics can change. Get the latest version at the start of every lab week.

## Getting started

**New here? Read [Help/navigating-the-repo.md](Help/navigating-the-repo.md) first** — it explains how the labs are laid out and how to work through one.

1. **Get the files onto your laptop.** They are not there until you do this.

   *Recommended* — clone once, then `git pull` before each lab:
   ```bash
   git clone https://github.com/DAVE3625/Dave3625-Host-2025.git
   ```
   *Or* — click the green **`< > Code`** button above → **Download ZIP** and unzip it. No Git needed, but you re-download each time we update.

2. Install [VS Code](https://code.visualstudio.com/) with the **Python** and **Jupyter** extensions.
3. In VS Code, **File → Open Folder** and pick **that week's lab folder** — `Lab0`, not the repo root. This keeps your terminal in the right place for the setup step.
4. Start with [Lab 0](Lab0/README.md). It sets up your Python environment with UV.

**Each lab is its own UV project with its own `.venv`.** Every lab README has a Setup section — run it before you start that lab.

Working in a notebook we ship, like `Pandas.ipynb`? Make a copy first and name it `my-pandas.ipynb`, so a later `git pull` doesn't conflict with your edits.

## Labs

| Lab | Topic | Session |
|-----|-------|---------|
| **[Lab 0](Lab0/README.md)** | Environment setup with UV + Python basics | Hosted |
| [Lab 1](Lab1/README.md) | Intro to Python — reference notebook | **Self-study (optional)** |
| **[Lab 2](Lab2/README.md)** | Pandas and data wrangling | Hosted |
| [Lab 3](Lab3/README.md) | Feature engineering (Titanic) | Hosted |
| [Lab 4](Lab4/README.md) | Regression | Hosted |
| [Lab 5](Lab5/README.md) | KNN and SVM (wine quality) | Hosted |
| [Lab 6](Lab6/README.md) | Decision trees, random forest, naive Bayes | Hosted |
| [Lab 7](Lab7/README.md) | LLMs and prompt engineering (slide deck) | Hosted |
| [Lab 8](Lab8/README.md) | Running a Norwegian LLM — **runs in Colab, not locally** | Hosted |
| [Mandatory Assignments](Mandatory%20Assignments/) | MA1 and MA2 | — |

> **Lab 1 is not run in a session.** It is a Python/Jupyter reference for anyone who wants it — read it before Lab 2 if you are new to Python, or come back to it when you get stuck. The hosted sequence goes **Lab 0 → Lab 2**.

## Help

| Guide | What it covers |
|-------|----------------|
| [Help/navigating-the-repo.md](Help/navigating-the-repo.md) | **Start here.** How a lab is laid out and how to work through one |
| [Help/git.md](Help/git.md) | Cloning the repo and pulling updates |
| [Help/uv-cheatsheet.md](Help/uv-cheatsheet.md) | Setting up a lab environment, and the UV commands you need |
| [Help/uv-troubleshooting.md](Help/uv-troubleshooting.md) | When the kernel won't show up in VS Code |

## License

Distributed under the MIT License.
