# Medical Image Classification using Classical Machine Learning and Deep Learning

---

# Abstract

Medical image classification has become an important research area due to its applications in automated disease detection and clinical decision support systems. This project investigates the application of classical machine learning and deep learning approaches for medical image classification using Brain Tumor MRI images and Chest X-Ray images.

Multiple classification pipelines were implemented and compared, including Support Vector Machines (SVM), Principal Component Analysis (PCA), Convolutional Neural Networks (CNN), Transfer Learning, and later XGBoost-based approaches.

The study evaluates how different learning methods behave under varying amounts of training data while maintaining fixed testing datasets to ensure fair evaluation. Performance comparison is conducted using metrics such as accuracy, F1-score, sensitivity, specificity, confusion matrices, and ROC analysis.

The results demonstrate the importance of feature representation, dataset size, and deep learning techniques in medical image classification problems.

---

# Introduction

Medical imaging plays a critical role in modern healthcare systems by enabling early diagnosis and treatment planning. However, manual analysis of medical images can be time-consuming and may be affected by subjective interpretation.

Machine learning and deep learning techniques provide opportunities for automated medical image analysis by learning discriminative patterns directly from imaging data.

This project investigates multiple approaches for solving medical image classification problems using two datasets:

* Brain Tumor MRI Dataset
* Chest X-Ray Pneumonia Dataset

The work progressively explores traditional machine learning methods, dimensionality reduction techniques, deep learning architectures, transfer learning methods, and feature-engineering approaches.

Special emphasis is placed on understanding how different models respond to increasing training data and comparing their ability to generalize to unseen medical images.

---

# Objectives

The primary objectives of this project are:

* Implement Support Vector Machine based medical image classification
* Study the effect of PCA dimensionality reduction
* Compare Linear and RBF kernel performance
* Implement CNN based image classification pipelines
* Apply Transfer Learning using pretrained architectures
* Compare classical machine learning and deep learning approaches
* Analyze model behavior using varying training dataset sizes
* Evaluate performance using multiple classification metrics
* Study generalization capability using fixed testing datasets

---

# Datasets Used

Two medical imaging datasets were used throughout this project to study the behavior of machine learning and deep learning approaches across different classification problems.

---

## Brain Tumor MRI Dataset

The Brain Tumor MRI dataset was used for Exercise-1 and consists of MRI images belonging to multiple tumor categories.

### Dataset Classes

* No Tumor
* Glioma Tumor
* Meningioma Tumor
* Pituitary Tumor

### Applications in This Project

The dataset was used for:

* PCA + SVM Classification
* Linear SVM Classification
* RBF Kernel SVM Classification
* Training Percentage Experiments
* Transfer Learning using MobileNet
* Comparative Analysis

The dataset presents a multi-class classification problem where the objective is to classify MRI images into their respective tumor categories.

---

## Chest X-Ray Pneumonia Dataset

The Chest X-Ray dataset was used for Exercise-2 and consists of binary classification of chest X-ray images.

### Dataset Classes

* NORMAL
* PNEUMONIA

### Dataset Statistics

| Category         | Number of Images |
| ---------------- | ---------------: |
| NORMAL Images    |             1583 |
| PNEUMONIA Images |             4273 |
| Total Images     |             5856 |

### Dataset Split Used

| Dataset Portion   | Number of Images |
| ----------------- | ---------------: |
| Training Images   |             4642 |
| Testing Images    |              919 |
| Validation Images |              295 |

### Applications in This Project

The dataset was used for:

* Linear SVM Classification
* CNN Classification
* MobileNet Based Transfer Learning
* Training Percentage Experiments
* CNN vs SVM Comparative Analysis

The testing dataset remained fixed across experiments to ensure fair performance comparison and avoid data leakage.

---

# Evaluation Metrics

Multiple evaluation metrics were used to analyze model performance comprehensively.

## Accuracy

Accuracy measures the proportion of correctly classified samples.

Accuracy is defined as:

Accuracy = Correct Predictions / Total Predictions

Higher accuracy indicates better overall classification performance.

---

## F1 Score

F1 Score measures the balance between precision and recall.

F1 Score becomes particularly important when datasets are imbalanced.

---

## Sensitivity (Recall)

Sensitivity measures the ability of the model to correctly identify positive cases.

For medical applications, sensitivity is important because missing positive disease cases may lead to severe consequences.

---

## Specificity

Specificity measures the ability of the model to correctly identify negative cases.

Higher specificity reduces false positive predictions.

---

## Confusion Matrix

Confusion matrices were used to visualize:

* True Positives
* True Negatives
* False Positives
* False Negatives

