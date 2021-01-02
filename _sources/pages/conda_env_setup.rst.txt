========================================
Setting up a conda environment for ML/DL
========================================

Setting up an environment for Machine/Deep Learning can be annoying--with different versions of CUDA, cuDNN and PyTorch. Here’s a simple, no-hassle way to do it.

**Install Anaconda/Miniconda**

`Decide between <https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html#anaconda-or-miniconda>`_ Anaconda and Miniconda and install one of them by going to their downloads page.

* `Anaconda <https://www.anaconda.com/distribution>`_
* `Miniconda <https://docs.conda.io/en/latest/miniconda.html>`_

**Create a conda environment**

Once that’s done, create a conda environment. Let’s call it ``robosub``::

  conda create python=3.7 -n robosub

This creates a new environment that runs Python 3.7. Activate the environment using::

  conda activate robosub

You can deactivate it using::

  conda deactivate

**Installing CUDA, PyTorch and other common ML packages**

Run the following command (remember to activate your conda environment before doing this). This sets up PyTorch with a CUDA 10.1 compatible GPU.::

  conda install pytorch torchvision cudatoolkit=10.1 -c pytorch

You can find other variations of the installation (CPU only, older CUDA version, older PyTorch version etc.) on the `PyTorch website <https://pytorch.org/>`_.

Here are some commonly used packages in ML that you can optionally install. You’ll need them for working with the EdgeNets or ESPNetv2 code.::

  conda install -c conda-forge opencv pycocotools
  conda install tensorboard

References
----------
#. `<https://pytorch.org/>`_
#. `<https://www.anaconda.com/distribution/>`_
#. `<https://docs.conda.io/en/latest/miniconda.html>`_
#. `<https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html>`_
#. `<https://anaconda.org/conda-forge/opencv>`_
#. `<https://anaconda.org/conda-forge/pycocotools>`_












