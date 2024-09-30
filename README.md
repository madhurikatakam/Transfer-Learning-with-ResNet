# FashionMNIST Classifier with Pretrained ResNet

This project implements a FashionMNIST classifier using a pretrained ResNet-18 model for feature extraction, followed by a fully connected classifier for classification. The model is fine-tuned and evaluated on the FashionMNIST dataset, and predictions can be visualized using a Tkinter GUI.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Testing and Accuracy](#testing-and-accuracy)
- [GUI Visualization](#gui-visualization)

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

## Training

- During training, the classifier is trained on features extracted from the FashionMNIST images using the pretrained ResNet-18. You can adjust the number of epochs, learning rate, and batch size in the train_classifier.py script.
- The optimizer used is Adam with a learning rate of 0.001, and the loss function is CrossEntropyLoss.

## Testing and Accuracy

-The accuracy is evaluated by comparing the classifier's predictions on the test set to the ground truth labels. The accuracy can be printed in the terminal after training is complete.

## GUI Visualization

- A Tkinter GUI is implemented to visualize the model's predictions on the test set. You can click a button to see the next prediction in the test set.
- Tkinter GUI: Displays the FashionMNIST images and shows the predicted class label.

![image](https://github.com/user-attachments/assets/a2d34a44-1548-4426-9058-ec90616aa988)
![image](https://github.com/user-attachments/assets/8a0390e3-6817-4f67-8fa1-d1d3a2e0f863)
![image](https://github.com/user-attachments/assets/a6b8b4e5-49ca-44f3-a9df-3a7f8d61ae15)
![image](https://github.com/user-attachments/assets/c124ec69-6132-4b75-b51d-3a8dd84dd500)
![image](https://github.com/user-attachments/assets/578b3cd6-7716-4803-8de0-61f3b515f10f)









