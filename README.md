### Project Title: Object Detection and Classification Framework for Analysis of Video Data Acquired from Indian Roads

## Overview
This repository contains the implementation of the **Object Detection and Classification Framework for Video Data**. The primary goal of the project is to develop a robust deep learning-based system tailored specifically for object detection and classification on Indian roads, leveraging the **YOLOv8 model**. The system addresses various challenges like complex traffic patterns, erratic driving behaviors, and diverse weather conditions.

## Key Features:
- **Real-time object detection** using YOLOv8 architecture.
- **35 distinct object classes**, including vehicles, pedestrians, and traffic signs specific to Indian road conditions.
- **High accuracy and precision** for object detection under diverse weather and lighting conditions.
- **Scalable and memory-efficient** to ensure deployment feasibility in resource-constrained environments, such as autonomous vehicles.
- Trained on an **Indian Driving Dataset (IDD)** to handle the challenges of Indian roads, such as dense traffic and erratic driver behavior.

## Table of Contents
- [Installation](#installation)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Future Work](#future-work)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/username/repo-name.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure you have the following installed:
   - Python 3.10+
   - PyTorch 2.0+
   - Ultralytics
   - OpenCV for video processing

4. Download the dataset from the link https://data.mendeley.com/datasets/nfc34n8svj/2

## Dataset
We used the **DATS_2022 dataset**, specifically designed for Indian roads, containing:
- 4,296 training images
- 35 distinct classes such as **cars, bikes, rickshaws, pedestrians, cattle**, and more.

The dataset was augmented using techniques such as **rotation, scaling, flipping**, and **brightness adjustments** to ensure model robustness across various environmental conditions like rain, fog, and night-time driving.


## Model Architecture
We used the **YOLOv8 Nano variant**, optimized for real-time performance. The model balances **accuracy** and **computational efficiency**, making it suitable for resource-constrained environments.

**YOLOv8 Features**:
- **PANet** for multi-scale feature fusion, allowing the model to handle objects of varying sizes.
- **Anchor-free detection** for improved object localization.

The system is designed to process video frames in real-time and detect objects by overlaying bounding boxes with associated class labels.

## Training and Evaluation 
For the Process of Training and Evaluation purposes refer to the Train and Eval.ipynb.

# Testing On Various conditions and environments
We ourselves collected various videos for testing and evaluation purposes on realtime environments.
The link to the test dataset is "https://www.kaggle.com/datasets/vivaaniiitdharwad/testing-videos"
## Results
The system demonstrated:
- **Real-time performance** on video streams with an average accuracy of **70%** across various scenarios.
- Peak accuracy of **95%** under optimal conditions.
- Robust detection in adverse weather conditions such as **rain, fog**, and **night**.

Sample results:
1. **Dense Traffic (Day)**: Detected and classified cars, bikes, and pedestrians with high precision.
2. **Rainy Condition**: Classified objects like cars with a slight misclassification but maintained good detection rates.

## Future Work
- **Integration with LiDAR/RADAR**: Enhance object detection in low-visibility scenarios like night or fog.
- **3D bounding box** support for better depth estimation in autonomous driving.
- **Dataset expansion** to include more challenging environments and rare object classes.

