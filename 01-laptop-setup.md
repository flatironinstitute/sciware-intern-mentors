# Environment Setup

Sciware recommends [uv](https://docs.astral.sh/uv/) Python and Jupyter notebooks in VS Code.
Here's how to set that up on your laptop.

> [!TIP]
> uv has fantastic [documentation](https://docs.astral.sh/uv), and a [dedicated guide](https://docs.astral.sh/uv/guides/integration/jupyter/)
> for using it with Jupyter notebooks. Check the documentation if you run into a problem!

## Python Setup
First, let's set up Python using uv.

Open a terminal, and run the following command to download and install uv:

```console
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Restart your shell, then run `uv --version`. If you see a version number, you're all set!

If you get stuck, check the [uv installation instructions](https://docs.astral.sh/uv/getting-started/installation).

## VS Code Setup
Go to the VS Code website and choose the installer (Windows, Mac, or Linux) for your laptop: https://code.visualstudio.com/download

**WSL Users**: For users with Windows laptops who are using WSL (Windows Subsystem for Linux), make sure you download the **Windows** installer, not the Linux one.

## Start a Python project

These instructions are adapted from uv's ["Using Jupyter from VS Code"](https://docs.astral.sh/uv/guides/integration/jupyter/#using-jupyter-from-vs-code) instructions

Create a project on the terminal, and open it in VS Code:

```console
uv init summer-2025
cd summer-2025
uv add --dev ipykernel
code .
```

To add a package (like NumPy) to the project, open a terminal and run

```console
uv add numpy
```
