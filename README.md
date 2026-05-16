# Part 2: Computer Vision Problem Formulation and CNN Prototype

Prepared by: Sharda Jadhav  
MBA in Data Analytics

---

# Project Overview

This project focuses on building a Convolutional Neural Network (CNN) model for an image classification problem. The main objective of this project was to understand how CNNs learn visual patterns from image data using convolution layers, pooling layers, activation functions, and dense layers.

The project was implemented using Python, TensorFlow/Keras, OpenCV, Matplotlib, Seaborn, and Scikit-learn.

---

# Dataset Information

The dataset contains images divided into four categories:

- normal
- dent
- stain
- scratch

The objective of the model is to classify images into the correct category based on visual defect patterns.

Dataset Source Link:

https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing

---

# Task 1: Problem Identification

The given dataset represents an Image Classification problem in the field of Computer Vision. Each image belongs to one predefined category such as normal, dent, stain, or scratch.

Image classification is the most suitable problem type because the CNN model only needs to predict the correct category of the image based on its visual appearance. The model does not need to detect object locations or perform segmentation.

CNN models are highly effective for image classification tasks because they automatically learn visual features such as textures, edges, stains, and defect patterns directly from image data.

---

# Task 2: Dataset Exploration

The dataset was explored to understand:

- Number of image classes
- Number of images per class
- Sample images from each class
- Image dimensions
- Dataset distribution

### Observation

The dataset contains four image classes: normal, dent, stain, and scratch. Each category contains 120 images, making the dataset balanced across all classes.

Sample images from each category were visualized to understand visual differences in defect patterns and surface conditions.

---

# Task 3: Image Preprocessing

The following preprocessing steps were performed:

- Resized all images to 64 × 64 pixels
- Normalized pixel values between 0 and 1
- Split dataset into training and validation/testing sets
- Applied image augmentation techniques such as:
  - Rotation
  - Zooming
  - Horizontal flipping

### Observation

Image preprocessing helped standardize the dataset for CNN training. Augmentation techniques improved dataset variability and helped reduce overfitting during training.

---

# Task 4: CNN Model Creation

A Convolutional Neural Network (CNN) model was created using TensorFlow/Keras Sequential API.

### CNN Architecture

- Convolution Layer
- ReLU Activation Function
- Max Pooling Layer
- Flatten Layer
- Dense Layer
- Dropout Layer
- Output Layer with Softmax Activation

### Model Details

- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Output Classes: 4

### Observation

The CNN model successfully learned visual features such as scratches, stains, and dents from image data. Pooling layers helped reduce computational complexity while dense layers learned higher-level image representations.

---

# Task 5: Model Training and Evaluation

The CNN model was trained for 10 epochs and evaluated using:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Confusion Matrix
- Classification Report
- Sample Predictions

### Model Performance

- Final Testing Accuracy: Approximately 84%

### Observation

Training and validation accuracy improved gradually during model training, while loss values continuously decreased. The CNN model was able to correctly classify many test images based on defect-related visual patterns.

The confusion matrix and classification report showed that some image classes were predicted more accurately than others. Certain defects had visually similar patterns, which created some classification challenges.

---

# Task 6: CNN Concept Explanation

## 1. What is Convolution?

Convolution is one of the main operations in a CNN model. In this process, small filters or kernels move across the image and try to identify important visual patterns such as edges, lines, textures, scratches, stains, or shapes. Instead of processing the entire image at once, the CNN learns small details step by step and combines them to understand the full image.

For example, in this project the CNN learns to identify features like scratch marks, stain spots, or dents from surface images. Different filters learn different types of patterns automatically during training.

---

## 2. Why is Pooling Used?

Pooling is used to reduce the size of the feature maps after convolution. This helps reduce computation time and makes the model more efficient. Pooling also helps the model focus only on the most important visual information instead of every small pixel detail.

In simple words, pooling works like summarizing important image features. For example, even if the position of a scratch changes slightly in the image, pooling helps the CNN still recognize the defect correctly. Max Pooling is commonly used because it keeps the strongest and most important features from the image.

---

## 3. Why is ReLU Commonly Used in CNNs?

ReLU (Rectified Linear Unit) is widely used in CNN models because it helps the network learn faster and improves training performance. ReLU converts negative values into zero while keeping positive values unchanged. This makes the calculations simpler and helps the model train efficiently.

Another important reason is that ReLU helps avoid the vanishing gradient problem, which can slow down learning in deep neural networks. Since CNN models contain multiple layers, ReLU makes training more stable and faster.

---

## 4. Why are CNNs Better than Regular Feed-Forward Networks for Image Data?

CNNs are specially designed for image processing tasks, while regular feed-forward neural networks are more suitable for simple numerical data. Images contain spatial relationships between nearby pixels, and CNNs can capture these relationships effectively using convolution and pooling operations.

For example, in this project the CNN can identify scratches, dents, and stains based on their visual appearance and location patterns. A normal feed-forward network would treat every pixel separately and would require a very large number of parameters, making learning difficult and inefficient.

CNNs automatically learn visual features directly from images, which makes them more accurate and powerful for computer vision tasks like image classification, object detection, and facial recognition.

---

# Task 7: Business Use Case Mapping

This type of computer vision solution can be highly useful in the manufacturing industry for automated quality inspection and defect detection.

In many industries, products must be checked for scratches, dents, stains, or damaged areas before delivery. Traditionally, this inspection process is done manually, which can be time-consuming and prone to human error.

A CNN-based computer vision system can automate this process by analyzing product images and identifying defects in real time.

For example, in smartphone manufacturing or automobile industries, cameras can capture product images during production and the CNN model can automatically classify defective and non-defective products. This helps improve product quality, reduce manual effort, minimize defective product delivery, and increase operational efficiency.

---

# Technologies Used

- Python
- Google Colab
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# Repository Structure

```bash
part-2-cnn-computer-vision/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
├── sample_predictions/
│   └── prediction_outputs.png
└── results/
    ├── accuracy_loss_curves.png
    └── confusion_matrix.png
```

---

# Conclusion

This project provided practical understanding of CNN architecture and computer vision fundamentals. The CNN model was able to learn visual defect patterns from images and classify them into different categories with good accuracy.

The project also demonstrated how convolution, pooling, activation functions, and dense layers work together in deep learning-based image classification systems.
