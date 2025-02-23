<h1>Brain Tumor MRI Classification - README</h1>


Required Packages for Brain Tumor Classification

To successfully run and train models using the brain tumor classification dataset, the following Python packages are required:

Essential Libraries

These are the fundamental packages necessary for handling data and building models:

numpy: Efficient numerical computations

pandas: Data manipulation and analysis

matplotlib: Visualization of data and model performance

seaborn: Statistical data visualization

Image Processing

These packages help in handling and preprocessing image data:

opencv-python: Image manipulation and augmentation

Pillow (PIL): Image file handling and conversions

----------------------

Project Overview

This project focuses on classifying MRI brain scan images into four categories:

Glioma

Meningioma

Pituitary

No Tumor

The classification is achieved using multiple supervised machine learning models, including Logistic Regression, Random Forest, Support Vector Machine (SVM), and K-Nearest Neighbor (KNN). The dataset is sourced from Kaggle and contains MRI images in JPEG format.

Dataset and Preprocessing

The dataset was initially downloaded from Kaggle and contains 7,023 images.

426 duplicate images were removed, leaving 6,597 unique images.

All images were resized to ensure uniformity.

Grayscale conversion was applied to maintain consistency.

Pixel values were normalized to the range [0,1].

Exploratory Data Analysis (EDA)

A heatmap was generated by averaging images within each class to observe structural differences.

Principal Component Analysis (PCA) was applied to visualize class separation.

Models Used and Hyperparameter Tuning

The following models were implemented with feature standardization:

1. Logistic Regression

Achieved 86% accuracy.

Performed poorly on pituitary classification.

AUC scores indicated weaker performance on pituitary and no tumor categories.

2. Random Forest

Achieved 92% accuracy.

The number of trees (n_estimators) was determined using the Out-of-Bag (OOB) error rate, with 60 chosen as the optimal value.

AUC analysis confirmed strong performance, though pituitary classification remained the weakest.

3. Support Vector Machine (SVM)

Achieved 86% accuracy.

The regularization parameter (C) was tuned, with an optimal range of 2-4.

AUC scores were high except for pituitary, which performed the worst.

4. K-Nearest Neighbor (KNN)

Achieved 89% accuracy.

The number of neighbors (K) was tuned using cross-validation, with K=2 chosen.

High misclassification between no tumor and pituitary categories.

Results and Conclusion

Random Forest had the highest accuracy (92%), followed by KNN (89%), SVM (86%), and Logistic Regression (86%).

Overfitting is suspected in KNN and SVM due to high accuracy but inconsistencies in performance.

Supervised learning models worked well, but deep learning models may be more suitable for complex image data.

Future improvements could include using convolutional neural networks (CNNs) for better feature extraction.

References

Dataset: [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data)
