# VGG16 Image Classification

## Overview

This repository contains an image classification model based on the VGG16 architecture using Transfer Learning with TensorFlow and Keras.

The model is designed to classify grayscale images of size 64×64. Since VGG16 expects RGB images, a convolutional layer is used to convert the single-channel input into a three-channel representation before feeding it to the pretrained network.

## Features

* Transfer Learning using VGG16 pretrained on ImageNet
* Support for grayscale image inputs
* Data preprocessing and normalization
* Training and validation split
* Accuracy and loss visualization
* TensorFlow/Keras implementation

## Dataset

The dataset consists of grayscale images stored in NumPy format.

Required files:

* `images_original.npy`
* `encoded_labels_original.npy`

Example shapes:

```python
images_original.npy      # (N, 64, 64, 1)
encoded_labels_original.npy
```

## Requirements

Install the required libraries:

```bash
pip install tensorflow numpy matplotlib scikit-learn
```

## Model Architecture

1. Input layer: `(64, 64, 1)`
2. Convolution layer to convert grayscale images to 3 channels
3. Pretrained VGG16 backbone (`ImageNet` weights)
4. Global Average Pooling
5. Dense layer (128 neurons, ReLU)
6. Dropout (0.5)
7. Softmax output layer

## Training

Run the notebook:

```bash
VGG16_images_original_0_9805.ipynb
```

Training settings:

* Optimizer: Adam (1e-4)
* Loss Function: Sparse Categorical Crossentropy
* Epochs: 40
* Batch Size: 64

## Results

The notebook includes:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss

Performance plots are generated after training.

## Project Structure

```text
├── VGG16_images_original_0_9805.ipynb
├── images_original.npy
├── encoded_labels_original.npy
└── README.md
```

## Citation

If you use this work in your research, please cite the corresponding publication.

## License

MIT License

```
```