This provides deeper insight into model behavior beyond accuracy alone.

---

## ROC Curve

Receiver Operating Characteristic (ROC) curves were used to evaluate classifier performance across different classification thresholds.

ROC analysis helps understand the tradeoff between:

* True Positive Rate
* False Positive Rate

---

# Exercise-1: Brain Tumor Classification using SVM and Transfer Learning

## Problem Statement

The objective of Exercise-1 is to classify brain MRI images into multiple tumor categories using classical machine learning and deep learning approaches.

The study investigates:

* Support Vector Machine (SVM) classification using PCA-based feature reduction
* Comparison between Linear and RBF kernels
* Effect of varying training dataset size
* Transfer learning using MobileNet architecture

The goal is to understand how feature extraction methods and classification algorithms influence medical image classification performance.

---

## Dataset Description

The Brain Tumor MRI dataset consists of MRI images categorized into four classes.

### Dataset Classes

* No Tumor
* Glioma Tumor
* Meningioma Tumor
* Pituitary Tumor

### Nature of Problem

* Multi-class Classification Problem
* Medical Image Classification Task
* Supervised Learning Problem

### Applications in This Exercise

The dataset was used for:

* PCA + SVM Classification
* Linear Kernel SVM
* RBF Kernel SVM
* Training Percentage Experiments
* MobileNet Transfer Learning

---

## Methodology

The overall workflow used in Exercise-1 is shown below:

MRI Images
    ↓
Image Preprocessing
    ↓
Feature Extraction / PCA
    ↓
Classification Model
    ↓
Evaluation Metrics


### Data Preprocessing

The following preprocessing steps were performed:

* Images converted into grayscale format
* Images resized into fixed dimensions
* Pixel normalization performed
* Images converted into numerical arrays for model input

### PCA Dimensionality Reduction

Principal Component Analysis (PCA) was used to reduce feature dimensionality before training SVM models.

Advantages of PCA:

* Reduces computational complexity
* Removes redundant features
* Reduces overfitting
* Preserves major variance information

### SVM Classification Pipeline

The SVM pipeline consisted of:

MRI Image
    ↓
Preprocessing
    ↓
Flattening
    ↓
PCA
    ↓
SVM Classifier


Two kernel types were investigated:

#### RBF Kernel

Characteristics:

* Captures nonlinear decision boundaries
* More flexible classification boundary
* Higher computational complexity

#### Linear Kernel

Characteristics:

* Faster training time
* Simpler decision boundary
* Lower computational complexity


---

## Baseline Results

Two SVM kernel configurations were investigated for baseline performance:

* RBF Kernel
* Linear Kernel

The objective was to study how nonlinear and linear decision boundaries influence brain tumor classification performance.

---

## Baseline SVM (RBF Kernel)

The RBF kernel was selected because medical image data often contains nonlinear feature relationships.

### Performance Summary

| Metric            |  Value |
| ----------------- | -----: |
| Training Accuracy | 96.47% |
| Testing Accuracy  | 83.10% |
| F1 Score          |  80.7% |
| Sensitivity       | 81.01% |
| Specificity       | 93.55% |

### Observations

* High training accuracy suggests strong learning capability
* RBF kernel successfully captures nonlinear feature relationships
* Testing performance indicates good generalization ability
* Slight performance gap between training and testing suggests moderate overfitting

---

## Baseline SVM (Linear Kernel)

Linear kernels were investigated to understand whether simpler decision boundaries can sufficiently separate tumor classes.

### Performance Summary

| Metric            |   Value |
| ----------------- | ------: |
| Training Accuracy | 100.00% |
| Testing Accuracy  |  80.14% |
| F1 Score          |  79.57% |
| Sensitivity       |  80.14% |
| Specificity       |  93.30% |

### Observations

* Linear kernel achieved perfect training accuracy
* Slight reduction in testing performance compared to RBF
* Simpler decision boundary may limit classification capability
* Computational complexity is lower compared to nonlinear kernels

---

# Kernel Comparison

The performance of Linear and RBF kernels was compared to understand how kernel selection influences classification performance.

## Comparison Table

| Metric            | RBF Kernel | Linear Kernel |
| ----------------- | ---------: | ------------: |
| Training Accuracy |     96.47% |       100.00% |
| Testing Accuracy  |     83.10% |        80.14% |
| F1 Score          |      80.7% |        79.57% |
| Sensitivity       |     81.01% |        80.14% |
| Specificity       |     93.55% |        93.30% |

## Discussion

The RBF kernel slightly outperformed the Linear kernel during testing.

Possible reasons include:

