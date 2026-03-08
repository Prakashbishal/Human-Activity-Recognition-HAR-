# COMP6246 – Machine Learning Technologies Coursework  
### Human Activity Recognition using SO-Lively Dataset

This repository contains the implementation notebook and supporting files for the COMP6246 Machine Learning Technologies coursework at the University of Southampton.

The project focuses on building three end-to-end machine learning pipelines for **Human Activity Recognition (HAR)** using accelerometer data:

1. **Unsupervised Learning:** K-Means  
2. **Classic Supervised Learning:** Random Forest  
3. **Deep Learning:** Convolutional Neural Network (CNN)

---


---

## 🧹 Preprocessing Summary

- All training CSV subjects concatenated  
- Dropped all cycling activities (13, 14, 130, 140)  
- Merged stairs up (4) and stairs down (5) into class **9**  
- Walking class explored using sampling, time-series plots, and ENMO  
- Timestamp parsed and sampling rate verified (≈100 Hz)  
- Cleaned dataset saved as:  
  `data/cleaned/train_cleaned.csv`

---

## 🧠 Models Implemented

### **1. K-Means (Unsupervised)**
- Feature-based clustering  
- Baseline (10 features) + fine-tuned (<20 features)  
- Evaluation using external metrics and class confusion

### **2. Random Forest (Supervised)**
- Classic feature-based classifier  
- Cross-validation scoring  
- Training error, generalisation error, misclassification analysis

### **3. CNN (Deep Learning)**
- Window-based representation  
- Multiple convolution + pooling layers  
- Fine-tuned architecture  
- Training/validation metrics visualisation

---

## 📊 Windowing Approach

- Window size: **2 seconds**  
- Overlap: **1 second**  
- Approx. window length: **200 samples**  
- Generated for all non-cycling classes

---

## 📝 GenAI Declaration

All report writing is done manually as per the COMP6246 GenAI policy.  
Generative AI tools were used only for:
- Code debugging (A1)  
- Grammar & formatting checks (A2)  
- High-level feedback or source recommendations (A4)  

No generative AI was used to write sections of the report.

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/Source_code.ipynb
