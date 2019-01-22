## Miniconda setup
Miniconda can be downloaded here: https://conda.io/miniconda.html

Miniconda comes with a very useful command line tool to manage isolate environments and install package. The "CONDA CHEAT SHEET" should cover most of your needs https://conda.io/docs/_downloads/conda-cheatsheet.pdf

Once miniconda installed, open a terminal/console/...:

1. List available environments: `conda env list` (you should have only the 'base' environment)
2. Install jupyter-notebook: `conda install jupyter`
3. Create a new isolated environment, actually cloning the base one: `conda create --name datascience-base --clone base`
4. Activate the newly created environment: `source activate datascience-base` (`source` only required for macosx - tbc)
5. Install required packages: `conda install pandas numpy matplotlib`

## Running a Jupyter Notebook presentation
There is a neat way to create presentation from Jupyter notebooks:

1. In a Jupyter notebook, navigate `View ▶ Cell Toolbar ▶ Slideshow`
2. Then render it with: `jupyter-nbconvert --to slides name-of-your-presentation.ipynb --reveal-prefix=reveal.js --post serve`
