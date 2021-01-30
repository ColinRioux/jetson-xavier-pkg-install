### [< BACK](https://github.com/ColinRioux/jetson-xavier-pkg-install)
# How to Install conda

## Requirements
1. For archiconda, python 3.6
2. For miniforge, varies

## Archiconda
**NOTE**: At the time of writing, archiconda seemed to be the most supported build of conda for the jetson

```bash
$ wget https://github.com/Archiconda/build-tools/releases/download/0.2.3/Archiconda3-0.2.3-Linux-aarch64.sh
$ sh Archiconda3-0.2.3-Linux-aarch64.sh
```
[Source](https://github.com/Archiconda/build-tools/releases)

## Miniforge
This is the superset of archiconda is updated regularly. I've had a mixed relationship working with [miniforge](https://github.com/conda-forge/miniforge)
Follow the instructions via the [miniforge github](https://github.com/conda-forge/miniforge) on getting miniconda
