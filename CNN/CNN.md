# CNN from Scratch

## Overview

This project implements a **Convolutional Neural Network (CNN) from scratch** using only Python and NumPy.  
The goal is to understand and demonstrate the **fundamental operations of a CNN**, including convolution, activation functions, pooling, flattening, and fully connected layers, applied to the **CIFAR-10 dataset**.

## Features

- **Forward Pass Implementation**  
  Processes input images through all layers of the network to produce predictions for ten classes.

- **Convolutional Layer**  
  Applies 3×3 kernels over input channels to extract features, including biases for each filter.

- **ReLU Activation**  
  Implements non-linearity by converting all negative values in the feature maps to zero.

- **Max Pooling**  
  Performs 2×2 spatial reduction, downsampling feature maps to reduce dimensionality while preserving the most prominent features.

- **Flattening**  
  Converts pooled feature maps into a single feature vector for the fully connected layer.

- **Fully Connected Layer**  
  Uses randomly initialized weights and biases to map the flattened feature vector to the output classes.

- **Prediction**  
  Selects the class with the maximum output value as the network’s predicted label.

## Step-by-Step Forward Pass Example

Below is the conceptual flow for a single image:

Input image: `(3, 32, 32)`

1. **Convolution**  
   `feature_map = sum(kernel * image_patch) + bias`  
   → output shape: `(3, 30, 30)`

2. **ReLU Activation**  
   `feature_map = max(0, feature_map)`  
   → negative values are zeroed out

3. **Max Pooling (2x2)**  
   `pooled_map = max of each 2x2 patch`  
   → output shape: `(3, 15, 15)`

4. **Flatten**  
   `feature_vector = pooled_map.reshape(225)`  
   → output shape: `(225,)`

5. **Fully Connected Layer**  
   `fc_output = feature_vector.dot(weights) + bias`  
   → output shape: `(10,)`

6. **Prediction**  
   `predicted_class = argmax(fc_output)`

**Note:** Because this implementation does **not use vectorized operations** for convolution, pooling, or fully connected layers, the computation is **extremely slow**. Even running inference on a single CIFAR-10 image can take significant time on a CPU. This demonstrates why **building CNNs from scratch for large datasets is not practical** compared to using optimized frameworks like PyTorch or TensorFlow.

## Learning Outcomes

- Deepened understanding of **CNN internals**, including feature extraction, activation, and dimensionality reduction.  
- Experienced **forward propagation** for image classification from first principles.  
- Gained insight into the **data flow of neural networks** without relying on high-level libraries.  
- Practiced **manual operations** in Python, highlighting the performance limitations of non-vectorized implementations.  

## Notes

- This project focuses on **learning and demonstration**; it does not include backpropagation or training.  
- Operates on **single images** at a time for clarity and conceptual understanding.  
- Provides a foundation for **future extensions**, such as multi-channel feature maps, multiple convolutional layers, and gradient-based learning.
