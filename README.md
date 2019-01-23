# ictp-3268-data-science

This repository contains teaching material used and developed for the **Workshop on Rapid Prototyping of Internet of Things Solutions for Science** (http://indico.ictp.it/event/8641/overview and http://wireless.ictp.it/school_2019/workshop) at the [International Center for Theoretical Physics (ICTP)](https://www.ictp.it/) in January 2019.

![Poster](lectures/img/poster.png)

## I. Setting up Miniconda and your virtual environment
Miniconda can be downloaded here: https://conda.io/en/latest/miniconda.html (Python 3.7 version).

Miniconda comes with a very useful command line tool to manage isolate environments and install package. "Conda cheatsheets" are available and will cover most of your daily needs:
- https://conda.io/projects/continuumio-conda/en/latest/_downloads/1f5ecf5a87b1c1a8aaf5a7ab8a7a0ff7/conda-cheatsheet.pdf
- https://kapeli.com/cheat_sheets/Conda.docset/Contents/Resources/Documents/index

### 1. The easy way
Once Miniconda installed, open a terminal:

1. Load already created virtual environment: `conda env create -f ictp-3268.yml`
2. Activate the newly created environment: `source activate ictp-3268` (`source` only required for macOS & Linux)

### 2. Doing it from scratch [Optional]
Once Miniconda installed, open a terminal:

1. List available environments: `conda env list`
2. Install "Jupyter notebook" globally: `conda install jupyter`
2. Create a new virtual environment named "ictp-3268": `conda create --name ictp-3268`
3. Activate the newly created environment: `source activate ictp-3268` (`source` only required for macOS & Linux)
4. Make virtual env. visible/switchable from Jupyter notebook: `conda install nb_conda`
5. Install required packages: `conda install pandas numpy matplotlib scipy`
6. Save current environment to a file: `conda env export > ictp-3268.yml`
7. Then to load an environment from that file a.k.a "The easy way": `conda env create -f ictp-3268.yml` (This is particularly convenient to make your data science pipeline reproducible).

## II. Launching Jupyter Notebook with created virtual environment
1. In a terminal (with "ictp-3268" not activate), launch Jupyter Notebook: `jupyter-notebook``
2. Once Jupyter Notebook fires up in your browser, select (click on) a notebook of interest (.ipynb extensions) and;
3. Switch to the kernel created for your virtual environment of interest (in our case "ictp-3268") by selecting on Notebook's top menu `Kernel` &#9658; `Change kernel` &#9658; `ictp-3268` 

## III. Useful Jupyter notebook keyboard shorcuts
Preliminary note: Cells should be run sequentially from top to bottom as the latter would rely on the former.

* Create cell (after current one): `Esc + b`
* Create cell (before current one): `Esc + a`
* Switch from code cell to markdown cell: `Esc + m`
* Switch from markdown cell to code cell: `Esc + y`
* Delete cell: `Esc + x`
* Run cell: `Shift + Enter`

To edit a markdown cell (if not in editing mode already): `double-click on it`
