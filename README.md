# YOLO-MOT17-PedestrianTracking

> A deep learning pipeline for pedestrian and multi-class object tracking using YOLOv8, trained and tested on the MOT17 dataset.  

---

## 🧠 Project Overview

This project demonstrates how to process, train, and evaluate a custom object detection model on the **MOT17 dataset** using **YOLOv8**. The focus is on **pedestrian tracking**, but the pipeline supports 12 object categories including vehicles, bicycles, and occluders.

### Key Features
- 🔧 **Label Preprocessing**: Convert `gt.txt` ground truth annotations to YOLOv8 format.
- 🧠 **Model Training**: Leverage Ultralytics YOLOv8 for training on a custom dataset.
- 📊 **Evaluation**: Analyze detection performance and visualize predictions on video.
- 🎥 **Application-Oriented**: Simulates real-world tracking in urban scenes (occlusion, crowding, motion blur).

---

## 📂 Dataset: MOT17

The [MOT17](https://motchallenge.net/data/MOT17/) dataset includes labeled video sequences with various real-world challenges:
- Crowded pedestrian walkways
- Occlusions and shadows
- Moving vehicles and distractions

| ID | Label                 | Notes                          |
|----|----------------------|--------------------------------|
| 0  | pedestrian           | Main tracking target           |
| 1  | person on vehicle    | Riders on bikes/motorbikes     |
| 2  | car                  | Public and private vehicles     |
| 3  | bicycle              | Bicycles without a rider       |
| 4  | motorbike            | Motorcycles without a rider    |
| 5  | non motorized vehicle | Carts, wheelchairs             |
| 6  | static person        | Sitting or waiting people      |
| 7  | distractor           | Trees, billboards, etc.        |
| 8  | occluder             | Partially blocking objects     |
| 9  | occluder on ground   | Ground-based clutter           |
|10  | occluder full        | Fully blocking objects         |
|11  | reflection           | False positives (glass, etc.)  |

---

## 🚀 How to Run

### 1. Environment Setup
```bash
pip install ultralytics
```bash

✅ Code was developed and tested on Google Colab.

### 2. Prepare Dataset
- Mount Google Drive.
- Copy the MOT17 dataset to your working directory.
- Run the notebook to convert gt.txt into YOLO-format label files.
