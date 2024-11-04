# Unidirectional Guidance Network for Enhanced Small Object Detection in UAV Imagery
See below for a quickstart installation and usage example.

## Table of Contents

- [Dataset](##Dataset)
- [Install](##Install)
- [Usage](##Usage)

## Dataset
The dataset in our study is based on VisDrone2019-DET dataset(https://github.com/VisDrone/VisDrone-Dataset), and AI-TOD dataset (https://github.com/jwwangchn/AI-TOD)


## Install
Pip install the UGNet package including all requirements in a [**Python>=3.8**](https://www.python.org/) environment with [**PyTorch>=1.8**](https://pytorch.org/get-started/locally/).

[![PyPI version](https://badge.fury.io/py/ultralytics.svg)](https://badge.fury.io/py/ultralytics) [![Downloads](https://static.pepy.tech/badge/ultralytics)](https://pepy.tech/project/ultralytics)

```bash
# Clone the UGNet
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

yolo detect train data=ultralytics/cfg/datasets/aitod.yaml model=ultralytics/cfg/models/UGNet.yaml epochs=120 imgsz=640 batch=4
 ```







