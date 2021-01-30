### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# How to Install NVIDIA-DALI
Finally, NVIDIA finally has pre-compiled binaries for DALI. No more building from source attempts.

## Requirements
1. Cuda 11.0+
2. python 3.6

## Install
```bash
$ wget https://developer.download.nvidia.com/compute/redist/nvidia-dali-cuda110/nvidia_dali_cuda110-0.30.0-1983575-py3-none-manylinux2014_aarch64.whl
$ python3 -m pip install nvidia_dali_cuda110-0.25.1-1612461-py3-none-manylinux2014_aarch64.whl
```
[Source](https://github.com/NVIDIA/DALI/releases)
