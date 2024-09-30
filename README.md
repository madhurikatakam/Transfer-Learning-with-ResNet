# FashionMNIST Classifier with Pretrained ResNet

This project implements a FashionMNIST classifier using a pretrained ResNet-18 model for feature extraction, followed by a fully connected classifier for classification. The model is fine-tuned and evaluated on the FashionMNIST dataset, and predictions can be visualized using a Tkinter GUI.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Training](#training)
- [Testing and Accuracy](#testing-and-accuracy)
- [GUI Visualization](#gui-visualization)
- [Results](#results)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project demonstrates a hybrid approach of using a pretrained ResNet-18 model to extract features from images in the FashionMNIST dataset, followed by training a simple fully connected classifier to predict the correct label for each image. The project also includes a Tkinter-based GUI for visualizing predictions on the test set.

## Dataset

We use the *FashionMNIST* dataset, which consists of 60,000 grayscale images (28x28 pixels) in 10 fashion-related categories, with 7,000 images per category. The test set contains 10,000 images.

- *Train Set*: 1,000 images (subset for faster processing)
- *Test Set*: 500 images (subset for faster processing)

Each image belongs to one of 10 classes:
1. T-shirt/top
2. Trouser
3. Pullover
4. Dress
5. Coat
6. Sandal
7. Shirt
8. Sneaker
9. Bag
10. Ankle boot

## Model Architecture

- *Feature Extractor*: We use a pretrained ResNet-18 model (with ImageNet weights) to extract features from the FashionMNIST images. The final fully connected layer of the ResNet is removed.
- *Classifier*: A simple fully connected layer (Linear layer) is trained on the extracted features to classify the images into one of the 10 categories.

## Installation

### 1. Clone the repository:
```bash
git clone https://github.com/your-username/fashionmnist-resnet-classifier.git
cd fashionmnist-resnet-classifier
