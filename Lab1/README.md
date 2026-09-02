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
<h2 align="center">Dave3625 - Lab 1</h2>
<p align="center">
  <a href="https://github.com/DAVE3625/Dave3625-Host-2025/tree/main/Lab1">
    <img src="img/header.png" alt="Intro to Python" width="auto" height="auto">
  </a>

<h3 align="center">Intro to Python — reference notebook</h3>

<p align="center">
  <a href="https://github.com/DAVE3625/Dave3625-Host-2025/issues">Report Bug</a>
  ·
  <a href="https://github.com/DAVE3625/Dave3625-Host-2025/issues">Request Feature</a>
</p>


## ⚠️ This lab is optional self-study

**We do not run this lab in a session.** The hosted sequence goes **[Lab 0](../Lab0/README.md) → [Lab 2](../Lab2/README.md)**.

It is a reference notebook, not an exercise set — there are no tasks and no solution file. Use it if:

- You are new to Python or to Jupyter notebooks, and want to read through the basics before Lab 2.
- You get stuck on syntax later in the course and want to look something up.

Bookmark it. It is more useful as a lookup than as a read-through.

**[Open the notebook →](./python-intro.ipynb)**


## What's in it

| Section | Covers |
|---------|--------|
| Python program files | `.py` files, comments, running scripts |
| IPython notebooks | How notebook cells work |
| Modules | `import`, namespaces, exploring what a module contains |
| Variables and types | Naming, assignment, fundamental types, casting |
| Operators and comparisons | Arithmetic, boolean, comparison |
| Strings, lists and dictionaries | Indexing, slicing, string formatting, modifying lists, tuples, dicts |
| Control flow | `if` / `elif` / `else` |
| Loops | `for`, `while`, list comprehensions |
| Functions | Arguments, defaults, keyword args, `lambda` |
| Classes | Defining classes and methods |
| Exceptions | `try` / `except`, raising errors |

If you only read one part before Lab 2, read **Variables and types**, **Strings, lists and dictionaries**, and **Loops** — Lab 2 leans on all three.


## Setup

Only needed if you want to run the cells rather than just read them:

```bash
cd Lab1
uv init --bare
uv add jupyter ipykernel
```

Then select the `Lab1/.venv` kernel in the top-right corner of the notebook.

Stuck? → [Help/uv-troubleshooting.md](../Help/uv-troubleshooting.md) · [Help/uv-cheatsheet.md](../Help/uv-cheatsheet.md)


## Credit

This notebook is from **[Scientific Python Lectures](http://github.com/jrjohansson/scientific-python-lectures)** by J.R. Johansson, used under its original license.


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[issues-shield]: https://img.shields.io/github/issues/umaimehm/Intro_to_AI_2021.svg?style=for-the-badge
[issues-url]: https://github.com/DAVE3625/Dave3625-Host-2025/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/DAVE3625/Dave3625-Host-2025/blob/main/Lab1/LICENSE
