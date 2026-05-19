# Part 2 — CNN Computer Vision Prototype

## Project Overview

This project focuses on building a Convolutional Neural Network (CNN) prototype for an image classification problem using a synthetic manufacturing defect dataset.

The main objective is to understand how CNNs learn visual patterns using:

- Convolution layers
- Activation functions
- Pooling layers
- Dense layers
- Backpropagation

The model is trained to classify manufacturing product images into different defect categories.

---

# Dataset Information

Dataset Used:
- `Synthetic Manufacturing Defect Image Dataset`

Dataset reference:
- images/normal/
- images/scratch/
- images/dent/
- images/stain/
- labels.csv

## Problem Type

This is an **Image Classification** problem because each image belongs to exactly one category.

### Classes

- `normal` → product surface without defects
- `scratch` → surface with scratch-like defects
- `dent` → surface with dent-like defects
- `stain` → surface with stain-like defects

---

# Project Workflow

The project follows these steps:

1. Dataset exploration
2. Image preprocessing
3. Image resizing and normalization
4. Data augmentation
5. CNN model creation
6. Model training
7. Model evaluation
8. Prediction visualization
9. Business use case analysis

---

# Technologies Used

- Python
- NumPy
- Pandas
- OpenCV
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

---

# Repository Structure

```text
part-2-cnn-computer-vision/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
├── sample_predictions/
│   └── prediction_outputs.png
│
└── results/
    ├── accuracy_loss_curves.png
    └── confusion_matrix.png
```

---

# Image Preprocessing

The following preprocessing steps were applied:

- Resizing images to 128×128
- Converting images into NumPy arrays
- Pixel normalization
- Train-test split
- Data augmentation

### Data Augmentation Techniques

- Rotation
- Zoom
- Horizontal flipping

These techniques help improve model generalization and reduce overfitting.

---

# CNN Model Architecture

The CNN model contains:

- Convolution layers
- ReLU activation functions
- Max pooling layers
- Flatten layer
- Dense layer
- Dropout layer
- Softmax output layer

---

# Model Evaluation

The following evaluation metrics were used:

- Training accuracy
- Validation accuracy
- Testing accuracy
- Loss curves
- Confusion matrix
- Classification report
- Sample predictions

---

# CNN Concept Explanation

## 1. What is Convolution?

Convolution is an operation where small filters scan across an image to detect visual patterns such as edges, textures, and shapes.

CNNs automatically learn these important visual features during training.

---

## 2. Why is Pooling Used?

Pooling reduces the spatial size of feature maps while preserving important information.

Benefits include:
- reduced computation
- reduced overfitting
- improved feature focus

Max pooling is commonly used in CNNs.

---

## 3. Why is ReLU Commonly Used in CNNs?

ReLU (Rectified Linear Unit) introduces non-linearity into the network.

Advantages:
- faster training
- efficient gradient flow
- reduced vanishing gradient problem

---

## 4. Why Are CNNs Better Than Feed-Forward Networks for Images?

CNNs are specifically designed for image data.

They:
- preserve spatial relationships
- detect local image patterns
- require fewer parameters
- automatically learn visual hierarchies

Regular feed-forward networks flatten images and lose spatial structure.

---

# Business Use Case Mapping

## Manufacturing Quality Inspection

This CNN solution can be used in manufacturing industries for automated defect detection.

The model can identify:
- scratches
- dents
- stains
- defective product surfaces

### Benefits

- faster quality inspection
- reduced human error
- lower operational costs
- real-time monitoring

### Real-World Applications

- automobile manufacturing
- electronics production
- industrial quality control
- packaging industries

---

# Results

The CNN model successfully learned visual patterns from manufacturing images and was able to classify defects with good accuracy.

The training and validation curves showed effective learning behavior, while the confusion matrix demonstrated the model’s classification performance across all defect categories.

---

# How to Run the Project

## 1. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 2. Run Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebook.ipynb
```

---

# Output Files

The project generates:

- `accuracy_loss_curves.png`
- `confusion_matrix.png`
- `prediction_outputs.png`

These outputs are stored inside:
- `results/`
- `sample_predictions/`

---

# Conclusion

This project demonstrated the complete workflow of solving a computer vision image classification problem using CNNs.

The project covered:
- image preprocessing
- CNN architecture design
- model training
- evaluation
- prediction analysis
- business application mapping

The results showed how CNNs effectively learn visual features and outperform traditional feed-forward networks for image-based tasks.
