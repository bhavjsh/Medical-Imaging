# Brain Tumor MRI Detection using Deep Learning

This project demonstrates an automated approach for detecting **brain tumors from MRI images** using **Deep Learning** techniques. A **Convolutional Neural Network (CNN)** is trained to classify MRI scans into **Tumor** and **No Tumor**, highlighting the potential of AI in medical image analysis.

---

## Project Overview

Manual examination of MRI scans is time-consuming and highly dependent on expert radiologists. With the increasing volume of medical imaging data, automated diagnostic support systems are becoming essential.

In this project:
- Brain MRI images are classified using a CNN
- The model learns visual patterns associated with tumors
- Performance is evaluated using standard classification metrics
- Results are visualized to assess model reliability

---

##  Dataset

- **Source:** Kaggle – Brain MRI Images for Brain Tumor Detection  
  https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection

- **Classes:**  
  - Tumor  
  - No Tumor  

- **Total Images:** 253  
  - Training set: ~80%  
  - Validation set: ~20%

> ⚠️ The dataset is **not included** in this repository due to size constraints.

### Expected Directory Structure

data/
├── train/
│ ├── Tumor/
│ └── No Tumor/
└── val/
├── Tumor/
└── No Tumor/

yaml
Copy code

---

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to understand the dataset before model training.

**Key EDA steps:**
- Visualized random MRI samples from both classes
- Checked class distribution and balance
- Verified image formats and integrity
- Observed pixel intensity and contrast variations

EDA confirmed that the dataset was clean, consistent, and suitable for CNN-based modeling.

---

## ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- Resized images to a uniform input size
- Normalized pixel values to the range [0, 1]
- Applied data augmentation:
  - Rotation
  - Horizontal flipping
  - Zooming
- Used class weights to reduce the effect of class imbalance

---

## Model Architecture

A **custom CNN model** was developed from scratch, consisting of:

- Convolutional layers with ReLU activation
- Max-pooling layers for feature reduction
- Fully connected (dense) layers
- Dropout for regularization
- Sigmoid activation for binary classification

The architecture was kept lightweight to allow training on a CPU environment.

---

##  Model Training

- **Framework:** TensorFlow / Keras  
- **Optimizer:** Adam  
- **Loss Function:** Binary Cross-Entropy  
- **Batch Size:** 8  
- **Epochs:** 10  
- **Hardware:** CPU  

**Training observations:**
- Accuracy improved steadily from ~65% to ~88%
- Loss decreased consistently
- Training and validation curves showed stable learning
- No major overfitting was observed

The trained model was saved for future use.

---

##  Model Evaluation

The model was evaluated on the validation dataset using multiple metrics.

| Metric      | Score |
|-------------|-------|
| Accuracy    | 0.88  |
| Precision   | 0.85  |
| Recall      | 0.89  |
| F1-Score    | 0.87  |
| ROC-AUC     | 0.90  |

**Evaluation insights:**
- Strong true positive and true negative rates
- Most errors occurred on images with faint tumor boundaries
- ROC curve indicated good class separation
- Visual predictions showed reliable generalization

---

##  Visualization Results

The notebook includes:
- Class distribution plots
- Sample MRI images from both classes
- Confusion matrix visualization
- ROC curve
- Correct and incorrect prediction examples

These visualizations help interpret model performance and behavior.

---

## Clinical Relevance

This project demonstrates how AI can support medical imaging workflows by:

- Assisting in early brain tumor screening
- Reducing diagnostic workload
- Supporting radiologists in prioritizing critical cases
- Improving efficiency in healthcare environments

> This system is intended as a **decision-support tool**, not a replacement for medical professionals.

---

##  Limitations & Future Work

**Current limitations:**
- Small dataset size
- Training limited to CPU hardware
- Limited model interpretability

**Future improvements:**
- Use larger and more diverse MRI datasets
- Experiment with pre-trained models (ResNet, EfficientNet)
- Apply explainable AI techniques such as Grad-CAM
- Optimize the model for real-world clinical deployment

---

## How to Run the Project

1. Clone the repository:
git clone https://github.com/bhavjsh/Medical-Imaging.git
cd Medical-Imaging

2. Download the dataset from Kaggle and organize it as shown above.

3. Open the notebook:

jupyter notebook BrainTumor_Project.ipynb

4 .Run all cells sequentially.

 Repository Contents

BrainTumor_Project.ipynb – Main Jupyter Notebook

README.md – Project documentation

Report.docx – Detailed project report

Slides.pptx – Project presentation

model_a.keras – Trained CNN model

checkpoint_best.keras – Best model checkpoint

 Conclusion
This project successfully demonstrates the application of deep learning for brain tumor detection from MRI scans. The CNN model achieved strong performance and highlights the potential of AI-assisted diagnostic tools in medical imaging.
