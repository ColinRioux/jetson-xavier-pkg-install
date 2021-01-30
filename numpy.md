### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# How to install/upgrade numpy

```bash
$ sudo apt-get update
$ sudo apt-get install -y build-essential gfortran libatlas-base-dev
$ sudo python3 -m pip install numpy
```

# Debugging issues with numpy
- At of time of writing, numpy 1.19.5 supports python 3.6 just fine but will likely throw an `(Illegal instruction) core dumped` error on import.
This issue is caused by OPENBLAS. To fix, you must set an environment variable: `OPENBLAS_CORETYPE=ARMV8`
