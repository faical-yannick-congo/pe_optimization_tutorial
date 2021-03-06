Basic Python Optimization Tutorial
==================================
In this tutorial, we will explore a number of different acceleration approaches
and libraries for Python code. We will use a real-world science example to do 
this, namely the potential energy calculation from a molecular simulation. This 
example is simple enough for those not familiar with molecular simulation, but 
still a performance critical chunk of real simulation codes. Can we optimize 
this calculation in a language that is not known for runtime performance?

Goals
-----
- Explore a number of different code runtime optimization paradigms and 
toolsets in Python
    - Numpy
    - Numba
    - Cython
    - Dask
- Demonstrate the programming idioms of these libraries and tools
- Compare runtime vs memory optimization and the tradeoffs
- Expose the audience to various code profiling tools and techniques:
    - prun
    - memory_profiler
    - Snakeviz
    - Cython-Python interaction profiling
- Demo other useful Python libraries and tools:
    - Jupyter Notebooks
    - Bokeh
    - Holoviews
    - Pandas

**Disclaimer**
The author of this repo isn't necessarily an expert in *all* of these 
toolsets. If you have improvements or suggestions, please submit an issue
or pull request.

Setup
=====
This document explains how to get your computer set up for the
tutorial, including how to install the software libraries.

Step 1: Clone this repo
-----------------------

- Any Linux, Mac OS X, or Windows computer with a web browser should work.  We recommend Chrome, but typically also test Firefox and Safari.
- Clone this repository, e.g. using ```git clone https://github.com/martintb/pe_optimization_tutorial.git```
- Open a terminal window inside the repository.


Step 2: Create a conda environment from ``environment.yml``
-----------------------------------------------------------

The easiest way to get an environment set up for the tutorial is
installing it using the ``environment.yml`` we have provided. If you
don't already have it, install [conda](https://www.continuum.io/downloads),
and then create the ``peopt`` environment by executing::
```
   > conda env create -f environment.yml
```
When installation is complete you must activate the environment. If you
are on Windows:
```
   > activate peopt
```
If you are using OSX/Linux:
```
   $ source activate peopt
```

Later, when you are ready to exit the environment after the tutorial, you can type:
```
   > deactivate
```
If for some reason you want to remove the environment entirely, you can do so by writing:

```
   > conda env remove --name peopt
```


Step 3: Launch Jupyter Notebook
-------------------------------

You can then launch the notebook server and client:
```
   (peopt)> jupyter notebook 
```
A browser window with a Jupyter Notebook instance should now open, letting
you select and execute each notebook. If it does not open, there may be a link
that appears in your terminal that you should copy and paste into your browser.

Credits
-------
This style and layout of this tutorial was adapted from:
https://github.com/ioam/scipy-2017-holoviews-tutorial
