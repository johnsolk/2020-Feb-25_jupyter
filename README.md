# 2020-Feb-25_jupyter

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/johnsolk/2019-Feb-25_jupyter/master)

# Intro

[Jupyter](https://jupyter.org/) notebooks started as IPython (interactive Python) notebook. This is why the file extension of the notebooks is `.ipynb`. You can use Jupyter notebooks for Python coding in addition to [many other languages, including R](https://jupyter.org/try).

Jupyter notebooks allow you to see and save output rendered directly below the code. This is different than other interactive developer environments (IDE) where the code is stored in a separate file and the output is rendered separately.

Motivation:
* Save analyses, keep code and output rendered in a single document
* Tutorials

# Objectives:

Today, we will:

* Load an existing notebook file
* Export
* Start a new notebook file
* (Optional) install jupyter notebook locally

# Load an existing notebook file

1. Click on the [mybinder](https://mybinder.org/) link below:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/johnsolk/2019-Feb-25_jupyter/master)

Click on the 'Build logs' to show what is being installed.

2. Open Terminal to install scanpy:
```
git clone https://github.com/theislab/scanpy.git
cd scanpy
pip install --user .
```

3. Open notebook file.
4. Run commands.

# Export

Click on the 'File' menu, select 'Download as'. There are several options. I use .pdf, .html, and .ipynb. These are the easiest to share with other people. Only the .ipynb will be executable for others.

# Start a new notebook file

1. Start a new Python 3 notebook file.

2. Copy/paste:

```


```
If you try to run the above, you can't because `` is not intalled.

To install it, run this:
```
!pip install
```

## RStudio:

Running [RStudio](https://github.com/binder-examples/dockerfile-rstudio) through binder:

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/v2/gh/binder-examples/dockerfile-rstudio/master)

Click [here for instructions on how to run an R Jupyter notebook with binder](https://github.com/binder-examples/r).

# (OPTIONAL) install jupyter notebook locally

Install Miniconda, a smaller version of conda. (doesn't install everything, just basic dependencies)

```
wget -O ~/miniconda.sh https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
bash ~/miniconda.sh -b -p $HOME/miniconda
source ~/miniconda/bin/activate
```
Create environment:
```
conda create -y -n py3.jupyter jupyter
```
Activate:
```
conda activate py3.jupyter
```
Install scanpy:
```
git clone https://github.com/theislab/scanpy.git
cd scanpy
pip install --user .
```
Add to path:
```
export PATH=/home/ljcohen/.local/bin:$PATH
```
Install dependencies:
```
pip install numpy scipy pandas matplotlib seaborn SpatialDE louvain python-igraph
```
