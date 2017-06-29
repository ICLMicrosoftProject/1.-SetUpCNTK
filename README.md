# SetUp CNTK
Basic Description for setting up CNTK Python on Ubuntu 14+ or 16+
We will start from describing the basic setup over the terminals

## Overview

### Some Resources
The Azure with CNTK is not covered in this tutorial, but you can access Azure from [this link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/category/compute?search=Data%20Science%20Viirtual%20Machine&page=1).
The official Github guide can be accessed through [here](https://github.com/Microsoft/CNTK).

In this tutorial, we focus on the python 2.7 setup following the step from [official Github guide](https://docs.microsoft.com/en-us/cognitive-toolkit/setup-linux-pythonK).

Other options accessing CNTK can be found [here](https://docs.microsoft.com/en-us/cognitive-toolkit/Setup-CNTK-on-your-machine)

## Set Up CNTK with Python on Linux Ubuntu
 
step 1. Ubuntu 16+ install openmpi-bin
```
sudo apt-get install openmpi-bin
```
Notes: For the Ubuntu 14+ install openmpi bin
```
wget https://www.open-mpi.org/software/ompi/v1.10/downloads/openmpi-1.10.3.tar.gz
tar -xzvf ./openmpi-1.10.3.tar.gz cd openmpi-1.10.3 ./configure --prefix=/usr/local/mpi make -j all sudo make install
export PATH=/usr/local/mpi/bin:$PATH export LD_LIBRARY_PATH=/usr/local/mpi/lib:$LD_LIBRARY_PATH
```
If you face any problem please go to the official site or leave a commend.
Regerence: Check out the open mpi section of the [official site](https://docs.microsoft.com/en-us/cognitive-toolkit/setup-cntk-on-linux#open-mpi)
