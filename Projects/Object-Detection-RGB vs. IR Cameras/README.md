# Comparison of Object Detection Capabilities: RGB vs. IR Cameras

This repository contains the code and dataset for comparing the object detection performance of RGB and IR cameras using YOLOv8. The study highlights the advantages of integrating IR cameras in self-driving cars to overcome the limitations of RGB cameras in challenging conditions.

## Overview

RGB cameras are crucial components of self-driving cars but exhibit notable limitations under certain conditions, such as poor visibility at night, in foggy weather, and in detecting pedestrians and animals. Infrared (IR) cameras offer a potential solution to these shortcomings by enhancing detection capabilities in challenging environments.

## Methodology

We employed YOLOv8, a state-of-the-art object detection architecture, due to its superior performance relative to other detectors. Our dataset comprised 200 labeled RGB images and 100 labeled IR images, all synchronized for consistency. The dataset included two classes: 'person' and 'car'. To augment the data, we applied techniques such as horizontal flipping, noise addition, saturation adjustment, blurring, and cropping. The model was trained on a total of 466 images using an A100 GPU on Google Colab.

## Experimental Results

- **IR Data:**
  - Accuracy:
  - Mean Average Precision (mAP) of 50%: 99.5% accuracy.
  - Mean Average Precision (mAP) of 95%: 82% accuracy.
- **RGB Data:**
  - Accuracy: 
  - Mean Average Precision (mAP) of 50%: 99% accuracy.
  - Mean Average Precision (mAP) of 95%: 75% accuracy.

Although RGB cameras demonstrated high accuracy, they failed to detect objects in certain scenarios, such as at the entrances and exits of tunnels where lighting conditions change abruptly. Conversely, IR cameras consistently detected objects, including people from significant distances. In adverse weather conditions like fog or dust, where visibility is compromised for both RGB cameras and drivers, IR cameras continued to perform effectively. At night, IR cameras maintained their detection capabilities, particularly on two-way roads where the headlights of oncoming vehicles impair visibility for drivers and RGB cameras. IR cameras, unaffected by these issues, functioned optimally.

## Image Comparison
![IRvsRGB](https://github.com/WonLabUCI/Drive-Dataset/blob/990e6128bd6a84544acfe5d5ddd95de027567a02/Projects/Figure/IRvsRGB.png)
Figure 5. Comparison of object detection capabilities between RGB and IR cameras in various challenging conditions:
- **(a)** Detection at the entrance of a tunnel, demonstrating IR camera's superior performance despite lighting changes.
- **(b)** Detection on a rainy road, showing IR camera's ability to detect distant objects that RGB cameras miss.
- **(c)** Detection in dusty conditions, highlighting IR camera's effectiveness where RGB visibility is compromised.
- **(d)** Nighttime detection on a two-way road, illustrating IR camera's consistent performance despite headlight glare that affects RGB cameras.


## Dataset

The dataset includes:
- 200 labeled RGB images.
- 200 labeled IR images.

Each image is labeled with two classes: 'person' and 'car'. The images are synchronized for consistency.

