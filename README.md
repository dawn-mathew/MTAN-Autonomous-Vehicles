# MTAN-Autonomous-Vehicles
## Introduction
This repository houses both the code and datasets for evaluation of the Multi-Task Attention Network (MTAN) in the context of autonomous driving tasks.It was utilized for assessing the performance of the MTAN for various autonomous vehicular applications such as object detection, object segmentation and depth map generation.

> Note: Majority of this code is borrowed from the original MTAN github repository. `MTAN_main` was created for educational purposes to learn about Multi-Task Attention Network (MTAN) in the context of autonomous driving tasks and evaluate its performance. Please take a look at the [original repository](https://github.com/lorenmt/mtan).

## Repo Structure
```
├── data
│   ├── train
│   │   ├── depth
│   │   ├── image
│   │   └── label
│   └── val
│       ├── depth
│       ├── image
│       └── label
└── MTAN_main.ipynb

```
- `depth` is the directory contains the various depth maps on which the neural network was trained.
- `image` is the directory containing the semantic segmented images for training the MTAN algorithm.
- `label` is the directory containing files with the various labels associated witheach segmented image in `image` directory. 
- `MTAN_main.ipynb` is a Jupyter Notebook containing the code and documentation related to training the MTAN algorithm and performing computer vision tasks on the provided dataset.
> Note: The entirety of the required dataset for training has not been uploaded due to size restrictions. Please download from the offical website.

## Dependencies
Install all of the following libraries. 
```py
import torch
import torch.nn as nn
import torch.optim as optim
import torch.nn.functional as F
from torch.utils.data.dataset import Dataset
import torch.utils.data.sampler as sampler
import os
import fnmatch
import numpy as np
import random
import matplotlib.pyplot as plt
```

## Results
> Note: Training the MTAN network is very computationally heavy. As a result the network was only trained for 1 epoch in my host machine, as evident from the Jupyter notebook. Instead I performed the training in my University's data lab, from which the following results are evident.
### Segmentation Prediction
![Segmentation Prediction](https://github.com/dawn-mathew/MTAN-Autonomous-Vehicles/assets/150279674/81f0ef63-9722-4e67-92ac-fe12d9ad1c9e)
### Overlays
![Overlay](https://github.com/dawn-mathew/MTAN-Autonomous-Vehicles/assets/150279674/731c65fa-7046-4718-96d2-dc72ddf630d5)
### Depth map estimation
![Depth map estimation](https://github.com/dawn-mathew/MTAN-Autonomous-Vehicles/assets/150279674/3df0f1b7-5283-4735-a89a-97eb4da1adcb)


