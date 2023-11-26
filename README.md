# Generative Model by Image Ordering

This project aims to generate synthetic images through a unique approach – by interpolating between two real images. The images from ImageNet could be considered as frames extracted from a real-world video. The generation process involves constructing an adjacency matrix of images based on features extracted from state-of-the-art (SOTA) models and Wasserstein distance. The final step involves sorting the images along one dimension.

## Objective

The primary goal is to create a generative model capable of producing synthetic images that smoothly transition between real-world frames. The approach leverages cutting-edge techniques in deep learning and optimal transport.

## Methodology

1. **Adjacency Matrix Construction:**
    - Features extracted from pretrained EfficientNet model ([EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/abs/1905.11946)) are utilized.
    - Wasserstein distance is employed to measure the dissimilarity between feature vectors.
    - The result is an adjacency matrix representing the relationships between different frames.

2. **Image Sorting:**
    - The adjacency matrix is used to sort images along a specific dimension, creating a coherent and smooth transition between frames.

## Tools and Frameworks

- **Pretrained SOTA Model:**
    - EfficientNet, known for its efficiency and accuracy in image classification tasks.

    [EfficientNet Paper](https://arxiv.org/abs/1905.11946)

- **Wasserstein Distance Calculation:**
    - Python Optimal Transport (POT) package is employed for calculating Wasserstein distance.

    [POT Paper](https://jmlr.org/papers/v22/20-451.html)
