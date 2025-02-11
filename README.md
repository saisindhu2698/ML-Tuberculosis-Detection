# 🩺 Detection of Lung Tuberculosis using Machine Learning

This repository contains the implementation of a machine learning-based approach for detecting lung tuberculosis using chest X-ray images. The project explores different classification techniques, including K-Nearest Neighbors (KNN), Distance Weighted KNN, and Gradient Boosting, to determine the most effective model for tuberculosis detection.

---

## 📌 Project Overview

Tuberculosis (TB) is a life-threatening bacterial infection primarily affecting the lungs. According to WHO reports, over 1.2 million people die from TB annually, with a significant number of cases occurring in South-East Asia. Early detection is crucial for timely medical intervention and improving survival rates.

This project employs machine learning models to classify lung X-ray images as **TB-positive** or **TB-negative** using supervised learning algorithms. The dataset comprises **155 chest X-ray images**, preprocessed and analyzed to enhance diagnostic accuracy.

---

## 🏥 Introduction

The rapid growth of biomedical data presents opportunities for leveraging **machine learning (ML)** in healthcare applications. Medical data mining allows for the extraction of critical insights, assisting healthcare professionals in diagnosing diseases like TB.

**Challenges in TB detection:**
- Variability in X-ray images makes manual diagnosis difficult.
- High false-positive and false-negative rates in traditional screening methods.
- Need for automated, AI-driven diagnostic tools for rapid assessment.

This project applies **ML classification techniques** to overcome these challenges, comparing multiple algorithms to determine the most effective approach.

---

## 🔧 Data Preprocessing

**Dataset Information:**
- Collected from **SourceForge**.
- Contains **155 X-ray images**, evenly distributed between **TB-positive** and **TB-negative** cases.
- Images were originally of variable sizes (~60KB each).

**Preprocessing Steps:**
1. **Image Resizing:** Standardized all images to **600x600** pixels.
2. **Inversion:** Applied image transformations to enhance contrast.
3. **Background Adjustments:** Used image processing techniques to improve image quality.
4. **Data Splitting:** Separated into **training** and **testing** datasets.

---

## 📊 Model Training

The following **machine learning classifiers** were implemented:

### 1️⃣ Local K-Nearest Neighbors (Local KNN)
- A lazy learning algorithm that classifies data points based on the majority vote of their nearest neighbors.
- The model determines the **optimal value of K** through experimentation.

### 2️⃣ Distance Weighted K-Nearest Neighbors (DW-KNN)
- A variation of KNN that assigns **higher weights to closer neighbors** to improve accuracy.
- Reduces misclassification by emphasizing nearby data points.

### 3️⃣ Gradient Boosting Classifier
- An ensemble learning method that builds models sequentially, correcting previous errors.
- Fine-tuned using various **learning rates** for optimal performance.

**Cross-validation** was used to ensure robustness in model evaluation.

---

## 📈 Evaluation and Results

**Performance Metrics Used:**
- **Accuracy:** Measures the overall correctness of the model.
- **Precision & Recall:** Evaluates false positives and false negatives.
- **F1-score:** Balances precision and recall for a more comprehensive assessment.

| Model                | Accuracy | Precision | Recall | F1-score |
|----------------------|---------|-----------|--------|----------|
| Local KNN           | 67%     | 0.70      | 0.67   | 0.66     |
| Weighted KNN        | 69%     | 0.79      | 0.73   | 0.72     |
| Gradient Boosting   | **73.8%**  | -         | -      | -        |

✅ **Gradient Boosting** achieved the highest accuracy of **73.8%**, outperforming both KNN variants.

---

## 🔍 Conclusion

This study demonstrates that **machine learning** can enhance tuberculosis diagnosis through automated image classification. The results show that **Gradient Boosting** is the most effective classifier among the tested models.

### **Key Takeaways:**
- **Preprocessing techniques** play a crucial role in improving model accuracy.
- **Distance-weighted KNN** performed better than basic KNN due to its emphasis on closer neighbors.
- **Ensemble learning techniques** (Gradient Boosting) yielded the best performance.
- The approach can be further improved using **deep learning (CNNs)** for better feature extraction.

### 🔮 **Future Work**
- Expand the dataset for more robust generalization.
- Implement **deep learning models (CNNs)** for advanced image analysis.
- Develop a **real-time TB detection system** for clinical use.
