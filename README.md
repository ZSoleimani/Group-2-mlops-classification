# Group-2-mlops-classification
Group 2: Project for 02476 Machine Learning Operations (DTU Course)

## Project goal
This project aims to classify images of various PC parts using a deep learning model, specifically leveraging the power of Albumentations for data augmentation to improve model robustness. The dataset used for this project is the PC Parts Images Dataset from Kaggle, which contains images of different computer components (e.g., motherboards, RAM, graphics cards, etc.).

## Project Overview
The goal of this project is to create an image classification model that can recognize different PC parts using convolutional neural networks (CNNs). We apply Albumentations, an image augmentation library, to artificially increase the size and variability of the dataset, which helps improve model performance by providing a more diverse set of training examples. This ensures better generalization for real-world application, such as automatic identification of PC components in various scenarios.

## Data description
The dataset data initially used for this project is the [PC Parts Images Dataset](https://www.kaggle.com/datasets/asaniczka/pc-parts-images-dataset-classification?select=pc_parts) from Kaggle, consisting of 3,279 images categorized into 14 distinct classes: 
- cables
- case
- cpu
- gpu
- hdd
- headset
- keyboard
- microphone
- monitor
- motherboard
- mouse
- ram
- speakers
- webcam

Each image has a resolution of 256x256 pixels and formatted in the JPG file type. The data provides a balanced representation of PC parts, which makes it suitable for a multi class classification task.

## Models
Our primary focus will be on developing a simple convolutional neural network (CNN) architectur for the image classification task. The CNN will include layers for feature extraction (convolutional and pooling layers) and fully connected layers for classification. To optimize performance, we will experiment with the network architecture and hyperparameter settings using the tools provided in 02476. If needed, we might explore transfer learning using pre-trained models such as MobileNet or ResNet and fine-tuning them; we might also instead just experiment with the third party package, Albumentation, where two identical models are trained (one uses Albumentaion and one doesn't)and compared to quantify the efficacy of albumentation.
