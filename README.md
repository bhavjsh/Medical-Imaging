# 🧠 Brain Tumor MRI Detection

## Overview
This project uses **Deep Learning (CNN)** to detect whether an MRI scan of the brain shows a **Tumor** or **No Tumor**.  
It demonstrates all key steps — dataset preparation, training, testing, and visualization — using **TensorFlow** and **Keras**.

---

## Objective
To build an image classification model that can automatically identify brain tumors from MRI images and support early diagnosis.

---

## Dataset
**Source:** [Kaggle – Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)  
**Classes:** Tumor / No Tumor  
**Total Images:** 253 (80% training, 20% validation)

> The dataset is not uploaded here due to size limits.  
> After downloading from Kaggle, arrange it as:
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

## Tools & Libraries
- Python  
- TensorFlow & Keras  
- NumPy, Matplotlib, scikit-learn, Pillow  
- Jupyter Notebook / VS Code  

---

## How to Run
1. Clone this repository  
   ```bash
   git clone https://github.com/bhavjsh/Medical-Imaging.git
   cd Medical-Imaging
Install dependencies

bash
Copy code
pip install tensorflow matplotlib numpy pillow scikit-learn
Open and run the notebook

bash
Copy code
jupyter notebook BrainTumor_Project.ipynb
Results
Validation Accuracy: ~88%

Metrics used: Accuracy, Precision, Recall, F1-Score, ROC-AUC

Visual outputs include:

Confusion Matrix

ROC Curve

Sample Predictions (Correct vs Incorrect)

Clinical Relevance
This model helps radiologists in faster MRI screening, improving diagnostic accuracy and reducing manual workload.

Project Files
css
Copy code
BrainTumor_Project.ipynb   → Main code notebook  
Report.docx                → Detailed project report  
Slides.pptx                → Presentation slides  
README.md                  → Project summary  
yaml
Copy code
