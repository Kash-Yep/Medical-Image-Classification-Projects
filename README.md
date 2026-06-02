# Medical Image Classification Projects

Machine Learning and Deep Learning projects for medical image classification using SVM, CNN, PCA, Transfer Learning and XGBoost.

---

# Exercise-1: Brain Tumor Detection using SVM + PCA

## Project Description

The objective of this project is to classify MRI brain scans into:

* No Tumor
* Pituitary Tumor
* Glioma Tumor
* Meningioma Tumor

### Method Used

* Image preprocessing
* Image normalization
* PCA dimensionality reduction
* Support Vector Machine (SVM)

---

## Project Files

### Code

[View Notebook on GitHub](https://github.com/Kash-Yep/Medical-Image-Classification-Projects/blob/main/Exersize-1%28BrainTumour-SVM%29/Code/Brain.ipynb)

---

# Results

# Baseline SVM (RBF Kernel)

## Training and Testing Scores

<img src="./Exersize-1(BrainTumour-SVM)/Results/RBF_Baseline/baseline_scores.png" width="800">

---

## Tumor Count

<img src="./Exersize-1(BrainTumour-SVM)/Results/RBF_Baseline/tumor_count_table.png" width="500">

---

## Sample Predictions

### Prediction Set 1

<img src="./Exersize-1(BrainTumour-SVM)/Results/RBF_Baseline/sample_predictions1.png" width="800">

### Prediction Set 2

<img src="./Exersize-1(BrainTumour-SVM)/Results/RBF_Baseline/sample_predictions2.png" width="800">

---

## Histogram

<img src="./Exersize-1(BrainTumour-SVM)/Results/RBF_Baseline/histogram.png" width="700">

---

# Linear Kernel Experiment

## Training and Testing Scores

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/linear_scores.png" width="800">

---

## Tumor Count

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/tumour_count_table.png" width="500">

---

## Sample Predictions

### Prediction Set 1

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/sample_predictions%20(1).png" width="800">

### Prediction Set 2

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/sample_predictions%20(2).png" width="800">

### Prediction Set 3

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/sample_predictions%20(3).png" width="800">

### Prediction Set 4

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/sample_predictions%20(4).png" width="800">

---

## Histogram

<img src="./Exersize-1(BrainTumour-SVM)/Results/Linear_Kernel/histogram.png" width="700">

---

# Training Percentage Experiment

## Training and Testing Scores

<img src="./Exersize-1(BrainTumour-SVM)/Results/Training_Percentage_Experiment/TrainingDataAccuracy.png" width="800">

---

## Tumor Count

<img src="./Exersize-1(BrainTumour-SVM)/Results/Training_Percentage_Experiment/TumorCountTable.png" width="500">

---

## Training vs Accuracy Plot

<img src="./Exersize-1(BrainTumour-SVM)/Results/Training_Percentage_Experiment/accuracy_plot.png" width="800">

---

## RBF Performance Metrics

<img src="./Exersize-1(BrainTumour-SVM)/Results/Training_Percentage_Experiment/rbf_metrics.png" width="800">

---

## Linear Performance Metrics

<img src="./Exersize-1(BrainTumour-SVM)/Results/Training_Percentage_Experiment/linear_Metrics.png" width="800">

---

## Histogram

<img src="./Exersize-1(BrainTumour-SVM)/Results/Training_Percentage_Experiment/Histogram.png" width="700">

---

# Brain Tumor Transfer Learning (MobileNet)

## Project Description

Transfer learning was implemented on the Brain Tumor MRI dataset using MobileNet pretrained on ImageNet.

Objective:

Compare classical ML approaches with transfer learning approaches.

Classes:

* Glioma Tumor
* Meningioma Tumor
* No Tumor
* Pituitary Tumor

---

## Method Used

* Transfer Learning
* MobileNet (ImageNet Pretrained)
* Frozen Feature Extractor
* Multi-Class Classification
* Softmax Output Layer

---

## Project Files

### Code

[View Notebook on GitHub](./Exersize-1%28BrainTumour-SVM%29/Code/BrainTumor_TransferLearning.ipynb)

---

# Results

## Model Summary

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Metrics/Model_Summary.png" width="800">

---

## Training Logs

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Metrics/TransferLearning_Training_Log.png" width="800">

---

## Training vs Validation Accuracy

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Training_Curves/Accuracy.png" width="800">

---

## Training vs Validation Loss

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Training_Curves/Loss.png" width="800">

---

## Confusion Matrix

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Confusion_Matrix/ConfusionMatrix.png" width="700">

---

## Classification Report

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Metrics/Classification_Report.png" width="800">

---

## Sample Predictions

<img src="./Exersize-1(BrainTumour-SVM)/Results/TransferLearning/Sample_Predictions/Sample_Predictions.png" width="900">

---

## Final Performance Summary

* Test Accuracy: 70.56%

* Weighted F1 Score: 68%

* Transfer learning showed strong performance for pituitary and no tumor classes but struggled with glioma classification.

---

# Exercise-2: Chest X-Ray Classification using CNN

## Project Description

The objective of this project is to classify chest X-Ray scans into:

* NORMAL
* PNEUMONIA

### Method Used

* Image preprocessing
* Image normalization
* Data augmentation
* MobileNet CNN Architecture
* Binary Classification
* Model Checkpointing
* Reproducible Training Pipeline

---

## Project Files

### Code

[View Notebook on GitHub](./Exersize-2%28ChestXRay%29/Code/ChestXRay_CNN.ipynb)

---

# Results

# Baseline CNN

## Total Image Count

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Image_Count.png" width="700">

---

## Train Test Validation Split Count

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Split_Count.png" width="700">

---

## Preprocessed Training Images

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Preprocessed_train.png" width="700">

---

## Class Distribution

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Class_Distribution.png" width="800">

---

## Sample Images

### Training Samples

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Sample_Train.png" width="850">

### Testing Samples

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Sample_Test.png" width="850">

### Validation Samples

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Sample_Validation.png" width="850">

---

## Initial CNN Training

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Initial_CNN_Training.png" width="850">

---

## Training and Validation Accuracy

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/TvsV_Accuracy.png" width="850">

---

## Training and Validation Loss

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/TvsV_Loss.png" width="850">

---

## Performance Metrics

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Performance_Metrics.png" width="700">

---

## Confusion Matrix

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/Confusion_Matrix.png" width="700">

---

## ROC Curve

<img src="./Exersize-2(ChestXRay)/Results/Baseline_CNN/ROC_Curve.png" width="700">

---

## Baseline Performance Summary

* Accuracy: 78.35%

* Precision: 95.29%

* Sensitivity (Recall): 72.54%

* Specificity: 91.73%

* F1 Score: 82.37%

* AUC Score: 0.93

---

# Future Work

## Training Percentage Experiments

### 20 Percent Training Data

(To be implemented)

### 40 Percent Training Data

(To be implemented)

### 60 Percent Training Data

(To be implemented)

### 80 Percent Training Data

(To be implemented)

---

## CNN vs SVM Comparison

(To be implemented)

---

## Detailed Final Report

(To be implemented)

---

# Future Exercises

Exercise-3: XGBoost for Medical Image Classification
