# Finding your way around this repo

*New here? Read this once. It explains how every lab is put together, so you can find what you need without hunting.*

## This repo is a work in progress

We update the labs during the semester — tasks and even topics can change. **Get the latest version at the start of every lab week.** Don't assume the copy you grabbed in week 1 is still current.

## Reading a lab

Every lab is explained in its `README.md`. Two ways to read it, both fine:

* **On GitHub** — click into the lab folder in your browser. Images, tables and the collapsible task sections all render properly.
* **In VS Code** — open the `README.md` and press `Ctrl+Shift+V` (`Cmd+Shift+V` on Mac) for the preview. Without it you'll see raw markdown and wonder where the pictures went.

A lot of people read the lab page on GitHub and keep VS Code beside it for the code.

## Getting the files

### Recommended: clone once, pull weekly

```bash
git clone https://github.com/DAVE3625/Dave3625-Host-2025.git
cd Dave3625-Host-2025
```

Then before each lab, from inside that folder:

```bash
git pull
```

That's it — one command to be up to date. New to Git? See [git.md](git.md).

> **You can't break anything.** Cloning gives you a read-only copy. You do not have permission to push to this repo, so nothing you do locally affects anyone else.

### Alternative: download the ZIP

On the [repo page](https://github.com/DAVE3625/Dave3625-Host-2025), click the green **`< > Code`** button → **Download ZIP**, then unzip it.

No Git needed, but you have to re-download when we announce changes, and you redo each lab's setup in the new folder. GitHub only offers the whole repo as a ZIP — there's no way to download a single lab folder on its own.

### One rule that keeps `git pull` working

The walkthrough notebooks (like `Pandas.ipynb`) are part of the repo. If you type your own code into one and we later update it, your `git pull` will hit a conflict.

**So make a copy before you work in a notebook.** Name it `my-pandas.ipynb` or similar and leave the original alone — copies named `my-*.ipynb` are ignored by Git, so they'll never clash.

Already stuck with a refused pull? `git stash` parks your changes and lets the pull through.

## Open one lab folder at a time

Each week, in VS Code use **File → Open Folder** and pick **that week's lab folder** — `Lab2`, not the repo root.

This matters more than it sounds:

* Your terminal opens already inside the lab, so the setup step lands in the right place.
* If you open the root and run `uv init` there by mistake, you create a project at the top level. Every lab underneath silently becomes part of it, and the kernel picker starts showing the wrong environment. See [uv-troubleshooting.md](uv-troubleshooting.md) if this already happened to you.

## What you'll find in a lab folder

The same handful of file types show up everywhere:

| File | What it is |
|------|-----------|
| `README.md` | **Always start here.** What the lab covers, the setup step, and the tasks. |
| A topic-named notebook, e.g. `Pandas.ipynb` | The walkthrough your TA teaches from. **Not every lab has one** — see below. |
| `solution.ipynb` | The answer key. Have a go at the tasks first. |
| `Lab-N-exercises.pdf` | A printable version of the exercises, where we've made one. |
| `data/` | The CSV files the lab loads. Paths in the notebooks are relative, so **don't move files out of the lab folder.** |
| `img/` | Screenshots the README displays. You never need to open these yourself. |
| `pyproject.toml`, `uv.lock`, `.venv/` | **You create these yourself** when you run the lab's setup step. They are not in the download — that's normal, your copy isn't broken. |

## How to work through a lab

1. **Read the README.** It says what you're doing and why.
2. **Run the Setup section.** Every lab is its own project with its own `.venv`, so you do this once per lab. Commands are in [uv-cheatsheet.md](uv-cheatsheet.md).
3. **Follow the walkthrough** — in your own copy of the notebook. If the lab has no walkthrough notebook, the README *is* the walkthrough and the code is written inline; type it as you read.
4. **Do the tasks.**
5. **Compare with `solution.ipynb`.** After you've tried, not before.

### Two things that don't follow the pattern

* **Lab 1 is optional self-study.** It's a Python reference notebook with no tasks and no answer key — useful if you're new to Python or want to look something up later. The hosted sequence goes **Lab 0 → Lab 2**.
* **Some labs are a slide deck or a Colab notebook** instead of a README plus notebook. Lab 8 in particular runs in Google Colab on a GPU, not in a local `.venv`. Its README tells you what to do.

## Stuck?

| Problem | Where to look |
|---------|---------------|
| Kernel won't show up, wrong environment, `uv init` in the wrong folder | [uv-troubleshooting.md](uv-troubleshooting.md) |
| Which UV command do I need? | [uv-cheatsheet.md](uv-cheatsheet.md) |
| Cloning, pulling, general Git confusion | [git.md](git.md) |

Still stuck? Ask a TA in the lab session — that's what we're there for.
