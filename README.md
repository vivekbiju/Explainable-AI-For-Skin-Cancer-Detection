# XAI
Explainable AI for skin cancer detection


This repository contains the source code that implements the research for the MSc dissertation titled "Explainable AI for Skin Cancer Detection". The project evaluates multiple deep learning architectures for classifying dermatoscopic images of skin lesions and employs a suite of Explainable AI (XAI) techniques to interpret the final model's predictions.

**Overview**

The accurate and early diagnosis of melanoma is critical for improving patient outcomes. While deep learning models, particularly Convolutional Neural Networks (CNNs), have achieved dermatologist-level accuracy, their "black box" nature is a significant barrier to clinical adoption. This project tackles that challenge by systematically identifying a high-performing model and then applying various XAI techniques to make its decision-making process transparent and trustworthy.

The key contribution is the empirical validation of an optimal model-explanation pairing (ResNet50 explained by Grad-CAM) as a robust and interpretable pipeline for skin cancer detection.

**Research Workflow**
The research followed a multi-stage funneling process to systematically narrow down the best model and explanation technique.

1.  **Performance Filtering:** Six candidate models were trained and evaluated on performance metrics (accuracy, F1-score) and efficiency.
2.  **Initial XAI Screening:** The top three models were subjected to an initial screening with Grad-CAM and SHAP to assess baseline interpretability.
3.  **In-depth Analysis:** The single best model, **ResNet50**, was selected for a comprehensive analysis using a full suite of five different XAI techniques.

## Dataset

This study utilizes the **Melanoma Cancer Image Dataset** available on Kaggle. It is a publicly available and meticulously curated collection comprising 13,900 dermatoscopic images, with a relatively balanced split between 'Benign' and 'Malignant' classes.

- **Link to Dataset:** [[Link to the Kaggle dataset](https://www.kaggle.com/datasets/bhaveshmittal/melanoma-cancer-dataset)]
- **Image Size:** All images were resized to 224x224 pixels.

## Methodology

### Models Evaluated
Six distinct architectures were evaluated to find the optimal balance of performance and efficiency.
1.  **ResNet50** (Final Selected Model)
2.  **VGG16**
3.  **Xception**
4.  **DenseNet201**
5.  **EfficientNetB0**
6.  **Custom CNN** (Baseline)

### XAI Techniques Used
A diverse suite of XAI techniques was applied to the final ResNet50 model to provide a comprehensive understanding of its behavior.
* **Gradient-Based:** Vanilla Saliency, SmoothGrad
* **Activation-Based:** Grad-CAM, Grad-CAM++
* **Perturbation/Game-Theory-Based:** SHAP (Partition and Kernel Explainers)

## Results

The **ResNet50** model emerged as the top-performing architecture, achieving a **test accuracy of 92.4%** and a **malignant class F1-Score of 0.92**. The systematic XAI comparison revealed that standard **Grad-CAM** provided the most effective, intuitive, and clinically relevant visual explanations for this task.

## Acknowledgements

This work was submitted in partial fulfilment of the requirements for the degree of MSc Artificial Intelligence at the University of Plymouth. My deepest gratitude to my supervisor,Dr Haoyi Wang, for her invaluable guidance.
