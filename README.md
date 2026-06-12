# Medical Image Classification Projects

Machine Learning and Deep Learning projects for medical image classification using SVM, CNN, Transfer Learning, PCA, XGBoost, and Hybrid Deep Learning approaches.

---

# 1. Project Overview

Medical image classification plays a significant role in assisting healthcare professionals with disease diagnosis and early detection. This repository explores both classical machine learning and modern deep learning approaches for classifying medical images across multiple datasets.

The project compares:

* Support Vector Machines (SVM)
* Convolutional Neural Networks (CNN)
* Transfer Learning using MobileNet
* Principal Component Analysis (PCA)
* XGBoost
* VGG16 + XGBoost Hybrid Models

The objective is to evaluate how different approaches perform on medical imaging tasks while studying the impact of feature engineering, dimensionality reduction, transfer learning, and training dataset size.

---

# Key Achievements

* Implemented SVM, CNN, Transfer Learning, PCA and XGBoost pipelines.
* Compared classical machine learning and deep learning approaches.
* Evaluated models on Brain Tumor MRI and Chest X-Ray datasets.
* Performed training-percentage experiments (20%, 40%, 60%, 80%).
* Implemented VGG16 feature extraction combined with XGBoost classification.
* Generated confusion matrices, classification reports and performance visualizations.
* Managed development using Git, GitHub and WSL Ubuntu.

---

# 2. Repository Structure


Medical-Image-Classification-Projects

├── Exersize-1(BrainTumour-SVM)
├── Exersize-2(ChestXRay)
├── Exersize-3
├── Medical_Image_Classification_Report.md
└── README.md


---

# 3. Datasets

## Brain Tumor MRI Dataset

### Classes

* No Tumor
* Glioma Tumor
* Meningioma Tumor
* Pituitary Tumor

### Task

Multi-Class Classification

### Techniques Evaluated

* Linear SVM
* RBF SVM
* MobileNet Transfer Learning
* Original XGBoost
* PCA + XGBoost
* VGG16 + XGBoost

---

## Chest X-Ray Dataset

### Classes

* Normal
* Pneumonia

### Task

Binary Classification

### Techniques Evaluated

* Linear SVM
* CNN (MobileNet)
* Original XGBoost
* PCA + XGBoost
* VGG16 + XGBoost

---

# Exercise-1: Brain Tumor Classification

## Objective

Classify MRI brain scans into four categories using classical machine learning and transfer learning approaches.

---

## Linear SVM

### Method Overview

* Image preprocessing
* Normalization
* PCA dimensionality reduction
* Linear kernel SVM

### Notebook


[Open Notebook](./Exersize-1%28BrainTumour-SVM%29/Code/Brain.ipynb)


### Final Results

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | XX.XX% |
| F1 Score    | XX.XX% |
| Specificity | XX.XX% |

---

## RBF SVM

### Method Overview

* Image preprocessing
* PCA dimensionality reduction
* Radial Basis Function kernel
* Multi-class classification

### Notebook

[Open Notebook](./Exersize-1%28BrainTumour-SVM%29/Code/Brain.ipynb)

### Final Results

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | XX.XX% |
| F1 Score    | XX.XX% |
| Specificity | XX.XX% |

---

## MobileNet Transfer Learning

### Method Overview

* MobileNet pretrained on ImageNet
* Frozen feature extractor
* Transfer learning
* Softmax output layer

### Notebook


[Open Notebook](./Exersize-1%28BrainTumour-SVM%29/Code/BrainTumor_TransferLearning.ipynb)


### Final Results

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 70.56% |
| F1 Score    | 68.00% |
| Specificity | XX.XX% |

---

## Exercise-1 Performance Comparison

| Model      | Accuracy | F1 Score | Specificity |
| ---------- | -------: | -------: | ----------: |
| Linear SVM |   XX.XX% |   XX.XX% |      XX.XX% |
| RBF SVM    |   XX.XX% |   XX.XX% |      XX.XX% |
| MobileNet  |   70.56% |   68.00% |      XX.XX% |

---

## Key Visualizations

* Confusion Matrix
* Training Percentage Accuracy Plot
* MobileNet Learning Curves
* Classification Reports

---

# Exercise-2: Chest X-Ray Classification

## Objective

Classify Chest X-Ray images into Normal and Pneumonia categories using classical machine learning and deep learning approaches.

---

## Linear SVM

### Method Overview

* Image preprocessing
* Flattened grayscale features
* Linear kernel SVM
* Binary classification

### Notebook

[Open Notebook](./Exersize-2%28ChestXRay%29/Code/ChestXRay_SVM.ipynb)


### Final Results

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | XX.XX% |
| F1 Score    | XX.XX% |
| Specificity | XX.XX% |

---

## CNN (MobileNet)

### Method Overview

* MobileNet architecture
* Data augmentation
* Binary classification
* Model checkpointing

### Notebook

[Open Notebook](./Exersize-2%28ChestXRay%29/Code/ChestXRay_CNN.ipynb)


### Final Results

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 78.35% |
| Precision   | 95.29% |
| Recall      | 72.54% |
| Specificity | 91.73% |
| F1 Score    | 82.37% |
| AUC Score   |   0.93 |

---

## Training Percentage Experiment

| Training % | CNN Accuracy | SVM Accuracy |
| ---------- | -----------: | -----------: |
| 20%        |       69.75% |       74.36% |
| 40%        |       69.75% |       74.04% |
| 60%        |       82.81% |       73.72% |
| 80%        |       85.20% |       75.00% |

### Observation

