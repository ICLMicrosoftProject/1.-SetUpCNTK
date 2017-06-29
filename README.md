# SetUp CNTK
Basic Description for setting up CNTK Python on Ubuntu 14+ or 16+
We will start from describing the basic setup over the terminals

## I. Overview

## II. Some Resources
The Azure with CNTK is not covered in this tutorial, but you can access Azure from [this link](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/category/compute?search=Data%20Science%20Viirtual%20Machine&page=1).
The official Github guide can be accessed through [here](https://github.com/Microsoft/CNTK).

In this tutorial, we focus on the python 2.7 setup following the step from [official Github guide](https://docs.microsoft.com/en-us/cognitive-toolkit/setup-linux-pythonK).

Other options accessing CNTK can be found [here](https://docs.microsoft.com/en-us/cognitive-toolkit/Setup-CNTK-on-your-machine)

## III. Set Up CNTK with Python on Linux Ubuntu
 
### step 1-Ubuntu 16+ install openmpi-bin
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
Check out the open mpi section of the [official site](https://docs.microsoft.com/en-us/cognitive-toolkit/setup-cntk-on-linux#open-mpi)

### step 2. install CNTK for the first time
for python 2.7 CPU versions
```
sudo pip install https://cntk.ai/PythonWheel/CPU-Only/cntk-2.0-cp27-cp27mu-linux_x86_64.whl
```
for python 2.7 GPU versions 
This requires Cuda and cuDNN which can be found [here](https://docs.microsoft.com/en-us/cognitive-toolkit/Setup-CNTK-on-Windows#nvidia-cuda-8)
```
sudo pip install https://cntk.ai/PythonWheel/GPU/cntk-2.0-cp27-cp27mu-linux_x86_64.whl
```

Once complete it shows:
```
Requirement already satisfied: scipy>=0.17 in /usr/lib/python2.7/dist-packages (from cntk==2.0)
Requirement already satisfied: numpy>=1.11 in ./.local/lib/python2.7/site-packages (from cntk==2.0)
Installing collected packages: enum34, cntk
Successfully installed cntk-2.0 enum34-1.1.6
```
### step 3. Test the installation
We can test the installation through input in terminal:
```
python -c "import cntk; print(cntk.__version__)"
```
terminal should output(my current CNTK version is 2.0):
```
2.0
```

Reference: other options of installing CNTK with python can be found [here](https://docs.microsoft.com/en-us/cognitive-toolkit/setup-linux-python)
