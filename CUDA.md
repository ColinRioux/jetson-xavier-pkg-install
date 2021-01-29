### < [BACK](README.md)
# How to Upgrade CUDA

1. Select the version you want from the [CUDA toolkit archive](https://developer.nvidia.com/cuda-toolkit-archive)
2. Select your OS family
3. Select your architecture. **NOTE**: jetsons use ARMv8 == aarch64 so select `sbsa` (if available)
4. Select Native (if option is available)
5. Select your OS and version
6. Follow the steps provided. For 11.2.0 at time of writing, it may look something like this:

```bash
$ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/sbsa/cuda-ubuntu1804.pin
$ sudo mv cuda-ubuntu1804.pin /etc/apt/preferences.d/cuda-repository-pin-600
$ wget https://developer.download.nvidia.com/compute/cuda/11.2.0/local_installers/cuda-repo-ubuntu1804-11-2-local_11.2.0-460.27.04-1_arm64.deb
$ sudo dpkg -i cuda-repo-ubuntu1804-11-2-local_11.2.0-460.27.04-1_arm64.deb
$ sudo apt-key add /var/cuda-repo-ubuntu1804-11-2-local/7fa2af80.pub
$ sudo apt-get update
$ sudo apt-get -y install cuda
```
