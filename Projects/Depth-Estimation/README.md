# 2D Image Depth Prediction Model

## Overview

Depth estimation from 2D images is a fundamental task in computer vision that supports advances in scene understanding, 3D reconstruction, and autonomous navigation. Generating reliable depth maps from real-world scenarios significantly enhances applications in augmented reality, navigation, and semantic segmentation. With the rise of deep learning, convolutional neural networks (CNNs) have become crucial in converting 2D images into detailed 3D depth maps, enabling more accurate and dynamic environmental interactions.

## Dataset

Our dataset is uniquely poised to advance research in depth estimation due to its comprehensive coverage under diverse weather conditions and its multi-camera setups (13 cameras). This diversity ensures robust depth map generation, particularly in complex road scenes, which is essential for autonomous vehicle applications. The multi-perspective data mimics real-world driving scenarios, providing an invaluable resource for developing and testing depth estimation models.

## Methodology

Inspired by [Reference], we adopted the U-Net encoder-decoder architecture, renowned for its efficiency in image segmentation, and adapted it for depth estimation. This model excels at capturing both high-level context and intricate details, which are vital for generating precise depth maps from RGB images.

### Encoder (Contracting Path)

The contracting path includes multiple convolutional layers and pooling operations that progressively reduce the spatial dimensions while increasing feature depth. This architecture extracts crucial contextual information from the input images.

### Bottleneck

This section, devoid of pooling, processes the most abstract features extracted by the encoder, acting as a critical juncture between feature encoding and decoding.

### Decoder (Expanding Path)

The expanding path reconstructs the depth map by progressively up-sampling the encoded features and reintegrating spatial details through skip connections with the contracting path, ensuring detailed and accurate depth perception.

### Output Layer

The network concludes with a convolutional layer that outputs the depth map. For depth estimation tasks, linear or softmax activations are typically adapted, depending on the required depth representation.

## Experimental Results

We trained and validated the adapted U-Net model using the depth dataset from Kitti. The model achieved an accuracy of 94% and a Mean Squared Error (MSE) of 0.0682 on the training set, alongside 93% accuracy and an MSE of 0.0701 on the validation set. These results underscore the model’s effectiveness in handling real-world depth estimation challenges.

### Image Comparison

![Depth Estimation](https://github.com/WonLabUCI/Drive-Dataset/blob/3c92bf66d3e88c957bf58ba483a3eec50ede4914/Projects/Figures/Depth-Estimation.png)

*Illustration of an encoder-decoder architecture for depth estimation from images under various weather conditions. The left side depicts the model's architecture, with the encoder compressing the input image and the decoder reconstructing depth information. The right side shows examples of depth predictions for different weather scenarios (sunny, rainy, snowy) compared to LiDAR ground truth. The model performs well under clear conditions but shows variability in accuracy with adverse weather, highlighting the challenges in depth prediction using monocular vision systems.*

