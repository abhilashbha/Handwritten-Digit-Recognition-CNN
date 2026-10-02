# Handwritten Digit Recognition Using Convolutional Neural Network

A deep learning project for handwritten digit classification using a Convolutional Neural Network (CNN) trained on the MNIST dataset.

## Overview

This project implements a CNN for recognizing handwritten digits from 0 to 9 using the MNIST dataset.

- Training images: 60,000
- Testing images: 10,000
- Image size: 28 × 28 pixels
- Image type: Grayscale
- Number of classes: 10

## CNN Architecture

The model consists of:

1. Input: 28 × 28 × 1
2. Conv2D: 32 filters, 3 × 3, ReLU
3. MaxPooling2D: 2 × 2
4. Conv2D: 64 filters, 3 × 3, ReLU
5. MaxPooling2D: 2 × 2
6. Flatten
7. Dense: 64 neurons, ReLU
8. Output Dense: 10 neurons, Softmax

**Total trainable parameters:** 121,930

## Preprocessing

Pixel values are normalized from the range 0–255 to 0–1 and the images are reshaped to include a single grayscale channel.

## Training Configuration

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Cross-Entropy |
| Epochs | 10 |
| Batch Size | 64 |
| Validation Split | 10% |

## Results

The final recorded model achieved:

| Metric | Result |
|---|---:|
| Training Accuracy | 99.74% |
| Best Validation Accuracy | 99.20% |
| Test Accuracy | **98.93%** |
| Test Loss | **0.0380** |
| Correct Test Predictions | 9,893 |
| Incorrect Test Predictions | 107 |
| Macro F1-Score | 0.99 |

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Seaborn
- Jupyter Notebook

## Project Structure

```text
Handwritten-Digit-Recognition-CNN/
│
├── notebooks/
│   └── digit_recognition.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

1. Install Python and Jupyter Notebook.
2. Install the required libraries:

```bash
pip install -r requirements.txt
```

3. Open `notebooks/digit_recognition.ipynb`.
4. Run the cells sequentially.

The notebook downloads the MNIST dataset through TensorFlow/Keras.

## Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Future Scope

Possible future extensions include:

- Testing on more diverse handwritten digit datasets
- Recognition of handwritten characters
- Support for different image resolutions
- Deeper CNN architectures
- Hyperparameter optimization
- Multi-digit handwritten number recognition

## Author

**Abhilash Bhat**  
Department of Computer Science and Engineering  
Sahyadri College of Engineering and Management, Mangaluru, Karnataka, India
