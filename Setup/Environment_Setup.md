# Machine Learning Environment Setup

This note documents a step-by-step how-to steps of setup my machine learning environment based on TensorFlow.

Last updated date: July 27th, 2023

# Platform

## Hardware
-CPU: intel i5-13600k<br />
-GPU: RTX-3060 with 12G-byte RAM<br />
-System RAM: 16G-byte<br />
-Hard Drive: 1T-Byte M2 SSD<br />

## Operation System:
-Windows 10<br />

# Setup Steps

## Install Python and Python tools

### Python Installation

Though the most certification Python version of TensorFlow is up to v3.9, but it seems okay to install the most updated Python version; Python version V3.11 is installed in my environment and seems working properly.

_Note: TensorFlow requires the developer to use Python version V3.6 or above for TensorFlow 2. Details can be found in this [page](https://www.tensorflow.org/install)_

The most updated Python can be found and download in [Python Download page](https://www.python.org/downloads/)

After the installation, check if the Python is available by checking its version with the following command:
```
python --version
```
You should be able to see the Python version echo in your command prompt if it is installed properly.

### Upgrade pip

It is required to upgarde the pip to the most updated version, use the following command to make it upgrade to the most updated version:
```
python -m pip install --upgrade pip
```

Similiar with how-to checking Python version, the version of pip can be also checked by using the command:
```
pip --version
```

_Note: TensorFlow requires the developer to use pip version above V19.0 (in Windows) or 20.3 (in macOS) for TensorFlow 2. Details can be found in this [page](https://www.tensorflow.org/install)_

### Install matplotlib

Matplotlib is a visualization library for Python, it is a useful tool for creating visualizations interface in Python, here is the command of how to install it:
```
pip install matplotlib
```

For detail information of matplotlib can be found in the [Matplotlib official website](https://matplotlib.org/)

### Install Jupyter Notebook

Jupyter notebook is a free and open standards for interactive compution across all programming languages and it is a flexible tool allows users to configur and arrange workflows in data science, scientific computing and machine learning, here is the command of how to install it:

```
pip install jupyter
```

Detail information about Jupyter can be checked in [Jupyter official website](https://jupyter.org/)

