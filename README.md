# ictp-3268-data-science

This repository contains teaching material used and developed for [Workshop on Rapid Prototyping of Internet of Things Solutions for Science](http://indico.ictp.it/event/8641/overview and http://wireless.ictp.it/school_2019/) workshop at the [International Center for Theoretical Physics (ICTP)](https://www.ictp.it/) in January 2019.


## Setting up Miniconda for hands-on sessions
Miniconda can be downloaded here: https://conda.io/en/latest/miniconda.html

Miniconda comes with a very useful command line tool to manage isolate environments and install package. The "Conda cheatsheet" should cover most of your needs https://conda.io/projects/continuumio-conda/en/latest/_downloads/1f5ecf5a87b1c1a8aaf5a7ab8a7a0ff7/conda-cheatsheet.pdf

Once miniconda installed, open a terminal/console/...:

1. List available environments: `conda env list` (you should have only the 'base' environment)
2. Install jupyter-notebook: `conda install jupyter`
3. Create a new isolated environment, actually cloning the base one: `conda create --name datascience-base --clone base`
4. Activate the newly created environment: `source activate datascience-base` (`source` only required for macosx - tbc)
5. Install required packages: `conda install pandas numpy matplotlib`

## [Optional]Running a Jupyter Notebook presentation
There is a neat way to create presentation from Jupyter notebooks:

1. In a Jupyter notebook, navigate `View ▶ Cell Toolbar ▶ Slideshow`
2. Then render it with: `jupyter-nbconvert --to slides name-of-your-presentation.ipynb --reveal-prefix=reveal.js --post serve`
