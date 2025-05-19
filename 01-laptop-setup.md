# Laptop Setup (Python, VS Code, and Notebooks)

Sciware recommends [uv](https://docs.astral.sh/uv/) Python. For notebooks, we recommend Jupyter notebooks in VS Code.
For Windows users, we recommend Windows Subsystem for Linux (WSL).
Here's how to set these up on your laptop.

> [!TIP]
> uv has fantastic [documentation](https://docs.astral.sh/uv), and a [dedicated guide](https://docs.astral.sh/uv/guides/integration/jupyter/)
> for using it with Jupyter notebooks. Check the documentation if you run into a problem!

## Windows Users: Install WSL
If you have a Windows laptop, start by installing the Window Subsystem for Linux (WSL). This will give you a fully-fledged
Linux terminal to use, and it integrates nicely with VS Code.  Microsoft has great [installation instructions](https://learn.microsoft.com/en-us/windows/wsl/install),
which these days usually boils down to a single command: `wsl --install`. If you get stuck, reach out to the [#code-help](https://simonsfoundation.enterprise.slack.com/archives/C08SZK2C0TB) channel on Slack.

## Python Setup
Let's set up Python using uv. If you haven't installed uv before, open a terminal, and run the following command to download and install uv:

```console
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**WSL Users**: run that command in a WSL terminal (Start Menu -> WSL)

Restart your shell, then run `uv --version`. If you see a version number, you're all set!

If you get stuck, check the [uv installation instructions](https://docs.astral.sh/uv/getting-started/installation).

## VS Code Setup
Go to the VS Code website and choose the installer (Windows, Mac, or Linux) for your laptop: https://code.visualstudio.com/download

Run the installer and follow the instructions.

**WSL Users**: For users with Windows laptops who are using WSL (Windows Subsystem for Linux), make sure you download the **Windows** installer, not the Linux one.

## Start a Python project
These instructions are adapted from uv's ["Working on projects"](https://docs.astral.sh/uv/guides/projects/) docs.

**WSL Users**: start by opening VS Code, then connect to WSL by pressing `F1` then `WSL: Connect to WSL`

Open a terminal in VS Code, and run the following to create a project and open the project directory as a VS Code "workspace":

```console
uv init summer-2025
code summer-2025
```

Now open a VS Code terminal and try adding a dependency. Instead of `pip install` use `uv add`:
```console
uv add numpy
```

Check the `pyproject.toml` file, and you'll see uv has added NumPy as a dependency!

Make a new file (e.g. `science.py`) and start writing code that uses your new dependency. To run the script, use:
```console
uv run science.py
```

With uv, you'll usually use `uv run script.py` instead of `python script.py`. Doing so ensures your virtual environment is always in sync with your project dependencies.

Once you've added a dependency or used `uv run`, there will be a virtual environment in the `.venv` directory. Make sure VS Code finds this directory with `F1 -> Python: Select interpreter`.

For creating more complicated Python projects, like a package that will be published on GitHub or PyPI, we recommend reading about uv's "packaged applications" and "libraries" concepts: https://docs.astral.sh/uv/concepts/projects/init/.

## Using Notebooks

These instructions are adapted from uv's ["Using Jupyter from VS Code"](https://docs.astral.sh/uv/guides/integration/jupyter/#using-jupyter-from-vs-code) docs.

If not already done, create a project on the terminal, and open it in VS Code:

```console
uv init summer-2025
code summer-2025
```

Add ipykernel as a dev dependency:

```console
uv add --dev ipykernel
```

Make sure VS Code has selected the virtual environment as the interpreter: `F1 -> Python: Select interpreter`, then select the `.venv` in the current directory.

Create a new notebook with `F1 -> Create: New Jupyter Notebook`, then click `Select kernel` in the top right, and choose `Python environments...`, then select the `.venv` in the current directory.

Done! Now your notebook should work. To add a new dependency, like NumPy, run `uv add numpy` from the command line and it will be available in your notebook.
