# Cat vs Dog Image Classification using Transfer Learning

## Overview

This project implements an image classification system that distinguishes between **cats and dogs** using deep learning. The models are trained using **transfer learning techniques** with pretrained convolutional neural networks.

Two pretrained models were implemented and compared:

* **MobileNetV2**
* **ResNet50**

The goal of this project is to evaluate the performance of these models on a cat vs dog image dataset and analyze their classification accuracy.



# Dataset

The dataset used in this project was obtained from Kaggle.

Dataset:
**Cat and Dog Images for Classification**

The dataset contains images labeled as either:

* Cat
* Dog

### Dataset Size

| Type       | Images |
| ---------- | ------ |
| Training   | 20,000 |
| Validation | 5,000  |
| Total      | 25,000 |

Each image is associated with a label stored in a CSV file.



# Methodology

The project follows the following pipeline:

1. Dataset loading and preprocessing
2. Image normalization and resizing (224 × 224)
3. Training using transfer learning models
4. Model evaluation using accuracy and confusion matrix
5. Comparison of model performance



# Models Implemented

## 1. MobileNetV2

MobileNetV2 is a lightweight convolutional neural network optimized for mobile and embedded devices. It uses **depthwise separable convolutions**, which significantly reduce the number of parameters while maintaining high accuracy.

MobileNetV2 was used as a **pretrained feature extractor**, and additional dense layers were added for binary classification.

### Performance

* Validation Accuracy: **≈ 98.3%**
* Correct Predictions: **4914 / 5000**

Confusion Matrix:

| Actual \ Predicted | Cat  | Dog  |
| ------------------ | ---- | ---- |
| Cat                | 2445 | 38   |
| Dog                | 48   | 2469 |



## 2. ResNet50

ResNet50 is a deep residual neural network consisting of **50 layers**. It introduces **residual connections** to solve the vanishing gradient problem in deep neural networks.

The pretrained ResNet50 model was fine-tuned for the cat vs dog classification task.

### Performance

* Validation Accuracy: **≈ 70.5%**
* Correct Predictions: **3527 / 5000**

Confusion Matrix:

| Actual \ Predicted | Cat  | Dog  |
| ------------------ | ---- | ---- |
| Cat                | 1706 | 777  |
| Dog                | 696  | 1821 |


# Evaluation Metrics

The models were evaluated using the following metrics:

* Accuracy
* Confusion Matrix
* Classification Report
* Training vs Validation Accuracy Graphs


# Results

| Model       | Validation Accuracy |
| ----------- | ------------------- |
| MobileNetV2 | **98.3%**           |
| ResNet50    | 70.5%               |

MobileNetV2 achieved significantly higher accuracy compared to ResNet50 on this dataset.

# Conclusion

This project demonstrates the effectiveness of **transfer learning for image classification tasks**. The MobileNetV2 model achieved the highest performance due to its efficient architecture and ability to generalize well on smaller datasets.

ResNet50, while powerful, did not perform as well in this experiment due to limited fine-tuning and the smaller dataset size.

Overall, the results show that **lightweight pretrained networks like MobileNetV2 are highly effective for cat vs dog image classification tasks**.


# Technologies Used

* Python
* TensorFlow / Keras
* Google Colab
* NumPy
* Pandas
* Matplotlib
* Seaborn

# Future Improvements

Future improvements for this project include:

* Fine-tuning deeper layers of pretrained models
* Applying data augmentation techniques
* Experimenting with additional architectures such as EfficientNet
* Increasing the dataset size for improved generalization

