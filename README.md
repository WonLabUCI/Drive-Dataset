# DRIVE: Deep Representative Input for Vision Environment in Autonomous Vehicles

## Overview

DRIVE (Deep Representative Input for Vision Environment) is a comprehensive dataset designed for advancing the research and development of autonomous vehicles. This dataset has been meticulously collected by the collaborative efforts of Hyundai Company and the University of California, Irvine (UCI).

## Dataset Description
![https://github.com/WonLabUCI/Drive-Dataset/Projects/Figures/Figure2.png](https://github.com/WonLabUCI/Drive-Dataset/blob/main/Projects/Figures/Figure2.png)

The DRIVE dataset includes a variety of sensor data from different environments(dust and anti-ice mixture) and conditions(sunny, rain, snow), aimed at providing a robust foundation for training and evaluating machine learning models in the context of autonomous driving. The data encompasses: 

- **LiDAR:** The placement of the LiDARs—two on the front bumper, one on the roof, one on each side, and one on the rear—reflects arrangements. It employs commercial 905nm LiDAR sensors, known for their ability to identify objects up to 250 meters away. Each LiDAR unit offers a horizontal field of view (FOV) of 133 degrees and a vertical FOV of 10 degrees, operating at a scan rate of 25 frames per second(fps). This configuration delivers a high resolution of 625 horizontal points across 16 vertical layers, resulting in a data capture rate of 260,800 points per second.
- **Camera:** The vehicle is equipped with 13 supplementary cameras that encompass short, moderate, and long-range views: seven cameras are dedicated to the front, capturing intricate details at various ranges; two side-facing cameras focus on capturing short-range data; and four rear-facing cameras provide short and moderate range coverage. These cameras collectively operate at 10 fps with a resolution of 1920x1080
- **LiDAR Cam:** The LiDAR Cam system is installed to observed the actual condition of the sensor surfaces. It records 30 fps with a resolution of 854x480.
- **Infrared Camera:** The IR camera employs a passive sensor that detects infrared energy, providing superior image quality day and night. This type of camera is highly resilient to environmental factors like dust and rain. In contrast to RGB cameras, IR cameras are robust under light intensity, maintaining consistent image output within tunnels, under direct sunlight, or when confronted with vehicle headlights during nighttime. Due to these inherent features, IR cameras can accurately represent different environmental scenarios, allowing for effective recognition, identification, and response. It can distinguish objects up to a distance of 300 meters. It is an uncooled thermal imaging camera with a resolution of 640x480 and can capture 30 fps. 

## Goals and Applications

The primary objective of the DRIVE dataset is to support research in the following areas:

- **Computer Vision:** Enhancing object detection, recognition, and tracking capabilities.
- **Machine Learning:** Developing and refining algorithms for autonomous navigation and decision-making.
- **Data Analysis:** Exploring correlations between visual data and spatial information to improve sensor fusion techniques.
- **Autonomous Vehicles:** Contributing to the safety and efficiency of self-driving car technologies.

## Collaboration and Contributions

The development of the DRIVE dataset has been a joint effort between Hyundai Company and the University of California, Irvine. Contributions from both industry and academia have been pivotal in ensuring the dataset's quality and relevance.

## How to Use This Dataset

1. **Download the Dataset:** Access the dataset from the provided links and follow the instructions for downloading and organizing the data.
2. **Explore and Visualize:** Utilize the sample scripts and tools provided to explore and visualize the dataset.
3. **Develop and Test Models:** Use the dataset to train and test your machine learning models, leveraging the extensive annotations and sensor data.
4. **Contribute:** We welcome contributions to improve and expand the dataset. Feel free to submit issues or pull requests with your enhancements and findings.
5. 
## Website

For more information, visit our website: [DRIVE Project Website](http://your-website-link.com)

## Acknowledgments

We extend our gratitude to Hyundai Company and the University of California, Irvine, for their support and collaboration in creating this dataset. We also thank the researchers and engineers who have contributed their time and expertise to this project.

## License

DRIVE dataset and codes are released under the Creative Commons Attribution 4.0 International License.
