# Brain-Tumor-Detection-YOLOv8-KerasCV



This project applies YOLOv8 (XS backbone) using KerasCV to perform brain tumor detection on MRI scans. It leverages the Kaggle dataset “Medical Image DataSet: Brain Tumor Detection” formatted for object detection tasks.



## Project Objectives

Detect presence and location of brain tumors in MRI images
Use a custom-annotated dataset from Kaggle
Evaluate model performance via Mean Average Precision (mAP)
Generate visual outputs displaying detected tumor bounding boxes



## Model Summary

| Component              | Details                                      |
|-----------------------|----------------------------------------------|
|      Dataset          | Kaggle: Medical Image DataSet for Brain Tumor Detection by pkdarabi :contentReference[oaicite:2]{index=2} |
|      Backbone         | `yolo_v8_xs_backbone_coco` (KerasCV)         |
|    Detector Model     | `keras_cv.models.YOLOV8Detector`             |
| Bounding Box Format   | `'xywh'`                                     |
|     Optimizer         | `AdamW`                                      |
| Evaluation Metric     | `MeanAveragePrecision` (mAP)                 |



##  Evaluation

mAP is calculated to assess detection performance, comparing predicted tumor bounding boxes against annotated ground truths.



## Notebook Highlights

Imports: TensorFlow, KerasCV, and utility libraries
Data Preparation: Loads MRI images and bounding box annotations in `xywh` format
Model Construction: Instantiates YOLOv8 XS model
Training Loop: Fits the model on custom MRI dataset
mAP Computation: Utilizes `MeanAveragePrecision` metric
Visualization: Plots predicted tumor bounding boxes on example MRI images



