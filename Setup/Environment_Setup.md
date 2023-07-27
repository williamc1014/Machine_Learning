# Machine Learning Environment Setup

This note documents a step-by-step how-to steps of setup my machine learning environment based on TensorFlow.

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

TensorFlow requires the developer to use Python version V3.8 (or above) with __64-bit__ system for TensorFlow 2. Details can be found in this [page](https://www.tensorflow.org/install)

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

## Install tool chain of Grapgics Processor 

### What is CUDA?
>Compute Unified Device Architecture (CUDA) is a proprietary and close closed parallel computing platform and application program interface (API) that allows software to use certian types of graphics processing units (GPUs) for general purpose processing, an approach called general-purpose computing on GPUs (GPGPUs). CUDA is a software layer that gives direct access to the GPU's virtual instruction set and parallel computational elements, for the execution of compute kernels. 

A more information of the general descrption of CUDA can be found in this [Wiki page](https://en.wikipedia.org/wiki/CUDA)
Check more information in this [CUDA home website](https://developer.nvidia.com/cuda-toolkit)

_CUDA is a proprietary software toolkit provided by NVIDIA therefore it is impossible to use this toolkit on any other graphics processors such as from AMD or Intel._

This online document [CUDA Installation Guide for Microsoft Windows](https://docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html) illustrates the installation instructions for the CUDA Toolkit on Microsoft Windows.

### Install Visual Stdio 

In this document _CUDA Installation Guide for Microsoft Windows_ it shows that CUDA the version 12.2 is supported by the following Visual Studio compilers:
- MSVC Version 193x (Visual Studio 2022 17.0) [Download Link](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false)<br/>
- MSVC Version 192x (Visual Studio 2019 16.0) [Download Link](https://my.visualstudio.com/Downloads?q=visual%20studio%202019&wt.mc_id=o~msft~vscom~older-downloads)<br/>
- MSVC Version 191x (Visual Studio 2017 15.0) [Download Link](https://my.visualstudio.com/Downloads?q=visual%20studio%202017&wt.mc_id=o~msft~vscom~older-downloads)<br/>

Download one of above Visual Studio software and install it. Be aware that as Python, C and C++ are the candidate language for machine learning developments later, the Python, C and C++ related components should be checked and installed in Microsoft Visual Studio Installer.

_Visual Studio should be installed ahead CUDA is installed as CUDA will search which Visual Studio software is installed in your PC and install the essential components._

### Install CUDA

Go to [CUDA download page](https://developer.nvidia.com/cuda-downloads) and download the CUDA Toolkit installer.
During the installation, DO NOT change the default installation path to avoid any path setting issue.

### Setup cuDNN

cuDNN (CUDA Deep Neural Network) 
>is a GPU-accelerated library of primitives for deep neural networks. It provides highly tuned implementations of routines arising frequently in DNN applications. These release notes describe the key features, software enhancements and improvements, and known issues for the NVIDIA cuDNN 8.9.3 and earlier releases.

Follows the instructions described in section 2 of this [NVIDIA CuDNN Document](https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html) to setup the cuDNN to the system and also the Visual Studio environments.

### Install Visual Studio Code

Visual Studio Code is a efficient IDE tool that we can rely on developments for various applications.
Go to [Visual Studio Code Downlosd page](https://code.visualstudio.com/download), download the installer and install it.

The launch Visual Studio Code and install the extensions of [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) and [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter).

## Install TensorFlow 

In Windows Command Prompt, use the command beneath to install TensorFlow:
```
pip install tensorflow
```

It should take a while to finish the download and installation.

# Hello World! 

The following instructions is intending to verifying if all the software, component and path variable are setup properly.

(1) Launch Visual Studio Code
(2) Add a new Juypter source file from File menu.
(3) Key-in the following code.
```
import tensorflow as tf
print('tensorflow version', tf.__version__)

x = [[3.]]
y = [[4.]]

print('Result: {}'.format(tf.matmul(x, y)))
```
(4) Click on Run button and you should be able to see the TensorFlow version and the calculation result as the example shown beneath.

_Make sure that you it is using the correct Python version which showing on the up-right corner to the code console area; it it is not, change it to the correct Python version in the setting. Refer to this document [Jupyter Notebooks in VS Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) for the details_
