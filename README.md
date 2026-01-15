Brain Tumor MRI Detection using Deep Learning

This project focuses on the automated detection of brain tumors from MRI images using Deep Learning, specifically Convolutional Neural Networks (CNNs). The goal is to classify brain MRI scans into two categories: Tumor and No Tumor, helping demonstrate how AI can assist in medical image analysis.

📌 Project Overview

Manual analysis of MRI scans is time-consuming and highly dependent on expert radiologists. With the increasing number of medical images generated daily, there is a strong need for automated and reliable diagnostic support systems.

In this project:

A custom CNN model is trained on brain MRI images.

The model learns visual patterns associated with tumors.

Performance is evaluated using multiple classification metrics.

Visual results are analyzed to understand model behavior.

📂 Dataset

Source: Kaggle – Brain MRI Images for Brain Tumor Detection
https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection

Classes:

Tumor

No Tumor

Total Images: 253

Training set: ~80%

Validation set: ~20%

⚠️ The dataset is not included in this repository due to size limitations.

Expected Folder Structure
data/
├── train/
│   ├── Tumor/
│   └── No Tumor/
└── val/
    ├── Tumor/
    └── No Tumor/

🔍 Exploratory Data Analysis (EDA)

EDA was performed to understand the dataset before training:

Visualized random MRI samples from both classes

Checked class distribution (slight class imbalance observed)

Verified image formats and integrity

Observed intensity patterns and contrast variations

This analysis confirmed that the dataset was suitable for CNN-based modeling after preprocessing.

⚙️ Data Preprocessing

The following preprocessing steps were applied:

Resized all images to a fixed input size

Normalized pixel values to the range [0, 1]

Applied data augmentation techniques such as:

Rotation

Horizontal flipping

Zooming

Used class weights to handle minor class imbalance

🧠 Model Architecture

A custom CNN model was built from scratch with the following key components:

Convolutional layers with ReLU activation

Max-pooling layers for spatial reduction

Fully connected (dense) layers

Dropout for regularization

Sigmoid activation for binary classification

The model was intentionally kept lightweight to allow training on a CPU environment.

🏋️ Model Training

Framework: TensorFlow / Keras

Optimizer: Adam

Loss Function: Binary Cross-Entropy

Batch Size: 8

Epochs: 10

Hardware: CPU

Training Observations

Accuracy improved steadily from ~65% to ~88%

Training and validation curves showed stable learning

No significant overfitting was observed

The trained model was saved for reuse:

model_a.keras

checkpoint_best.keras

📊 Model Evaluation

The model was evaluated on the validation dataset using standard metrics:

Metric	Score
Accuracy	0.88
Precision	0.85
Recall	0.89
F1-Score	0.87
ROC-AUC	0.90
Additional Analysis

Confusion matrix showed strong true positive and true negative rates

ROC curve demonstrated good class separation

Visual prediction samples confirmed reliable generalization

🖼️ Visualization Results

The notebook includes:

Class distribution plots

Sample MRI images from both classes

Confusion matrix visualization

ROC curve

Correctly and incorrectly classified MRI examples

These visualizations help interpret model behavior and performance.

🏥 Clinical Relevance

Although not intended to replace radiologists, this system demonstrates how AI can:

Assist in early brain tumor screening

Reduce diagnostic workload

Support decision-making in resource-limited settings

Improve efficiency in medical imaging workflows

⚠️ Limitations & Future Work

Current Limitations

Small dataset size

Training performed on CPU

Limited model interpretability

Future Improvements

Use larger and more diverse datasets

Experiment with pre-trained models (ResNet, EfficientNet)

Apply explainable AI techniques (e.g., Grad-CAM)

Optimize model for clinical deployment

▶️ How to Run

Clone the repository:

git clone https://github.com/bhavjsh/Medical-Imaging.git
cd Medical-Imaging


Download the dataset from Kaggle and arrange it as shown above.

Open the notebook:

jupyter notebook BrainTumor_Project.ipynb


Run all cells sequentially.

📁 Repository Contents

BrainTumor_Project.ipynb – Main Jupyter Notebook

README.md – Project documentation

Report.docx – Detailed project report

Slides.pptx – Project presentation

model_a.keras – Trained CNN model

checkpoint_best.keras – Best model checkpoint

✅ Conclusion

This project demonstrates the practical application of deep learning in medical imaging. The CNN model successfully learned meaningful patterns from MRI scans and achieved strong performance, highlighting the potential of AI-assisted diagnostic tools in healthcare.
