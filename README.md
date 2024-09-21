# Diabetic Foot Ulcer Detection Using Thermograms

## Overview

This project aims to detect and classify diabetic foot ulcers (DFUs) using thermograms (thermal images of the plantar region). DFUs are a common complication of diabetes, which can lead to serious consequences such as amputation if not detected early. The project employs deep learning techniques, specifically a Convolutional Neural Network (CNN), to analyze thermograms and predict the presence of ulcers and their severity.

We utilize a multi-class classification system to distinguish between non-diabetic subjects and subjects with different levels of diabetic foot complications, providing early diagnosis without invasive procedures.

## Table of Contents

- [Overview](#overview)
- [Motivation](#motivation)
- [Methodology](#methodology)
- [Dataset](#dataset)
- [Model](#model)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [Contributors](#contributors)
- [License](#license)

## Motivation

Diabetic foot ulcers often go unnoticed due to reduced pain sensitivity in diabetic patients. Early detection through non-invasive methods is crucial to prevent severe complications. Research shows that variations in foot temperature can indicate the development of ulcers. This project aims to leverage these temperature changes using deep learning for automated detection and classification of ulcers.

## Methodology

The approach taken in this project involves the following steps:
1. **Data Collection and Preparation**: Thermograms of the plantar region from diabetic and non-diabetic subjects are processed.
2. **Feature Extraction**: Temperature distributions are analyzed using asymmetrical analysis and temperature distribution analysis.
3. **Model Training**: A CNN model is trained to classify the thermograms into multiple categories based on ulceration severity.
4. **Data Augmentation**: Techniques like image rotation, scaling, and flipping are applied to balance the dataset and avoid overfitting.

## Dataset

The dataset includes thermograms from 167 subjects, divided into:
- **Control Group**: 45 subjects without diabetes.
- **Diabetic Group**: 122 subjects with varying degrees of diabetic foot conditions.

Each thermogram is classified into one of six classes:
- **Class 0**: Non-diabetic (control group).
- **Class 1 to 5**: Diabetic subjects with increasing levels of ulcer severity, based on the Thermal Change Index (TCI).

### Thermal Change Index (TCI)
The TCI is a quantitative index calculated using the temperature difference between the subject's feet and reference values from the control group. It is used to assign the ulcer severity grade.

## Model

The project uses a CNN for classification of thermograms. The CNN model:
- **Input**: Thermograms of diabetic and non-diabetic feet.
- **Output**: Multi-class classification predicting ulcer severity or absence of diabetes.

Techniques such as **data augmentation** and **weighted classification** are used to handle the imbalance in the dataset. 

### Key Features of the Model:
- Non-invasive and autonomous detection of diabetic foot ulcers.
- Multi-class classification of diabetic foot complications.
- Lower computational cost compared to previous studies.

## Results

The model achieves promising results in classifying diabetic foot ulcers:
- **Training Accuracy**: High accuracy was achieved during training.
- **Generalization**: The model generalizes well, though improvements can be made by gathering more data and reducing class imbalance.

### Example Visualizations:
- **Training Accuracy per Epoch**
- **Class Distribution of Thermograms**

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/KVSGVinayak11/Diabetic-Foot-Ulcers-Detection-Using-Thermograms.git
    cd diabetic-foot-ulcer-detection
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the dataset and place it in the `data/` directory.

## Usage

1. **Data Preprocessing**:
   The code for data preprocessing, augmentation, and preparation is included in the `data_preprocessing.py` script.

2. **Training the Model**:
   Train the CNN model using the `train_model.py` script:
   ```bash
   python train_model.py