* MRI image features may not be linearly separable
* Nonlinear kernels can capture more complex feature relationships
* PCA reduces dimensionality but may still preserve nonlinear structures

Although Linear SVM achieved higher training accuracy, the RBF kernel produced better testing performance, suggesting improved generalization.

---

# Training Percentage Experiments

The objective of these experiments was to investigate how model performance changes as the amount of available training data increases.

The testing dataset remained fixed throughout all experiments to ensure fair comparison.

Training dataset percentages investigated:

* 20%
* 40%
* 60%
* 80%

---

## Experimental Results

| Training Percentage | RBF Accuracy | Linear Accuracy |
| ------------------- | -----------: | --------------: |
| 20%                 |       67.77% |          71.95% |
| 40%                 |       73.69% |          74.74% |
| 60%                 |       77.35% |          78.57% |
| 80%                 |       80.14% |          81.01% |

---

## 20 Percent Training Data

Training Samples Used:

**459 Samples**

Results:

| Kernel | Training Accuracy | Testing Accuracy |
| ------ | ----------------: | ---------------: |
| RBF    |            94.34% |           67.77% |
| Linear |           100.00% |           71.95% |

Observation:

* Limited training data reduces generalization capability
* Linear kernel performs better under low data availability
* RBF struggles with insufficient data

---

## 40 Percent Training Data

Training Samples Used:

**918 Samples**

Results:

| Kernel | Training Accuracy | Testing Accuracy |
| ------ | ----------------: | ---------------: |
| RBF    |            94.34% |           73.69% |
| Linear |           100.00% |           74.74% |

Observation:

* Both models improved compared to 20%
* Increased data improved feature representation
* Linear kernel continued to maintain higher accuracy

---

## 60 Percent Training Data

Training Samples Used:

**1377 Samples**

Results:

| Kernel | Training Accuracy | Testing Accuracy |
| ------ | ----------------: | ---------------: |
| RBF    |            94.92% |           77.35% |
| Linear |           100.00% |           78.57% |

Observation:

* Significant improvement observed
* Additional training samples improve decision boundaries
* Gap between kernels becomes smaller

---

## 80 Percent Training Data

Training Samples Used:

**1836 Samples**

Results:

| Kernel | Training Accuracy | Testing Accuracy |
| ------ | ----------------: | ---------------: |
| RBF    |            95.75% |           80.14% |
| Linear |           100.00% |           81.01% |

Observation:

* Highest performance achieved at largest dataset size
* Linear kernel slightly outperformed RBF
* Both models benefited from additional training data

---

## Overall Trend Analysis

Several important observations can be made:

* Performance improved consistently with additional training data
* Both kernels benefit from larger datasets
* Linear kernel performed slightly better across most experiments
* RBF kernel showed larger improvement between smaller and larger datasets
* Larger training datasets improved generalization capability

The experiments demonstrate the importance of dataset size in medical image classification problems.

---

## Training Percentage Conclusion

Increasing training data improved performance for both kernels.

The Linear kernel consistently achieved slightly higher testing accuracy, suggesting that PCA-transformed features may have become sufficiently linearly separable.

However, both kernels demonstrated clear dependence on training dataset size.

---

# Transfer Learning (MobileNet)

Transfer learning was implemented to compare classical machine learning approaches with deep learning based feature extraction methods.

Instead of training a CNN from scratch, a pretrained MobileNet architecture was used.

The motivation behind transfer learning is that pretrained models can reuse previously learned visual features and adapt them for medical imaging tasks.

---

## Methodology

The transfer learning pipeline used the following workflow:

MRI Images
    ↓
Resize and Preprocessing
    ↓
MobileNet Feature Extractor
    ↓
Dense Classification Layer
    ↓
Softmax Output


### Model Configuration

* MobileNet pretrained on ImageNet
* Frozen feature extraction layers
* Custom classification head
* Multi-class classification output
* Softmax activation function

### Model Statistics

| Parameter                |     Value |
| ------------------------ | --------: |
| Total Parameters         | 3,232,964 |
| Trainable Parameters     |     4,100 |
| Non-Trainable Parameters | 3,228,864 |

The majority of network weights were frozen to reduce computational cost and overfitting.

---

## Training Results

Training curves demonstrated steady learning behavior.

### Training Behavior

Observations from training logs:

* Training accuracy increased from approximately 56% to over 90%
* Validation accuracy improved steadily during training
* Validation loss decreased initially before slight fluctuations appeared
* Training loss consistently decreased throughout training

This indicates successful convergence of the transfer learning model.

---

## Final Performance Summary

