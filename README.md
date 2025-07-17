# lidc_classification
# LIDC Lung Nodule Classification

This project performs **binary classification of lung nodules** (Benign vs. Malignant) using the **LIDC-IDRI dataset**. It utilizes a ResNet-based convolutional neural network and is implemented in PyTorch.

## 📌 Objective

To build a deep learning pipeline that:
- Extracts lung nodules from DICOM images using segmentation annotations from XML files
- Classifies the nodules as **benign (0)** or **malignant (1)** based on their size and characteristics
- Evaluates the classification performance using standard metrics

---

## 📂 Dataset

- **Dataset**: [LIDC-IDRI](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI)
- **Format**: DICOM images with accompanying XML annotations
- **Preprocessing**:
  - Extract axial slices containing nodules
  - Label nodules: 
    - **Benign (0)** if diameter < 3mm
    - **Malignant (1)** if diameter ≥ 3mm

---

## 🧠 Model

- **Architecture**: `ResNet50` / `ResNet101V2` (customizable)
- **Input Size**: 224×224 grayscale
- **Loss Function**: Binary Cross Entropy
- **Optimizer**: Adam
- **Metrics**: Accuracy, Precision, Recall, F1-Score

---

## 🔧 Installation

```bash
git clone https://github.com/madhumetha26/lidc_classification.git
cd lidc_classification

