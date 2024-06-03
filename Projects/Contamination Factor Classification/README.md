# Contaminant Factor Classification Model Using Only LiDAR Data

## Overview
Analyzing the impact of weather and environment on LiDAR is critical to ensure the safety of the car and the reliability of LiDAR sensors. The method of distinguishing between weather and contaminants using LiDAR point cloud data has been continuously studied. This document presents a model that improves upon past methods by utilizing machine learning and deep learning techniques to classify various contamination factors.

## Dataset
The model utilizes a dataset comprising point cloud data from LiDAR sensors mounted at various positions on the vehicle. The dataset is structured to capture different contamination effects such as snow, rain, dust, and anti-ice mixtures. 

- **Front**: 11,006 (Clear), 10,871 (Snow), 11,346 (Rain), 10,143 (Dust), 19,448 (Anti Ice Mixture)
- **Roof**: 15,572 (Clear), 18,973 (Snow), 15,340 (Rain), 18,069 (Dust), 19,784 (Anti Ice Mixture)
- **Rear**: 15,533 (Clear), 13,868 (Snow), 15,694 (Rain), 14,621 (Dust), 20,416 (Anti Ice Mixture)

## Methodology
The model leverages 16 feature vectors constructed from one frame of the near-field point cloud, which is the point cloud within a radius of 1 meter around the LiDAR. This reflects a more realistic situation based on data from the sensor cover, contaminated by real-world driving.

![Architecture of the Contamination Factor Classification Model](ContFactor_Classification_1_crop.pdf)
*Figure: Architecture of the Contamination Factor Classification Model*

## Experiment Results
The classification model has been tested using machine learning models like K-Nearest Neighbors (K-NN), Random Forest, and simple Deep Neural Networks (DNN), achieving high accuracy in various testing scenarios.

**Accuracy Comparison on Architectures:**
| Architecture | Position | Training Result | Test Result |
|--------------|----------|-----------------|-------------|
| K-NN (K=10)  | Front    | 99.8%           | 99.8%       |
|              | Roof     | 99.7%           | 99.6%       |
|              | Rear     | 99.7%           | 98.3%       |
| Random Forest (Max depth =16) | Front | 99.8% | 99.5% |
|                               | Roof  | 99.9% | 98.3% |
|                               | Rear  | 99.7% | 98.3% |
| DNN          | Front    | 98.8%           | 98.8%       |
|              | Roof     | 98.6%           | 98.6%       |
|              | Rear     | 96.4%           | 96.7%       |

This approach maintains high accuracy while reducing the complexity of data collection and processing, performing well in real-world road environments.