| Metric            |  Value |
| ----------------- | -----: |
| Test Accuracy     | 70.56% |
| Weighted F1 Score |    68% |

### Class-wise Observations

* Pituitary tumors achieved strong classification performance
* No tumor images were classified relatively well
* Meningioma showed moderate performance
* Glioma classification remained difficult

The confusion matrix indicates that glioma samples were frequently confused with other tumor categories.

---

## Observations

Several observations can be made regarding transfer learning performance:

* Transfer learning reduced the amount of trainable parameters significantly
* MobileNet learned meaningful MRI features despite limited training
* Training convergence occurred rapidly
* Performance remained lower than expected for glioma classification
* Frozen feature extraction reduced computational requirements

Although transfer learning simplified model training, medical image classification remains challenging due to inter-class similarity between tumor categories.

---

## Exercise-1 Observations

Important conclusions from Exercise-1:

* Dataset size significantly influenced classification performance
* PCA + SVM approaches produced competitive results
* Linear kernels performed slightly better during training percentage experiments
* Transfer learning reduced feature engineering requirements
* Different tumor classes exhibit varying classification difficulty

Exercise-1 demonstrates that both classical machine learning and deep learning approaches can achieve meaningful performance for medical image classification tasks.

---


---

# Exercise-2: Chest X-Ray Classification using SVM and CNN

## Problem Statement

The objective of Exercise-2 is to classify Chest X-Ray images into Normal and Pneumonia categories using both classical machine learning and deep learning approaches.

The study investigates:

- Support Vector Machine (SVM) based classification
- Convolutional Neural Network (CNN) based classification
- Transfer Learning using MobileNet
- Effect of varying training dataset size
- Comparative analysis between machine learning and deep learning approaches

The goal is to understand how different classification techniques perform for automated pneumonia detection using chest radiographs.

---

## Dataset Description

The Chest X-Ray dataset consists of chest radiographs belonging to two classes.

### Dataset Classes

- NORMAL
- PNEUMONIA

### Nature of Problem

- Binary Classification Problem
- Medical Image Classification Task
- Supervised Learning Problem

### Dataset Statistics

| Category | Number of Images |
|---------|---------:|
| Normal Images | 1583 |
| Pneumonia Images | 4273 |
| Total Images | 5856 |

### Dataset Split

| Dataset Portion | Number of Images |
|---------|---------:|
| Training Images | 4642 |
| Testing Images | 919 |
| Validation Images | 295 |

### Applications in This Exercise

The dataset was used for:

- Linear SVM Classification
- CNN Classification
- MobileNet Transfer Learning
- Training Percentage Experiments
- CNN vs SVM Comparative Analysis

The testing dataset remained fixed throughout experiments to ensure fair evaluation and avoid data leakage.

---

## Methodology

The overall workflow used in Exercise-2 is shown below:

Chest X-Ray Images
↓
Image Preprocessing
↓
Feature Extraction / CNN Features
↓
Classification Model
↓
Performance Evaluation

### Data Preprocessing

The following preprocessing steps were performed:

- Images resized into fixed dimensions
- Pixel normalization performed
- Images converted into numerical arrays
- Training, testing, and validation datasets created
- Binary labels assigned for Normal and Pneumonia classes

### SVM Pipeline

The SVM workflow consisted of:

Chest X-Ray Images
↓
Preprocessing
↓
Flattening
↓
Feature Extraction
↓
SVM Classifier

Characteristics:

- Classical machine learning approach
- Faster training compared to deep networks
- Lower computational requirements
- Used as baseline comparison model

### CNN Pipeline

The CNN workflow consisted of:

Chest X-Ray Images
↓
Convolution Layers
↓
Pooling Layers
↓
Feature Maps
↓
Dense Layers
↓
Binary Classification Output

Characteristics:

- Automatic feature extraction
- Learns spatial image patterns
- More computationally intensive
- Better suited for image classification tasks

### MobileNet Architecture

Transfer learning was implemented using MobileNet architecture.

Workflow:

Chest X-Ray Images
↓
Pretrained MobileNet Feature Extractor
↓
Custom Classification Head
↓
Binary Output Layer

Characteristics:

- Uses pretrained image features
- Reduced training time
- Lower trainable parameters
- Better computational efficiency

---

## Baseline SVM Results

The baseline SVM experiment was conducted to evaluate classical machine learning performance on Chest X-Ray classification.

### Dataset Characteristics

The dataset showed significant class imbalance.

| Class | Number of Images |
|------|------|
| NORMAL | 1341 |
| PNEUMONIA | 3875 |

This imbalance creates additional challenges because models may become biased toward the majority class.

### Baseline Linear SVM Performance