* Linear SVM performs better when training data is limited.
* CNN performance improves significantly with larger datasets.
* CNN overtakes SVM as training data increases.
* CNN scales more effectively than SVM.

---

## Exercise-2 Performance Comparison

| Model      | Accuracy | F1 Score | Specificity |
| ---------- | -------: | -------: | ----------: |
| Linear SVM |   75.00% |   XX.XX% |      XX.XX% |
| CNN        |   78.35% |   82.37% |      91.73% |

---

## Key Visualizations

* CNN Training Curves
* Confusion Matrix
* ROC Curve
* CNN vs SVM Accuracy Plot

---

# Exercise-3: XGBoost-Based Medical Image Classification

## Objective

Implementation and comparison of:

* Original XGBoost
* PCA + XGBoost
* VGG16 + XGBoost

for both medical imaging datasets.

---

# Brain Tumor Dataset Results

## Original XGBoost

### Method Overview

Raw image features directly classified using XGBoost.

### Notebook

[Open Notebook](./Exersize-3/Code/BrainTumor_XGBoost.ipynb)


### Final Metrics

| Metric   |  Value |
| -------- | -----: |
| Accuracy | 89.55% |

---

## PCA + XGBoost

### Method Overview

PCA dimensionality reduction followed by XGBoost classification.

### Notebook

[Open Notebook](./Exersize-3/Code/BrainTumor_PCA_XGBoost.ipynb)


### Final Metrics

| Metric   |  Value |
| -------- | -----: |
| Accuracy | 90.07% |

---

## VGG16 + XGBoost

### Method Overview

Deep features extracted using VGG16 and classified using XGBoost.

### Notebook

[Open Notebook](./Exersize-3/Code/BrainTumor_VGG16_XGBoost.ipynb)


### Final Metrics

| Metric   |  Value |
| -------- | -----: |
| Accuracy | 90.42% |

---

## Brain Tumor Comparison

| Model            | Accuracy |
| ---------------- | -------: |
| Original XGBoost |   89.55% |
| PCA + XGBoost    |   90.07% |
| VGG16 + XGBoost  |   90.42% |

---

# Chest X-Ray Dataset Results

## Original XGBoost

### Notebook

[Open Notebook](./Exersize-3/Code/ChestXRay_XGBoost.ipynb)


### Final Metrics

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 73.88% |
| F1 Score    | 69.58% |
| Specificity | 65.51% |

---

## PCA + XGBoost

### Notebook

[Open Notebook](./Exersize-3/Code/ChestXRay_PCA_XGBoost.ipynb)


### Final Metrics

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 75.48% |
| F1 Score    | 72.32% |
| Specificity | 68.08% |

---

## VGG16 + XGBoost

### Notebook

[Open Notebook](./Exersize-3/Code/ChestXRay_VGG16_XGBoost.ipynb)


### Final Metrics

| Metric      |  Value |
| ----------- | -----: |
| Accuracy    | 76.92% |
| F1 Score    | 73.75% |
| Specificity | 69.40% |

---

## Chest X-Ray Comparison

| Model            | Accuracy | F1 Score | Specificity |
| ---------------- | -------: | -------: | ----------: |
| Original XGBoost |   73.88% |   69.58% |      65.51% |
| PCA + XGBoost    |   75.48% |   72.32% |      68.08% |
| VGG16 + XGBoost  |   76.92% |   73.75% |      69.40% |

---

## Chest X-Ray Training Percentage Results

| Training % | Original XGBoost | PCA + XGBoost | VGG16 + XGBoost |
| ---------- | ---------------: | ------------: | --------------: |
| 20%        |           72.12% |        71.15% |          74.36% |
| 40%        |           72.92% |        73.88% |          76.28% |
| 60%        |           73.24% |        74.84% |          77.24% |
| 80%        |           73.40% |        75.32% |          76.92% |
| 100%       |           73.88% |        75.48% |          76.92% |

---

## Key Visualizations

* Original XGBoost Accuracy Plot
* PCA + XGBoost Accuracy Plot
* VGG16 + XGBoost Accuracy Plot
* Confusion Matrices
* Classification Reports

---

# Overall Comparative Analysis

## Brain Tumor Dataset

| Model            | Accuracy |
| ---------------- | -------: |
| Linear SVM       |   XX.XX% |
| RBF SVM          |   XX.XX% |
| MobileNet        |   70.56% |
| Original XGBoost |   89.55% |
| PCA + XGBoost    |   90.07% |
| VGG16 + XGBoost  |   90.42% |

---

## Chest X-Ray Dataset

| Model            | Accuracy |
| ---------------- | -------: |
| Linear SVM       |   75.00% |
| CNN              |   78.35% |
| Original XGBoost |   73.88% |
| PCA + XGBoost    |   75.48% |
| VGG16 + XGBoost  |   76.92% |

---

# Conclusion

* Classical machine learning models provide strong baseline performance.
* PCA improves XGBoost performance by reducing noise and redundancy.
* Deep feature extraction using VGG16 consistently improves classification accuracy.
* CNN models perform strongly when sufficient training data is available.
* Hybrid approaches such as VGG16 + XGBoost provide an effective combination of deep feature learning and gradient boosting.

---

# Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn
* TensorFlow / Keras
* XGBoost
* OpenCV
* Jupyter Notebook
* Git
* GitHub
* WSL Ubuntu

---

# References

* Brain Tumor MRI Dataset
* Chest X-Ray Pneumonia Dataset
* Scikit-Learn Documentation
* TensorFlow Documentation
* Keras Documentation
* XGBoost Documentation
* PCA Documentation
* VGG16 Documentation
* Kaggle VGG16 + XGBoost Reference Notebook
