### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# How to Install NVIDIA-DALI (Cuda 11+)
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

# How to Install NVIDIA-DALI (Cuda 10)

## Install
On your host linux machine:
1. Configure DALI source
```bash
$ git clone https://github.com/NVIDIA/DALI.git
$ cd DALI
$ git submodule update --init --recursive
$ cd ../
```
2. Go [download](https://developer.nvidia.com/NVIDIA-sdk-manager#dockersupport) the docker image for NVIDIA's sdk manager and follow the steps to configure
**NOTE**: Need docker installed on your host machine

3. Run the SDK manager and download the appropriate deb execs for cross-compiling dali for aarch64 with cuda 10
```bash
$ docker run -it --rm sdkmanager:latest --cli downloadonly --logintype devzone --product Jetson --version 4.5 --targetos Linux --host --target P3668-0001 --flash all --additionalsdk DeepStream
```

4. Follow the steps [here](https://docs.nvidia.com/deeplearning/dali/user-guide/docs/compilation.html#setup) to compile a DALI wheel for cuda 10

5. Alternatively, you can download the precompiled wheel from this repo