The Linear SVM classifier was trained after image preprocessing and feature extraction.

Results obtained:

| Metric | Value |
|------|------|
| Training Accuracy | 100% |
| Testing Accuracy | 75.00% |

Observation:

- Linear SVM achieved perfect training accuracy.
- However, testing performance dropped considerably.
- This indicates overfitting where the classifier learns training samples well but generalizes poorly.

### Baseline RBF SVM Performance

Results obtained:

| Metric | Value |
|------|------|
| Training Accuracy | 99.21% |
| Testing Accuracy | 77.72% |

Observation:

- RBF kernel produced higher testing accuracy compared to Linear SVM.
- Nonlinear decision boundaries improved classification performance.
- However, the large difference between training and testing performance suggests overfitting still exists.

### Baseline SVM Analysis

Key observations:

- RBF Kernel outperformed Linear Kernel
- Dataset imbalance likely affected classifier performance
- Both models exhibited signs of overfitting
- Classical machine learning methods showed limited generalization capability for medical image classification tasks

The baseline experiments motivated the use of deep learning based approaches for improved feature extraction and classification performance.

---

## Baseline CNN Results

A baseline Convolutional Neural Network (CNN) was implemented to investigate whether deep learning based feature extraction could outperform classical machine learning approaches for Chest X-Ray classification.

### Dataset Characteristics

The Chest X-Ray dataset is highly imbalanced.

| Class | Number of Images |
|------|------|
| NORMAL | 1583 |
| PNEUMONIA | 4273 |
| Total Images | 5856 |

This imbalance creates challenges because the model may become biased toward the majority class.

### Training Performance

The CNN model was trained using training and validation datasets while monitoring accuracy and loss across epochs.

Training results:

| Metric | Value |
|------|------|
| Training Accuracy | 92.46% |

The model successfully learned discriminative image features and achieved high training performance.

### Test Performance

The confusion matrix obtained on the testing dataset is:


[[255 23]
 [176 465]]


Performance metrics obtained:

| Metric | Value |
|------|------|
| Accuracy | 78.35% |
| Precision | 95.29% |
| Sensitivity (Recall) | 72.54% |
| Specificity | 91.73% |
| F1 Score | 82.37% |

### Interpretation of Results

The baseline CNN produced higher classification performance than baseline SVM models.

Important observations:

- High precision indicates strong reliability when predicting pneumonia cases
- Recall is comparatively lower, meaning some pneumonia cases were still missed
- High specificity indicates strong performance for identifying normal patients
- The difference between training and testing accuracy suggests moderate overfitting

### Baseline CNN Analysis

Key observations:

- CNN outperformed classical SVM approaches
- Deep learning enabled better automatic feature extraction
- Dataset imbalance still affected classification behavior
- CNN demonstrated stronger generalization capability compared to baseline machine learning approaches
---

## CNN Training Percentage Experiments

### 20 Percent Training Data

The first experiment investigated CNN performance using only 20% of the available training dataset.

### Dataset Statistics

| Parameter | Value |
|------|------|
| Original Training Samples | 4640 |
| Training Samples Used | 928 |
| Total Images | 5860 |
| Pneumonia Images | 4275 |
| Normal Images | 1585 |
| Test Images | 919 |
| Validation Images | 299 |

### Training Performance

| Metric | Value |
|------|------|
| Training Accuracy | 89.87% |

### Test Performance

Performance metrics:

| Metric | Value |
|------|------|
| Accuracy | 69.75% |
| Precision | 69.75% |
| Sensitivity (Recall) | 100.00% |
| Specificity | 0.00% |
| F1 Score | 82.18% |

Alternative evaluation metrics obtained:

| Metric | Value |
|------|------|
| Accuracy | 85.85% |
| Precision | 92.94% |
| Sensitivity | 86.27% |
| Specificity | 84.89% |
| F1 Score | 89.48% |

### Observations

Important observations:

- Performance using only 20% training data was unstable
- Very high recall combined with zero specificity suggests strong class bias toward pneumonia predictions
- Limited training data reduced model generalization capability
- Dataset imbalance strongly affected learning behavior
- Additional training data is expected to improve feature learning and reduce prediction bias

---

### 40 Percent Training Data

The second experiment evaluated CNN performance using 40% of the available training dataset.

### Dataset Statistics

| Parameter | Value |
|------|------|
| Original Training Samples | 4640 |
| Training Samples Used | 1856 |

### Training Performance

| Metric | Value |
|------|------|
| Training Accuracy | 91.33% |

### Test Performance

Confusion Matrix:

[[0 278]
 [0 641]]


Performance Metrics:

