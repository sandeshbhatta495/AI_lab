# CIFAR-10 Image Classification using Multiple Deep Learning Architectures

## Student Information
**Name:** Sandesh Bhatta  
**Roll No:** ACE080BEI025  

---

## Project Overview

This project focuses on image classification using three different deep learning architectures implemented in PyTorch:

- Simple Neural Network (Fully Connected)
- AlexNet (Modified for CIFAR-10)
- TinyVGG

All three models were trained and evaluated on the CIFAR-10 dataset. The primary objective of this project is to compare their performance in terms of:

- Test Accuracy
- Training Time
- Convergence Speed
- Model Complexity (Number of Parameters)
- Generalization Ability

---

## Dataset Description

The project uses the CIFAR-10 dataset provided by torchvision.

CIFAR-10 consists of:
- 60,000 color images
- Image size: 32 × 32
- 10 object classes:
  airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

The dataset was split into:
- 50,000 training images
- 10,000 test images

Data augmentation techniques such as random horizontal flipping, random cropping, and small rotations were applied to improve generalization.

---

## Models Implemented

### 1. Simple Neural Network (Baseline)

- Fully connected architecture
- Images flattened into 1D vectors
- Does not preserve spatial information
- Used as a baseline model for comparison

### 2. AlexNet (Modified)

Based on the paper:
"ImageNet Classification with Deep Convolutional Neural Networks"

The architecture was modified to accept 32×32 CIFAR-10 images. It includes:
- Multiple convolutional layers
- ReLU activation
- Max pooling
- Dropout layers
- Fully connected classifier

This model demonstrates the improvements introduced by deep convolutional networks over traditional neural networks.

### 3. TinyVGG

A simplified VGG-style architecture using:
- 3×3 convolution filters
- ReLU activation
- Max pooling
- Smaller and more efficient design

TinyVGG focuses on simplicity and efficiency while maintaining strong performance.

---

## Training Configuration

All models were trained under the same conditions to ensure fair comparison:

- Loss Function: CrossEntropyLoss
- Optimizer: SGD with Momentum
- Learning Rate: 0.01
- Momentum: 0.9
- Weight Decay: 5e-4
- Batch Size: 128
- Number of Epochs: 10
- GPU Training (Google Colab)

---

## Experimental Results

| Model     | Parameters | Training Time (s) | Test Accuracy (%) |
|-----------|------------|-------------------|-------------------|
| SimpleNN  | 1,707,274  | 403.1             | 49.38             |
| AlexNet   | 4,483,146  | 450.2             | 76.72             |
| TinyVGG   | 1,116,970  | 437.5             | 81.66             |

---

## Interpretation of Results

The Simple Neural Network achieved the lowest accuracy because it does not preserve spatial structure of images. Flattening the image removes positional information, making it difficult for the model to learn meaningful visual features.

AlexNet significantly improved performance due to the use of convolutional layers, ReLU activation, pooling, and dropout. These components allow the network to learn hierarchical image features and reduce overfitting.

TinyVGG achieved the highest accuracy while using fewer parameters than AlexNet. This indicates that smaller convolution kernels (3×3) stacked deeper can provide better feature extraction with improved efficiency.

Overall, convolutional neural networks clearly outperform fully connected neural networks for image classification tasks.

---

## Conclusion

This project demonstrates the importance of architecture design in deep learning. CNN-based models preserve spatial information and extract hierarchical features, resulting in better generalization and higher accuracy.

Among the three models, TinyVGG provided the best trade-off between model complexity and performance on CIFAR-10.

---

## References
1. PyTorch Documentation: https://pytorch.org/docs/stable/index.html
2. CIFAR-10 Dataset: https://www.cs.toronto.edu/~kriz/cifar.html
3. AlexNet Paper: "ImageNet Classification with Deep Convolutional Neural Networks" by Alex Krizhevsky, Ilya Sutskever, and Geoffrey E. Hinton (2012): https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf
4. VGG Paper: "Very Deep Convolutional Networks for Large-Scale Image Recognition" by Karen Simonyan and Andrew Zisserman (2014): https://arxiv.org/abs/1409.1556