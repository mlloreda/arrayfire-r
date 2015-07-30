arrayfire-r
==============

This repository contains the files required to use ArrayFire from R.

This is a work in progress. Please follow [this issue](https://github.com/arrayfire/arrayfire-r/issues/7) to check on the progress.

Prerequisites
---------------

- Clone and build [ArrayFire](https://github.com/arrayfire/arrayfire)
    - All the pre-requisites for ArrayFire still apply.

- **make**

- **Linux**.
    - **Windows** and **OSX** support coming soon.

Contents
---------------

- **src/**: Contains the cpp source files interfacing with arrayfire
- **R/**: Contains the R source files wrapping the C interface
- **examples/**: contains a few examples demonstrating the usage

Usage
----------------

After you the necessary pre-requisites, edit the following paramets

- Open **src/Makevars** and change **AF_PATH** to the right location
- Change **AFCL** to 1 if you are using OpenCL

### Linux

If you built arrayfire with CUDA support, you may want to run the following command before installing arrayfire package:

```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/nvvm/lib64
```

- To install the package as root, run the following command from the directory containing of arrayfire-r
    - `sudo R CMD INSTALL arrayfire-r`

- To install the packages for the local user do the following
    - Create `R_libs` in your home directory: `mkdir ~/R_libs`
    - add `export R_LIBS=~/R_libs` to your **.bashrc**
    - You may need to do **source ~/.bashrc** if you are in the same session
    - Run `R CMD INSTALL arrayfire-r` from the directory containing arrayfire-r (`sudo` is not needed)


You can also put this in your `~/.bashrc` so you will not need to run the command again.

You should be good to go now!

Documentation
---------------
- TODO

License
---------------

This repository is distributed under the BSD 3 clause license. Please check the LICENSE file in the root directory for further information.