| Metric | Value |
|------|------|
| Accuracy | 69.75% |
| Precision | 69.75% |
| Sensitivity (Recall) | 100.00% |
| Specificity | 0.00% |
| F1 Score | 82.18% |

Additional Evaluation Metrics:

| Metric | Value |
|------|------|
| Accuracy | 85.85% |
| Precision | 92.94% |
| Sensitivity | 86.27% |
| Specificity | 84.89% |
| F1 Score | 89.48% |

### ROC Analysis

The ROC curve appeared approximately diagonal.

This indicates:

- Weak class separation capability
- Poor threshold discrimination
- Significant bias toward the majority class

### Observations

Important observations:

- Increasing training data improved training accuracy slightly
- The model still suffered severe class imbalance issues
- Predictions remained strongly biased toward pneumonia classification
- Additional training data alone was insufficient to completely solve imbalance problems

---

### 60 Percent Training Data

The third experiment evaluated CNN performance using 60% of the available training dataset.

### Training Performance

| Metric | Value |
|------|------|
| Training Accuracy | 91.74% |

### Test Performance

Confusion Matrix:

```
[[194 84]
 [ 74 567]]
```

Performance Metrics:

| Metric | Value |
|------|------|
| Accuracy | 82.81% |
| Precision | 87.10% |
| Sensitivity (Recall) | 88.46% |
| Specificity | 69.78% |
| F1 Score | 87.77% |

Additional Evaluation Metrics:

| Metric | Value |
|------|------|
| Accuracy | 85.85% |
| Precision | 92.94% |
| Sensitivity | 86.27% |
| Specificity | 84.89% |
| F1 Score | 89.48% |

### Observations

Important observations:

- Significant improvement compared to the 20% and 40% experiments
- The model successfully learned features from both classes
- Specificity improved substantially, indicating better recognition of normal X-rays
- Recall remained high, demonstrating strong pneumonia detection capability
- The confusion matrix became more balanced, indicating reduced class bias

### Interpretation

This experiment represents the point where the CNN begins to fully benefit from increased training data.

Unlike the 20% and 40% experiments, the network no longer predicts a single dominant class and instead learns meaningful visual patterns associated with both Normal and Pneumonia cases.

---

### 80 Percent Training Data

The final experiment evaluated CNN performance using 80% of the available training dataset.

### Training Performance

| Metric | Value |
|------|------|
| Training Accuracy | 93.13% |

### Test Performance

Confusion Matrix:

```
[[225 53]
 [ 83 558]]
```

Performance Metrics:

| Metric | Value |
|------|------|
| Accuracy | 85.20% |
| Precision | 91.33% |
| Sensitivity (Recall) | 87.05% |
| Specificity | 80.94% |
| F1 Score | 89.14% |

Additional Evaluation Metrics:

| Metric | Value |
|------|------|
| Accuracy | 85.85% |
| Precision | 92.94% |
| Sensitivity | 86.27% |
| Specificity | 84.89% |
| F1 Score | 89.48% |

### Observations

Important observations:

- Highest classification accuracy achieved among all CNN experiments
- Strong balance between sensitivity and specificity
- Improved identification of both Normal and Pneumonia cases
- Reduced false positives and false negatives
- Demonstrated strong generalization capability

### Interpretation

The CNN benefited significantly from additional training data.

The model achieved:

- Higher accuracy
- Better class balance
- Improved specificity
- Strong pneumonia detection capability

These results demonstrate that CNN performance scales effectively with increasing dataset size.

---

## CNN Training Percentage Experiment Analysis

The effect of training dataset size on CNN performance is summarized below.

| Training Data | CNN Accuracy |
|------|------:|
| 20% | 69.75% |
| 40% | 69.75% |
| 60% | 82.81% |
| 80% | 85.20% |

### Trend Analysis

Several important observations can be made:

- CNN performance remained poor when only 20% and 40% of the training data were used.
- Severe class imbalance caused the model to predict pneumonia for most test samples.
- A substantial improvement occurred between 40% and 60% training data.
- The highest performance was achieved using 80% of the available training dataset.
- CNN models benefited significantly from additional training samples.

### Conclusion

Unlike classical machine learning methods, CNNs rely heavily on large amounts of training data.

The experiments demonstrate that CNN performance scales strongly with dataset size and eventually surpasses traditional machine learning approaches when sufficient data becomes available.

---

## CNN vs Linear SVM Comparison

The performance of CNN and Linear SVM models was compared across different training dataset sizes to understand how each approach responds to increasing amounts of training data.

### Accuracy Comparison

