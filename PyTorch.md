### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# How to Install PyTorch & torchvision

## Requirements
1. python v3.6

## Installing PyTorch 1.7

```bash
$ wget https://nvidia.box.com/shared/static/cs3xn3td6sfgtene6jdvsxlr366m2dhq.whl -O torch-1.7.0-cp36-cp36m-linux_aarch64.whl
$ sudo apt-get install python3-pip libopenblas-base libopenmpi-dev
$ python3 -m pip install Cython
$ python3 -m pip install numpy torch-1.7.0-cp36-cp36m-linux_aarch64.whl
```
[Source](https://forums.developer.nvidia.com/t/pytorch-for-jetson-version-1-7-0-now-available/72048)

**NOTE**: Before installing, you should verify if [this page](https://forums.developer.nvidia.com/t/pytorch-for-jetson-version-1-7-0-now-available/72048) 
has any newer releases of torch. If so, subsitute the wget url as appropriate. 

## Installing the corresponding torchvision

```bash
$ sudo apt-get install libjpeg-dev zlib1g-dev libpython3-dev libavcodec-dev libavformat-dev libswscale-dev
$ git clone --branch 0.8.1 https://github.com/pytorch/vision torchvision
$ cd torchvision
$ export BUILD_VERSION=0.8.0  # NOTE: THIS IS MEANT TO BE 0.8.0 not 0.8.1
$ sudo python3 setup.py install
$ cd ../  # attempting to load torchvision from build dir will result in import error
```
[Source](https://forums.developer.nvidia.com/t/pytorch-for-jetson-version-1-7-0-now-available/72048)

**NOTE**: You must select the appropriate torchvision version that corresponds to your PyTorch version. 
See [here](https://forums.developer.nvidia.com/t/pytorch-for-jetson-version-1-7-0-now-available/72048)
