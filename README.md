# Unidirectional Guidance Network for Enhanced Small Object Detection in UAV Imagery
See below for a quickstart installation and usage example.

## Table of Contents

- [Dataset](##Dataset)
- [Install](##Install)
- [Usage](##Usage)

## Dataset

We use the Multi-Perspective Road Damage Dataset, and everything about it is in the Baidu web disk：

link: https://pan.baidu.com/s/1E-Y9tU66-1a2SncA_s7APw?pwd=1027  code: 1027


## Install
Pip install the ultralytics package including all [requirements](https://github.com/ultralytics/ultralytics/blob/main/pyproject.toml) in a [**Python>=3.8**](https://www.python.org/) environment with [**PyTorch>=1.8**](https://pytorch.org/get-started/locally/).

[![PyPI version](https://badge.fury.io/py/ultralytics.svg)](https://badge.fury.io/py/ultralytics) [![Downloads](https://static.pepy.tech/badge/ultralytics)](https://pepy.tech/project/ultralytics)

```bash
# Clone the ultralytics repository
git clone https://github.com/medeID113/UGNet.git

# Navigate to the cloned directory
cd UGNet

# Install the package in editable mode for development
pip install -e .
```

## Usage

Training:

 ```
 yolo detect train data=VisDrone.yaml model=ultralytics/cfg/models/UGNet.yaml epochs=120 imgsz=640 batch=4
 ```







