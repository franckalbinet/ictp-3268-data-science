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

## IV. Learning track
Monday morning's (Jan. 28th, 2019) presentation/lecture is available [here](./lectures). 

As regards, afternoon's hands-on session, the following learning track is proposed:

* **Step 1**: setup up your working environment (see above);
* **Step 2 [Optional]**: In case you need a Python primer for Data Science, you will find one [here](./hands-on-sessions/notebooks/0-python-language-essentials-for-data-science.ipynb);
* **Step 3**: Execute, modify and expand this [notebook](./hands-on-sessions/notebooks/2-time-series-visualization-python.ipynb) on Time Series Visualization;
* **Step 4 [Optional]**: Execute, modify and expand this [notebook](./hands-on-sessions/notebooks/3-mapping-buoys.ipynb) to learn how to map geographical data and visualize RSSI embedded on Buoys drifting in the Gulf of Trieste;
* **Step 5**: Fetch time series data of your nodes through the MQTT channel, visualize them and set up a quick and dirty anomaly detection.

https://playground.tensorflow.org/

* **Step 6 [Optional / Pro.]**: Access F. Chollet notebook on [Time Series Forecasting using Deep Learning techniques](https://github.com/fchollet/deep-learning-with-python-notebooks/blob/master/6.3-advanced-usage-of-recurrent-neural-networks.ipynb), set up a dedicated conda environment, execute and try to get the general idea. 

