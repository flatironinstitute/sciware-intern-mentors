# Jupyter Notebooks

## Outline
- notebooks useful for mixing plots, text, and code
- jupyter notebooks not good with git (from [here](https://www.reviewnb.com/git-jupyter-notebook-ultimate-guide)):
    - Notebook Git diffs are hard to review 
    - Resolving notebook merge conflict is painful
    - Large notebooks fail to render on GitHub 
    - Notebook code reviews & collaboration is tough
- in general, move towards using scripts / write modular code

links:
- https://myst-nb.readthedocs.io/en/latest/
- https://jupytext.readthedocs.io/en/latest/
- https://mybinder.org/
- https://nbviewer.org/
- https://nbdime.readthedocs.io/en/latest/
- https://github.com/flatironinstitute/sciware/tree/main/34_PyPackaging/demo
- https://colab.research.google.com/drive/18Ss-Khlv9-RJWM8ixQsLNWMaRxovT1S9?usp=sharing

## Text

Many scientists and students who use python are used to working with jupyter notebooks, which provide a nice way of mixing code, explanatory text, and plots. However, using git with jupyter notebooks and working on jupyter notebooks collaboratively present some challenges.

...

One way to get the benefits of git while using jupyter notebooks is to use [jupytext](https://jupytext.readthedocs.io/en/latest/) to write ["text notebooks"](https://jupytext.readthedocs.io/en/latest/text-notebooks.html), where the jupyter notebook is saved as a `.md` or `.py` file. Once `jupytext` is installed, you can interact with these files through `jupyter lab` as if they were a regular `.ipynb` file. The outputs are not saved to disk by default.

...
