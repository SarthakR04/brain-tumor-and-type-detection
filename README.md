# 🧠 Brain Tumor Detection & Classification (Multi-Task Deep Learning)

This project focuses on detecting brain tumors and classifying tumor types using MRI images through a multi-task deep learning approach.

The model simultaneously performs:
- ✅ Tumor Detection (Binary Classification)
- 🧬 Tumor Type Classification (Multi-Class)

---

## 📌 Problem Statement

Brain tumor detection from MRI scans is a critical task in medical diagnostics.

While detecting the presence of a tumor is relatively straightforward, identifying the exact tumor type is significantly more challenging due to subtle visual differences.

This project explores how effectively a single deep learning model can handle both tasks simultaneously.

---

## 🗂️ Dataset

The dataset consists of **7,200 brain MRI images** divided into 4 categories:

- Glioma Tumor  
- Meningioma Tumor  
- Pituitary Tumor  
- No Tumor  

### 📊 Structure
Training/
glioma (1400)
meningioma (1400)
pituitary (1400)
notumor (1400)

Testing/
glioma (400)
meningioma (400)
pituitary (400)
notumor (400)

✔ Balanced dataset  
✔ No data leakage  
✔ Preprocessed before training  

---

## 🧠 Model Architecture

A **multi-task learning model** was implemented using a pretrained CNN backbone.

### 🔧 Key Components:

- Transfer Learning (EfficientNet / CNN backbone)
- Shared feature extractor
- Two output heads:
  - Binary Output → Tumor vs No Tumor
  - Type Output → Glioma / Meningioma / Pituitary

---

## ⚙️ Training Pipeline

- Image resizing (224 × 224)
- Normalization
- Batch-based data generator (memory efficient)
- Optional data augmentation (flip, rotation)

---

## 🔬 Experiments Conducted

Multiple approaches were tested to improve performance:

- ✔ Baseline model (frozen backbone)
- ✔ Fine-tuning (unfreezing layers)
- ✔ Data augmentation
- ✔ Loss balancing
- ✔ Custom loss exploration
- ✔ Image size variation

---

## 📊 Results

### 🔹 Model Performance

| Metric                  | Value |
|------------------------|------|
| Binary Accuracy        | ~82–84% |
| Type Accuracy          | ~35–48% |

---

## 🔍 Observations

- ✅ Tumor detection performed well and remained stable.
- ⚠️ Tumor type classification was significantly harder.
- 🧠 Subtle differences between tumor types limited model performance.
- ⚖️ Multi-task learning introduced **task interference**, where the easier task (binary classification) dominated learning.

---

## 🧠 Key Insight

> Increasing model complexity does not always improve performance.

Despite applying advanced techniques like fine-tuning and augmentation, improvements in tumor type classification were limited.

This highlights real-world challenges in medical image classification.

---

## 📉 Challenges

- Fine-grained classification between tumor types
- Shared feature representation limitations
- Model instability during advanced tuning
- Trade-off between simplicity and performance

---

## 🚀 Future Improvements

- Separate models for detection and classification
- Attention-based architectures
- Larger and higher-resolution datasets
- Medical-specific pretrained models

---

## 💡 What I Learned

- Multi-task learning is powerful but tricky
- Debugging deep learning pipelines is non-trivial
- Real-world datasets behave differently than textbook examples
- Simpler models can sometimes outperform complex ones

---

## 🛠️ Tech Stack

- Python  
- TensorFlow / Keras  
- OpenCV  
- NumPy  

---

## 📌 Conclusion

This project demonstrates that:

- Deep learning can effectively detect brain tumors from MRI images
- Fine-grained classification remains a challenging problem
- Model design and problem understanding are more important than blindly increasing complexity

---

## ⭐ If you found this project useful, consider giving it a star!
