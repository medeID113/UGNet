## <div align="center">Documentation</div>

See below for a quickstart installation and usage example.

<details open>
<summary>Install</summary>

Pip install the ultralytics package including all [requirements](https://github.com/ultralytics/ultralytics/blob/main/pyproject.toml) in a [**Python>=3.8**](https://www.python.org/) environment with [**PyTorch>=1.8**](https://pytorch.org/get-started/locally/).

[![PyPI version](https://badge.fury.io/py/ultralytics.svg)](https://badge.fury.io/py/ultralytics) [![Downloads](https://static.pepy.tech/badge/ultralytics)](https://pepy.tech/project/ultralytics)

```bash
# Clone the ultralytics repository
git clone https://github.com/ultralytics/ultralytics

# Navigate to the cloned directory
cd ultralytics

# Install the package in editable mode for development
pip install -e .
```

For alternative installation methods including [Conda](https://anaconda.org/conda-forge/ultralytics), [Docker](https://hub.docker.com/r/ultralytics/ultralytics), and Git, please refer to the [Quickstart Guide](https://docs.ultralytics.com/quickstart).

</details>

<details open>
<summary>Usage</summary>

### CLI

YOLOv8 may be used directly in the Command Line Interface (CLI) with a `yolo` command:

```bash
yolo predict model=yolov8n.pt source='https://ultralytics.com/images/bus.jpg'
```

`yolo` can be used for a variety of tasks and modes and accepts additional arguments, i.e. `imgsz=640`. See the YOLOv8 [CLI Docs](https://docs.ultralytics.com/usage/cli) for examples.

### Python

YOLOv8 may also be used directly in a Python environment, and accepts the same [arguments](https://docs.ultralytics.com/usage/cfg/) as in the CLI example above:

```python
from ultralytics import YOLO

# Load a model
model = YOLO("yolov8n.yaml")  # build a new model from scratch
model = YOLO("yolov8n.pt")  # load a pretrained model (recommended for training)

# Use the model
model.train(data="coco8.yaml", epochs=3)  # train the model
metrics = model.val()  # evaluate model performance on the validation set
results = model("https://ultralytics.com/images/bus.jpg")  # predict on an image
path = model.export(format="onnx")  # export the model to ONNX format
```







# Balanced-RDD

[![license](https://camo.githubusercontent.com/4738d430387c93da0d49ef0428a7c7ddae18e81eaff99a014996d4f6b30fd3ef/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6c6963656e73652f3a757365722f3a7265706f2e737667)](https://github.com/RichardLitt/standard-readme/blob/main/example-readmes/LICENSE) [![standard-readme compliant](https://camo.githubusercontent.com/f116695412df39ab3c98d8291befdb93af123f56aecc79fff4b20c410a5b54c7/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f726561646d652532307374796c652d7374616e646172642d627269676874677265656e2e7376673f7374796c653d666c61742d737175617265)](https://github.com/RichardLitt/standard-readme)

Balanced-RDD is a lightweight model for road damage detection that is designed to achieve the best balance of speed and accuracy.

![](/Users/heqihan/Desktop/Balanced-RDD/results.png)

## Table of Contents

- [Dataset](#Usage)
- [Install](#Install)
- [Usage](#Usage)

## Dataset

We use the Multi-Perspective Road Damage Dataset, and everything about it is in the Baidu web disk：

link: https://pan.baidu.com/s/1E-Y9tU66-1a2SncA_s7APw?pwd=1027  code: 1027

## Install

Clone repo and install [requirements.txt](https://github.com/ultralytics/yolov5/blob/master/requirements.txt) in a [**Python>=3.8.0**](https://www.python.org/) environment, including [**PyTorch>=1.8**](https://pytorch.org/get-started/locally/).

```
pip install -r requirements.txt  # install
```

## Usage

Training:

 ```
 from ultralytics import YOLO
 
 if __name__ == "__main__":
 
 # "From scratch"
 
   model = YOLO('ultralytics/models/Balnaced-RDD.yaml')
   
   model.train(**{'cfg':'ultralytics/yolo/cfg/default.yaml'})
 ```

![](/Users/heqihan/Desktop/Balanced-RDD/train.png)

See YOLOv8 [Python Docs](https://docs.ultralytics.com/usage/python) for more examples.

</details>