| Training Data | CNN Accuracy | Linear SVM Accuracy |
| ------------- | -----------: | ------------------: |
| 20%           |       69.75% |              74.36% |
| 40%           |       69.75% |              74.04% |
| 60%           |       82.81% |              73.72% |
| 80%           |       85.20% |              75.00% |

### Comparison Discussion

At lower training dataset sizes (20% and 40%), Linear SVM achieved higher accuracy than CNN.

This is expected because:

* SVM requires fewer training samples
* SVM relies on handcrafted feature representations
* CNN requires larger datasets to learn meaningful image features

However, as training data increased, CNN performance improved significantly.

At:

* 60% training data, CNN surpassed Linear SVM
* 80% training data, CNN achieved its highest accuracy of 85.20%

The results demonstrate that CNN models benefit substantially from additional training data, whereas Linear SVM performance remains relatively stable.

These findings highlight the difference between classical machine learning and deep learning approaches for medical image classification.


---

## Exercise-2 Observations

The following observations were made from the Chest X-Ray classification experiments:

* The dataset exhibited significant class imbalance, with Pneumonia images greatly outnumbering Normal images.
* Baseline SVM models achieved moderate performance but showed signs of overfitting.
* The RBF kernel performed slightly better than the Linear kernel.
* The baseline CNN outperformed the baseline SVM models.
* CNN performance was strongly dependent on training dataset size.
* At 20% and 40% training data, the CNN frequently predicted the majority class, resulting in poor specificity.
* Significant performance improvement occurred between 40% and 60% training data.
* The highest CNN accuracy was achieved using 80% of the available training dataset.
* Linear SVM performed better when training data was limited.
* CNN surpassed Linear SVM once sufficient training data became available.

### Exercise-2 Conclusion

The experiments demonstrate that classical machine learning methods can be effective when training data is limited. However, deep learning approaches such as CNNs become increasingly advantageous as larger datasets become available.

For Chest X-Ray classification, CNN achieved the best overall performance and demonstrated superior scalability with increasing training data.


---

# Exercise-3: XGBoost-Based Medical Image Classification

## Problem Statement

The objective of Exercise-3 was to investigate the effectiveness of gradient boosting techniques for medical image classification and compare their performance against the Support Vector Machine (SVM) and Convolutional Neural Network (CNN) models developed in previous exercises.

Three different approaches were implemented:

* Original XGBoost
* PCA + XGBoost
* VGG16 + XGBoost

The experiments were performed on both:

* Brain Tumor MRI Dataset
* Chest X-Ray Pneumonia Dataset

The impact of training dataset size was also studied using 20%, 40%, 60%, and 80% of the available training data while maintaining a fixed testing dataset.

---

## Motivation

Although SVM and CNN models achieved promising performance in previous exercises, they exhibit certain limitations.

Classical machine learning models rely heavily on handcrafted features and dimensionality reduction techniques, while deep learning models often require large datasets and significant computational resources.

XGBoost offers several advantages:

* High classification performance
* Robustness against overfitting
* Ability to handle high-dimensional features
* Fast training and inference

Combining XGBoost with PCA and VGG16 feature extraction enables investigation of hybrid approaches that integrate deep feature learning with gradient boosting classification.

---

# Methodology

## Original XGBoost

The baseline XGBoost approach uses flattened image features directly as input.

### Workflow

Image → Preprocessing → Flattening → XGBoost Classifier → Prediction

### Advantages

* Simple implementation
* Fast training
* Strong baseline performance

### Limitations

* Raw pixel values may contain redundant information
* High-dimensional feature space

---

## PCA + XGBoost

Principal Component Analysis was applied before classification.

### Workflow

Image → Preprocessing → Flattening → PCA → XGBoost → Prediction

### Advantages

* Reduced dimensionality
* Noise reduction
* Lower computational complexity

### Limitations

* Potential loss of information
* Linear dimensionality reduction

---

## VGG16 + XGBoost

Deep features were extracted using the pretrained VGG16 architecture.

### Workflow

Image → Preprocessing → VGG16 Feature Extraction → Feature Vector → XGBoost → Prediction

### Advantages

* Rich feature representation
* Transfer learning benefits
* Better feature discrimination

### Limitations

* Higher computational cost
* Additional feature extraction stage

---

# Brain Tumor MRI Classification

## Dataset Description

The Brain Tumor MRI dataset consists of four classes:

* No Tumor
* Glioma
* Meningioma
* Pituitary Tumor

This is a multi-class classification problem.

---

## Original XGBoost Results

### Performance Summary

| Metric   |  Value |
| -------- | -----: |
| Accuracy | 89.55% |

### Observations

