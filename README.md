# unstructured-mesh-parcels-sandbox

## Notebooks

* [Review of Particle Pushing on Unstructured Grids](./notebooks/Particle-pushing.ipynb)
* [Exploring ICON Mesh IO with UXArray](./notebooks/UXArray-ICON2.ipynb)
* [Exploring FESOM2 Mesh IO with UXArray](./notebooks/UXArray-FESOM2.ipynb)
* [Exploring PanGeo PyInterp and UXArray with ICON data](./notebooks/PanGeo-PyInterp-ICON.ipynb)

## Getting started
To work through the notebooks on your own system, we recommend setting up a conda environment and running notebooks within that environment.

To install miniconda on Linux

```
https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
```

For complete instructions and other distributions, see https://docs.anaconda.com/miniconda/miniconda-install/

> [!NOTE] The pyinterp package requires
> 
> * A 2017 compliant C++ compiler
> * Boost C++ libraries
> * Eigen3
> 
> It is recommended to install BLAS (e.g. libopenblas-dev). I have found that pyinterp fails to install due to a bug in the pyinterp CMake build system; when BLAS is not found, the library "FALSE" (which does not exist) is added to the linker libraries. 
> 
> On debian-based platforms, these can be installed using
> 
> sudo apt-get install g++ cmake libeigen3-dev libboost-dev libopenblas-dev
> See the [PyInterp docs[(https://pangeo-pyinterp.readthedocs.io/en/latest/setup/build.html#requirements)] for more details.


Next, create the conda environment and install all necessary packages.


```
conda env create -f environment.yaml
conda activate uop_sandbox
```

Start jupyter-lab
```
jupyter-lab
```

