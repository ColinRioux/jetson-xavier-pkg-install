### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# How to Configure TensorRt in a Conda environment

**Note**: TensorRt is already installed on Jetson units. 
This is if you want tensorRt and other dist packages (installed via apt) to be accessible via conda environment.

```bash
##### Outside of conda entirely
$ python3 -m pip show tensorrt
# The path that is outputted copy to your clipboard
$ cd ~/archiconda3/envs/<your env name>/lib/python3.6/site-packages
$ vi tensorrt.pth
# Paste that path in & save/quit
$ conda activate <your env name>
$ pip list # verify tensorrt is on the list
```