The baseline XGBoost model achieved strong performance despite using only flattened image features.

The results indicate that gradient boosting can effectively learn discriminative patterns from medical image data.

---

## PCA + XGBoost Results

### Performance Summary

| Metric   |  Value |
| -------- | -----: |
| Accuracy | 90.07% |

### Observations

PCA improved performance slightly by removing redundant information and reducing feature dimensionality.

The improvement suggests that dimensionality reduction can enhance XGBoost classification performance.

---

## VGG16 + XGBoost Results

### Performance Summary

| Metric   |  Value |
| -------- | -----: |
| Accuracy | 90.42% |

### Observations

The VGG16 feature extractor provided richer image representations and achieved the highest classification accuracy.

Deep features improved class separability and overall model performance.

---

## Brain Tumor Comparison

| Model            | Accuracy |
| ---------------- | -------: |
| Original XGBoost |   89.55% |
| PCA + XGBoost    |   90.07% |
| VGG16 + XGBoost  |   90.42% |

### Discussion

The results demonstrate that feature quality plays a significant role in classification performance.

The VGG16-based hybrid model achieved the best results because deep convolutional networks extract more meaningful visual features than raw pixels or PCA-transformed features.

---

# Chest X-Ray Classification

## Dataset Description

The Chest X-Ray dataset consists of two classes:

* Normal
* Pneumonia

This is a binary classification problem.

---

## Original XGBoost Results

### Performance Summary

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 73.88% |
| F1 Score    | 69.58% |
| Sensitivity | 73.88% |
| Specificity | 65.51% |

### Confusion Matrix

```
[[75 159]
 [ 4 386]]
```

### Observations

The model achieved high pneumonia recall but struggled to correctly classify normal images.

---

## PCA + XGBoost Results

### Performance Summary

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 75.48% |
| F1 Score    | 72.32% |
| Sensitivity | 75.48% |
| Specificity | 68.08% |

### Confusion Matrix

```
[[90 144]
 [ 9 381]]
```

### Observations

PCA improved classification performance and increased specificity compared to the baseline model.

---

## VGG16 + XGBoost Results

### Performance Summary

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 76.92% |
| F1 Score    | 73.75% |
| Sensitivity | 76.92% |
| Specificity | 69.40% |

### Confusion Matrix

```
[[92 142]
 [ 2 388]]
```

### Observations

The VGG16 feature extractor produced the best overall results.

The model achieved stronger discrimination between Normal and Pneumonia classes while maintaining high recall.

---

## Chest X-Ray Comparison

| Model            | Accuracy | F1 Score | Specificity |
| ---------------- | -------: | -------: | ----------: |
| Original XGBoost |   73.88% |   69.58% |      65.51% |
| PCA + XGBoost    |   75.48% |   72.32% |      68.08% |
| VGG16 + XGBoost  |   76.92% |   73.75% |      69.40% |

---

## Training Percentage Experiments

The effect of training dataset size was investigated using 20%, 40%, 60%, and 80% of the available training data.

### Original XGBoost

| Training % | Accuracy |
| ---------- | -------: |
| 20%        |   72.12% |
| 40%        |   72.92% |
| 60%        |   73.24% |
| 80%        |   73.40% |

### PCA + XGBoost

| Training % | Accuracy |
| ---------- | -------: |
| 20%        |   71.15% |
| 40%        |   73.88% |
| 60%        |   74.84% |
| 80%        |   75.32% |

### VGG16 + XGBoost

| Training % | Accuracy |
| ---------- | -------: |
| 20%        |   74.36% |
| 40%        |   76.28% |
| 60%        |   77.24% |
| 80%        |   76.92% |

### Discussion

Several important observations can be made:

* Accuracy improved as more training data became available.
* PCA consistently improved XGBoost performance.
* VGG16 + XGBoost achieved the highest performance at every training percentage.
* The largest gains occurred between 20% and 60% training data.
* Additional training data improved model generalization and reduced classification errors.

---

## Exercise-3 Conclusion

The experiments demonstrate that XGBoost is an effective classifier for medical image classification.

Important findings include:

* PCA improves XGBoost performance by reducing feature redundancy.
* Deep feature extraction significantly improves classification performance.
* VGG16 + XGBoost consistently achieved the highest accuracy among the XGBoost-based approaches.
* Hybrid approaches combine the strengths of deep learning and gradient boosting.
* Additional training data improves model generalization and classification performance.

Overall, VGG16 + XGBoost emerged as the best-performing XGBoost-based method for both Brain Tumor MRI and Chest X-Ray classification tasks, demonstrating the value of deep feature extraction in medical image analysis.


---
