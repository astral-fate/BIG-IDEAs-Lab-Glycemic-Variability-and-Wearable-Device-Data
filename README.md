[![Paper](https://img.shields.io/badge/arXiv-25XX.XXXXX-b31b1b.svg)](https://arxiv.org/abs/25XX.XXXXX)
[![Code](https://img.shields.io/badge/GitHub-Code-blue)](https://github.com/astral-fate/BIG-IDEAs-Lab-Glycemic-Variability-and-Wearable-Device-Data)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Page-F9D371)](https://huggingface.co/spaces/FatimahEmadEldin/BIG-IDEAs-Lab-Glycemic-Variability-and-Wearable-Device-Data)
[![Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-Hugging%20Face-blue)](https://huggingface.co/datasets/FatimahEmadEldin/BIG-IDEAs-Lab-Glycemic-Variability-and-Wearable-Device-Data)
![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fastral-fate%2FBIG-IDEAs-Lab-Glycemic-Variability-and-Wearable-Device-Data&label=Visitors&countColor=%23697689)

# BIG-IDEAs-Lab-Glycemic-Variability-and-Wearable-Device-Data

## Goal

The goal of this project is to predict glycemic variability using wearable device data. By leveraging machine learning, we aim to provide a non-invasive way to monitor blood glucose levels, which could significantly improve the management of diabetes and pre-diabetes.

## Data Source

The dataset used in this project is the "BIG-IDEAs Lab Glycemic Variability and Wearable Device Data" from PhysioNet. It can be accessed here: [https://physionet.org/content/big-ideas-glycemic-wearable/1.1.2/](https://physionet.org/content/big-ideas-glycemic-wearable/1.1.2/)

The dataset includes the following files for each subject:
* `ACC_001.csv`: Accelerometer/Motion data
* `BVP_001.csv`: Blood Volume Pulse data
* `Dexcom_001.csv`: Glucose data
* `EDA_001.csv`: Electrodermal Activity data
* `Food_Log_001.csv`: Food consumption logs
* `HR_001.csv`: Heart Rate data
* `IBI_001.csv`: Inter-Beat Interval for HRV
* `TEMP_001.csv`: Temperature data

## Feature Engineering

A crucial step in this project was feature engineering, where raw sensor data was transformed into meaningful features for the machine learning model. This process involved:
* **Time-series analysis**: Extracting statistical features from windowed sensor data (e.g., mean, standard deviation, min, max).
* **Lag features**: Creating features that represent past values of the sensor data to capture temporal dependencies.
* **Interaction features**: Combining different sensor data to create new features that might have a stronger predictive power.

## Model Training and Results

The project involved training a machine learning model to predict blood glucose levels based on the engineered features. The model was trained and evaluated, with the following results on the unseen test set:

---
### Clinical Success Metrics
* **MARD (Mean Absolute Relative Difference):** 10.74% (Target: < 10%)
* **Clinical Correlation (R²):** 0.65 (Target: > 0.7)
* **RMSE:** 13.99 mg/dL
---

### Evaluation Plots

**Clarke Error Grid:**
* **Zone A:** 83.21%
* **Zone B:** 16.79%
* **Zones A+B:** 100.00%

<img width="691" height="701" alt="Clarke Error Grid" src="https://github.com/user-attachments/assets/81be48c4-4a2c-4495-9fa5-8b3142fed319" />

<img width="756" height="455" alt="Prediction Plot" src="https://github.com/user-attachments/assets/71135a56-0561-47d1-8f3b-0da84a073a25" />

<img width="1650" height="624" alt="Feature Importance" src="https://github.com/user-attachments/assets/3e895e80-7172-408c-bff8-b543973caccd" />

## Deployment

This model is deployed on Hugging Face Spaces, allowing for an interactive demonstration of its predictive capabilities. You can access the live demo here:

[Hugging Face Space](https://huggingface.co/spaces/FatimahEmadEldin/BIG-IDEAs-Lab-Glycemic-Variability-and-Wearable-Device-Data)
