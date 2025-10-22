# 🔬 Breast Cancer Detection Mini Project
## Utilizing Machine Learning

<img src="./img/createdbyai.png" alt="An image related to Breast Cancer Detection">

---

# What is Breast Cancer?

Breast cancer is a disease in which cells in the breast grow out of control. It typically starts in the inner lining of milk ducts or the lobules that supply the ducts with milk. These cancer cells can form a mass or tumor and, if left unchecked, can metastasize (spread) to other parts of the body.

---
**Prevalence (Global Statistics)**

- **Global Burden (2022):** Breast cancer is the **most commonly diagnosed cancer worldwide**, with an estimated **2.3 million** new cases diagnosed globally in women.
- **Mortality Rate (Example/US based):** About **41,760** women will die from breast cancer (based on recent US estimates). This stark figure underscores the critical need for advanced and accurate early detection tools.

To illustrate the global variation, here are the estimated **Age-Standardized Incidence Rates (ASR)** per 100,000 women in selected countries (2022 Data):

| Country | ASR (per 100,000) |
| :---: | :---: |
| **France (Metropolitan)** | **105.4** |
| **United States** | **95.9** |
| **Germany** | **78.0** |
| **Brazil** | **52.2** |
| **Iran (Estimate)** | **47.7** |
| **China** | **33.0** |
| **India** | **26.6** |

**Reference:** These figures are sourced from the **Global Cancer Observatory (GLOBOCAN 2022)**, developed by the International Agency for Research on Cancer (IARC), which is a part of the World Health Organization (WHO).


# Role Of Machine Learning In Detection Of Breast Cancer

Machine Learning plays a crucial role by enabling systems to analyze complex patterns within medical data (such as biopsy results, mammograms, and patient records). Classification models are trained to accurately distinguish between **Benign** (non-cancerous) and **Malignant** (cancerous) tumors, thereby assisting medical professionals in early diagnosis and significantly improving screening accuracy.

---

# WHAT DID I DO AND WHAT IS THE RESULTS:



## 🎯 Overview

## 💾 Dataset and Preprocessing

The project utilizes the **Wisconsin Breast Cancer (Diagnostic) Dataset**.

| Characteristic | Value |
| :--- | :--- |
| **Number of Instances** | 569 |
| **Number of Attributes** | 30 numerical, predictive features (e.g., radius, texture, perimeter) |
| **Target Variable** | Malignant (1) or Benign (0) |

### Preprocessing Steps

1.  **Data Splitting**: The dataset was divided into an 80% Training set and a 20% Test set.
2.  **Feature Scaling**: All 30 numerical features were normalized to the range (0, 1) using the `MinMaxScaler` from Scikit-learn to ensure features contribute equally to the model training.

## 🤖 Models Tested

The following seven classification models were trained and evaluated on the preprocessed data:

1.  Gaussian Naive Bayes (`GaussianNB`)
2.  **K-Nearest Neighbors (`KNN`)**
3.  Decision Tree Classifier
4.  Random Forest Classifier
5.  Support Vector Machine (`SVM`) - with a 'poly' kernel
6.  Logistic Regression
7.  Artificial Neural Network (`ANN`) - via `MLPClassifier`

## 📊 Results and Performance Analysis

Model performance was primarily assessed using **Test Accuracy** (for generalization) and **Recall** (to minimize False Negatives, which is critical in medical diagnosis).

### Performance Summary

| Model | Train Accuracy | **Test Accuracy** | Precision | **Recall** |
| :--- | :--- | :--- | :--- | :--- |
| **KNN** | 0.989 | **0.991** | 0.986 | **1.000** |
| SVM | 0.989 | **0.982** | 0.973 | **1.000** |
| ANN (MLP) | 0.989 | **0.982** | 0.973 | **1.000** |
| Logistic Regression | 0.978 | 0.965 | 0.959 | 0.986 |
| Random Forest | 0.996 | 0.965 | 0.959 | 0.986 |
| Naive Bayes | 0.941 | 0.947 | 0.919 | 0.958 |
| Decision Tree | **1.000** | 0.930 | 0.908 | 0.972 |

### Key Findings

* **Optimal Performance**: The **KNN**, **SVM**, and **ANN** models demonstrated the highest performance.
* **Critical Recall Score**: Crucially, **KNN, SVM, and ANN** all achieved a perfect **Recall score of 1.000** on the test set. This means the models correctly identified **100% of the actual malignant cases**, which is the most important factor in this medical application to ensure no cancer case is missed (zero False Negatives).
* **Overfitting**: The Decision Tree model showed signs of overfitting (100% Train Accuracy vs. 93.0% Test Accuracy).

## ✅ Final Conclusion

The **K-Nearest Neighbors (KNN)** model is selected as the best classifier for this task, achieving the highest Test Accuracy of **0.991** while maintaining a perfect **1.000 Recall** score.



# Final Note

I am genuinely excited about this project! My intense interest in **Artificial Intelligence** motivated me to start learning Machine Learning. After grasping the foundational steps and completing several smaller practice projects, I have now embarked on one of the most rewarding, practical, and much-needed applications in the fields of medicine and AI.

Through this project, besides learning core Machine Learning concepts, I have gained profound and valuable insights into breast cancer, particularly the painful reality of its mortality rates. This knowledge has further fueled my strong motivation to develop better and more accurate detection projects in the future, ultimately aiming to help improve early diagnosis.

I am following this project by utilizing educational resources available on the internet and drawing inspiration from the structure and methodologies of previously completed projects in the ML community to gain a deeper understanding and prepare for future projects...