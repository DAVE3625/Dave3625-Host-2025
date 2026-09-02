# Mini UV Cheatsheet

*Short reference for the UV commands used in this course. Every command here has been run against **uv 0.12.5** — if something behaves differently for you, check `uv --version` first.*

UV is a fast Python package and project manager. It replaces conda + pip + venv.
Full docs: [docs.astral.sh/uv](https://docs.astral.sh/uv/)

## Setting up a lab

**Each lab is its own project with its own `.venv`.** Do this once per lab:

```bash
cd LabN                    # the lab you are about to work on
uv init --bare             # creates pyproject.toml
uv add <packages>          # creates .venv and uv.lock, installs the packages
```

The package list is in each lab's README.

Then in VS Code, open the notebook and pick the kernel in the **top-right corner**. You are looking for `LabN/.venv`.

Stuck on the kernel? → [uv-troubleshooting.md](uv-troubleshooting.md)

### Two things that trip people up

- **`uv init` does not create `.venv`.** Only `pyproject.toml` appears. The `.venv` folder and `uv.lock` show up on your first `uv add` (or `uv sync`). This is normal, don't go looking for `.venv` too early.
- **Check what folder you are in.** If a `pyproject.toml` exists in a *parent* folder, UV quietly attaches your lab to that project instead of making a new one, and you end up with the wrong kernel. Run `uv init` from inside the lab folder, not from the repo root.

If you re-run `uv init` in a folder that already has one, you get:
`error: Project is already initialized`. That is fine, it means you are already set up.

### Why `--bare`?

Plain `uv init` also builds a `src/` package layout with a `[build-system]` and a script entry point. That is for shipping a library. For a notebook lab you only need the dependency list, which is what `--bare` gives you.

## Installing

| What | Command |
|------|---------|
| Install UV — macOS/Linux | `curl -LsSf https://astral.sh/uv/install.sh \| sh` |
| Install UV — macOS via Homebrew | `brew install uv` |
| Install UV — Windows | `powershell -c "irm https://astral.sh/uv/install.ps1 \| iex"` |
| Check it worked | `uv --version` |
| Update UV | `uv self update` (standalone installer only — with Homebrew use `brew upgrade uv`) |

If `uv` is not recognized after installing, restart your terminal.

## Packages

| What | Command |
|------|---------|
| Add a package | `uv add pandas` |
| Add several | `uv add pandas numpy matplotlib` |
| Pin a version | `uv add "pandas==2.2.3"` |
| Remove | `uv remove pandas` |
| Reinstall a broken package | `uv add --reinstall matplotlib` |
| List what is installed | `uv pip list` |
| Show the dependency tree | `uv tree` |

## Project

| What | Command |
|------|---------|
| Install everything from `pyproject.toml` / `uv.lock` | `uv sync` |
| Run a command inside the project env | `uv run python script.py` |
| Update the lockfile | `uv lock` |

`uv sync` makes the environment match the lockfile exactly, it also **removes** packages that are not listed as dependencies. It does not "activate" anything; you rarely need to activate at all, since `uv run` and the VS Code kernel picker handle it.

If you do want an activated shell:

```bash
source .venv/bin/activate      # macOS / Linux
.venv\Scripts\activate         # Windows, cmd
.venv\Scripts\Activate.ps1     # Windows, PowerShell
```

## Python versions

| What | Command |
|------|---------|
| Install a Python version | `uv python install 3.12` |
| List available versions | `uv python list` |
| Pin the version for this project | `uv python pin 3.12` |

Pinning writes a `.python-version` file. Lab 0 ships one (3.12) so everyone gets a Python new enough for `match` / `case`.

## When things go wrong

| What | Command |
|------|---------|
| Clear the cache | `uv cache clean` |
| Start the environment over | delete `.venv`, then `uv sync` |
