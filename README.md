# Object Detection with Camera and Radar Data for Autonomous Vehicles

## Overview
This project implements an **object detection system** by integrating **camera** and **radar data** using **Bird's Eye View Fusion (BEVFusion)**. The goal is to enhance object detection accuracy in autonomous vehicles by leveraging both visual and radar-based spatial information.

## Features
- **Camera Data Processing**: Uses ResNet50 for feature extraction.
- **Radar Data Processing**: Converts radar point cloud to Bird's Eye View (BEV) representation.
- **Fusion Model**: Combines camera and radar features using a deep learning model.
- **Boosting Techniques**: Uses XGBoost for post-processing to improve classification accuracy.
- **Evaluation Metrics**: Accuracy, Precision, Recall, and F1-score.

## Dataset
The dataset consists of:
- **Camera Data**: 198 images of shape `(224, 224, 3)`.
- **Radar Data**: 366,645 radar points converted into BEV representation.
- **Annotations**: JSON files containing ground truth labels.

## Installation
Clone the repository and install dependencies:
```bash
git clone 
cd your-repo https://github.com/tgchandu25/Object-Detection-with-Camera-and-Radar-Data-for-Autonomous-Vehicles/edit/main/README.md
pip install -r requirements.txt
```

## Usage
Run the application:
```bash
python app.py
```
This will process the dataset, train the model, and generate evaluation metrics.

## Model Architecture
1. **Camera Feature Extraction**: ResNet50 without the top layer.
2. **Radar BEV Processing**: Converts radar data to a top-down view.
3. **Fusion**: Combines features using concatenation and attention mechanisms.
4. **Classification**: Uses fully connected layers for object detection.

## Evaluation Results
After model training, the evaluation metrics achieved are:
- **Accuracy**: 85% - 95%
- **Precision**: High precision for object detection.
- **Recall**: Improved recall due to radar integration.
- **F1-score**: Optimal balance between precision and recall.

## Future Improvements
- Use LiDAR data for additional depth information.
- Implement Transformer-based fusion techniques.
- Optimize real-time performance for deployment in autonomous vehicles.



