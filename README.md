# okada4py
Okada implementation in Python

## Citation
This is a python implementation of the solution proposed by Okada in 1992. Please cite:

Okada, Y. (1992), Internal deformation due to shear and tensile faults in a half-space, Bulletin of the Seismological Society of America, 82(2), 1018–1040.

and this implementation: [![DOI](https://zenodo.org/badge/212802180.svg)](https://doi.org/10.5281/zenodo.14170826) 

[Dr Leah Langer](https://en-exact-sciences.tau.ac.il/profile/llanger) kindly implemented her receiver elevation correction to provide a first order correction of the effect of topography on the evaluation of Green's functions. If you use this, please cite (and read) this paper: [doi: 10.1016/j.tecto.2020.228566](https://doi.org/10.1016/j.tecto.2020.228566)

## Install okada4py:

This installation requires meson. Install meson and meson-python first (check it out with pip).

### Install on a local directory

```
meson setup builddir --prefix /My/complete/path/to/the/install/dir
meson compile -C builddir
meson install -C builddir
```

Then update your PYTHONPATH variable to have it visible for python.
In your .bashrc, it would look like :
export PYTHONPATH=/My/complete/path/to/the/install/dir:$PYTHONPATH

### Install to the python root directory

```
meson setup builddir --prefix=$(python3 -c "import site; print(site.getsitepackages()[0])")
meson compile -C builddir
meson install -C builddir
```


